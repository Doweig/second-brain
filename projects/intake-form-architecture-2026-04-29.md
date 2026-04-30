# Intake Form Architecture — 2026-04-29

## Why this plan exists

Three overlapping Linear tickets got drafted in one session about intake form changes:

- [ORBA-238](https://linear.app/orba-health/issue/ORBA-238) — polish (separators, scale direction, ID upload, copy)
- [ORBA-239](https://linear.app/orba-health/issue/ORBA-239) — versioning + re-ask after form bumps
- [ORBA-244](https://linear.app/orba-health/issue/ORBA-244) — draft persistence (per-step save + resume)

They're all symptoms of the same architectural gap: the intake response is one big JSON blob, submitted in one shot, with no per-field metadata. Every "improve the intake" ask becomes awkward because the data shape doesn't support it.

Today's blocker driving this:
- We want to add new questions. Existing v1 users will silently lack those answers.
- There's no resume — close the tab at step 4 of 7 and you start over.
- "Have you filled the intake?" is a single yes/no — once yes, you're done forever, no way to retake or update specific questions.
- William mentioned wanting question decay later (e.g., re-ask mood every 6 months). That has nowhere to live in the current shape.

This plan lands on the destination, then chunks it into PR-sized tickets. The 3 existing tickets fold into the new structure.

## Vision (the destination)

A field-level versioned intake where:

1. **Every field has a definition row** with a stable `field_key`, current `version`, and metadata (label, type, options, required, optional `decay_after_days`). Adding a question = insert a definition row + bump catalog version.

2. **Every user answer carries field-level provenance**: which `field_key`, which `version`, when answered. Either inside the JSON blob as structured metadata, or in a normalized child table (TBD — see Architecture).

3. **A single `getMissingFields(user)` engine** answers "what does this user need to fill?" considering: never-answered, answered-an-old-version, answered-a-decayed-question. Same engine powers:
   - draft resume (the user is mid-form),
   - re-ask after schema bump (we added a question since they finished),
   - periodic decay (their mood answer is 6 months old).

4. **Partial save**: `PUT /intake/draft` accepts any subset of field answers, idempotent, doesn't trigger required-field validation. Final `POST /intake/submit` validates strict and marks the response complete.

5. **Friendly UX surfaces**:
   - Mid-flight intake → resume on next visit at the first unfilled required step.
   - Completed user, new questions added → dashboard card: "we have 3 new questions, takes 2 min."
   - Completed user, decayed question → dashboard prompt at the decay window.

6. **Backwards-compatible with v1 submissions**. We don't ask 6900001 to redo their intake; we just ask for the new/decayed fields.

## Architecture decision (the load-bearing call)

Three options for where field-level metadata lives. Recommend **C**.

### A — JSON blob + sidecar metadata column

- Keep `intake_responses.payload` as today (single JSON blob).
- Add `intake_responses.field_meta JSONB` storing `{ field_key: { version, answered_at } }` per filled field.
- Add `intake_field_definitions` table (catalog of fields with versions, types, decay rules).

**Pros:** minimum migration. Existing read paths (V1IntakeSchema validation) untouched.
**Cons:** querying "who has answered v1 of field X" requires JSONB ops. Decay queries are awkward. Two sources of truth inside one column.

### B — Fully normalized `intake_field_answers`

- Drop the JSON blob. One row per `(user_id, field_key)` with `version`, `value JSONB`, `answered_at`.
- Add `intake_field_definitions` table.

**Pros:** clean SQL for everything (decay, missing-fields, version drift, analytics). One source of truth.
**Cons:** bigger migration. V1IntakeSchema validation needs to be reconstructed from rows on read. Slower fetch (N rows instead of 1). Touches every existing intake reader.

### C (recommended) — Hybrid

- Keep `intake_responses.payload` JSON blob (reads stay simple, V1IntakeSchema still validates the way it does today).
- Add `intake_field_definitions` table (catalog).
- Add `intake_field_answers` shadow table populated alongside every save: one row per field per user, latest version + answered_at. Powers the missing-fields engine + decay + analytics.
- The blob is the system of record for "what did the user say." The shadow table is the index for "who needs to answer what."
- Single service-layer write helper writes both, so they can't drift.

**Pros:** existing read paths untouched. Fast missing-fields queries. Smooth migration (backfill shadow from existing blobs is straightforward). Decay/analytics queries are clean.
**Cons:** two write sites (mitigated by one helper). Slightly more storage.

## PR-sized ticket breakdown

Each PR is full-stack (API + frontend together, no layer-only PRs). Two PRs total, sequenced.

### PR 1 — Robust intake: foundation + save/resume + retake

**Scope**
- Schema migration: `intake_field_definitions` (catalog: field_key, version, type, options, required, optional `decay_after_days` column from day one for future-proofing) + `intake_field_answers` (shadow: user_id, field_key, version, answered_at). Backfill shadow from existing `intake_responses.payload` rows.
- Service-layer write helper that updates both blob and shadow on every save. Single source of write logic — no path bypasses it. Mitigates the "two write sites" risk of the hybrid architecture.
- Backend: `getMissingFields(user)` engine returning `{ field_key, reason: never_answered | outdated | decayed, step }[]`. (Decay reason wired but no fields opt in yet — covered in PR 2 polish if needed, or a future ticket.)
- Backend: `PUT /intake/draft` (partial save, Zod `V1IntakeSchema.deepPartial()`, idempotent merge into existing payload). Response includes `getMissingFields()` so the client updates without a second roundtrip.
- Backend: `GET /intake/missing` (dashboard read).
- Frontend: per-step save on Next click + resume on mount + jump-to-first-unfilled-required-step + "welcome back, picking up where you left off" toast.
- Frontend: dashboard "we have N new questions" card + mini-intake renderer that shows only missing fields in their original step context. Dismissal window (7 days) before the card reappears.
- Closes ORBA-244 and ORBA-239.

**Verification**
- v1 user logs in: card prompts only for new fields, mini-intake renders them in step context, submit updates blob + shadow + clears the prompt.
- New user mid-form: closes tab at step 4, returns next day, lands on step 4 with answers prefilled.
- Airplane mode mid-step → click Next → toast on failure, local state preserved, retry succeeds when network returns.
- Existing API readers (HOP integration, dashboard, `/intake/:userId` GET) keep working — payload shape unchanged on read.

### PR 2 — Intake polish + new fields

**Scope**
- Step 2 ("A Bit of Background"): improve visual separation between questions.
- Step 3 ("How You Live"): rename `"Portions of fruit or veg per day?"` → `"Portions of vegetables per day?"` + portion-size explainer. Register through catalog as `field_key=lifestyle.veg_portions_per_day`, version bump.
- Step 5 ("How Your Mind Feels"): reverse visual scale for Q2 (purpose) and Q4 (connected). Stored `value` codes unchanged. Per-question option-order override at render site.
- Step 6 ("Longevity Assessment"): passport scan upload (reuse `/upload/presign` + `/upload/complete`) + regulator-citation explainer copy (research the actual Thai regulator: TLO? FDA Thailand? Ministry of Public Health?). Address stays a single free-text textarea — no Thai address/district code integration.
- `form_version` bump to v2. New `intake_field_definitions` rows for added fields (passport upload, vegetables explainer wording).
- Closes ORBA-238.

**Verification**
- Walk all 7 steps end-to-end on preview deploy.
- Q3 in step 5 still reads "Not at all → Very much" (didn't get accidentally swept up in the reverse).
- Step 5 stored `value` codes unchanged (grep HOP / wellbeing scoring consumers).
- Passport scan uploads, retrievable from backoffice patient profile.
- Existing v1 users see the new questions as a "we have new questions" dashboard prompt on next visit (PR 1's mechanism kicks in automatically once the new field_definitions land).

## Linear cleanup proposal (NOT executed yet)

After William approves the cleanup, the following 6 Linear writes happen:

1. **Create new parent ticket** "Intake form architecture v2" — points at this plan file in second-brain, summarizes the 2-PR breakdown, labels `customer` + `Improvement`, priority Medium.
2. **Create new child ticket** "PR 1 — Robust intake: foundation + save/resume + retake (customer-web)" under the parent.
3. **Reuse ORBA-238** as the PR 2 child — set its parent to the new parent ticket, add a comment that it now sequences after PR 1.
4. **Close ORBA-244** as duplicate-of the new PR 1 ticket.
5. **Close ORBA-239** as duplicate-of the new PR 1 ticket.
6. (No standalone PR 2 ticket — ORBA-238 is the PR 2 ticket, just re-parented and recontextualized.)

Net: 2 creates, 1 re-parent + comment, 2 closes. Zero Linear writes happen until William's "go file."

## Decisions made (2026-04-29)

1. **Architecture: C (hybrid).** Keep JSON blob + add `intake_field_definitions` catalog + `intake_field_answers` shadow. Single service-layer write helper for both.
2. **PR breakdown: 2 PRs.** PR 1 = foundation + save/resume + retake (closes ORBA-244 + ORBA-239). PR 2 = polish + new fields (closes ORBA-238). Both full-stack, no API/frontend split.
3. **Decay rules: out of scope** for this sweep. `decay_after_days` column lands in PR 1's schema (cheap), but no fields opt in until a follow-up ticket after PR 1-2 ship.
4. **Review depth: skip /autoplan.** Going straight to ticket cleanup proposal.

## Status

- Plan: drafted + decisions locked (2026-04-29)
- Linear cleanup: drafted, awaiting William's go-ahead before any writes
- Memory: saved `feedback_confirm_before_creating_tickets.md` so the "ask before tickets" rule sticks across sessions
