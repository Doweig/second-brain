# The Vault PR Batch Migration Plan

> Master plan for moving knowledge from `the-vault` into `second-brain` in 10-file PRs, without modifying the source vault and without carrying over tooling/process baggage.

**Goal:** Transfer the knowledge-bearing content of `the-vault` into `second-brain` in small reviewable PRs, ranked by migration confidence, so William can approve, cut, or reclassify each batch before execution.

**Architecture:** Direct knowledge transfer. The source vault stays untouched. Each PR proposes up to 10 files, moved into the best-fit `second-brain` home. Straightforward pages transfer first; duplicate-prone pages are review-first; strategy/spec pages are rewrite-first. Tooling, prompts, and old vault-operating docs are excluded.

**Tech Stack:** markdown, git, GitHub PRs, GBrain-backed `second-brain` repo.

---

## Live path check
- Checked at 2026-04-19 21:13 +07.
- Live source vault found at `/Users/alt/orba-health/the-vault`.
- Live destination repo found at `/Users/alt/orba-health/second-brain`.
- Live company KB found at `/Users/alt/orba-health/knowledge`.
- If the workspace root changes later, update only the two root variables during execution; the chunking and confidence plan stays the same.

## What changed in this redo
- No `archive/the-vault/` staging plan.
- No QMD / skills / tooling migration logic.
- No touching the source vault during planning or execution.
- This is now a straight **knowledge-transfer master plan** with file-level confidence labels and 10-file PR batches.

## Inventory summary
- Total markdown files inspected: **247**
- **Direct transfer**: **99**
- **Review before move**: **120**
- **Rewrite while moving**: **17**
- **Skip / out of scope**: **11**
- At a hard cap of 10 files per PR, this creates **24** execution batches (**23 full batches + 1 tail batch of 6 files**).

## Confidence labels
- **Direct transfer** — confident this is knowledge worth moving with minimal reshaping.
- **Review before move** — probably worth moving, but the PR should confirm duplicate risk, recency risk, or final landing zone.
- **Rewrite while moving** — valuable, but the source file should become a fresh `second-brain` page rather than a verbatim copy.
- **Skip / out of scope** — tooling, prompts, templates, or vault-operating docs; not part of the knowledge transfer.

## Non-negotiable execution rules
- Never edit, delete, or rename anything inside the source vault.
- Each execution PR handles **10 source files max** (except the final tail batch).
- Each PR body must list: source files, per-file confidence label, and proposed destination homes.
- If William asks to drop a file from a PR, drop it and re-push; do not debate the review.
- Do not mix skip/out-of-scope files into migration PRs.
- Do not start with low-confidence duplicate-heavy market research; run the ranked order below.
- Only consider deleting or retiring the source vault after William is happy with the completed transfer.

## Default landing-zone rules
- `people/*.md` -> `people/`
- `companies/*.md` -> `companies/`
- `meeting-notes` -> `meetings/`
- `legal-research` -> `org/` or `projects/` (decide in PR)
- customer / product / market / growth / pitch research -> `projects/` or `org/` or `reports/` (decide in PR)
- strategy / vision / brief / PRD docs -> rewrite into native `second-brain` pages

## Ranked PR batches

### Batch 01 — people pages
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `people/andrew-huberman.md` — Direct transfer
  - `people/anton.md` — Direct transfer
  - `people/art-chawapon-kidhirunkul.md` — Direct transfer
  - `people/art-tanapote.md` — Direct transfer
  - `people/dan-aspire.md` — Direct transfer
  - `people/david-berghaeuser.md` — Direct transfer
  - `people/gift.md` — Direct transfer
  - `people/jiri-dvorak.md` — Direct transfer
  - `people/jonathan-swerdlin.md` — Direct transfer
  - `people/kojchakorn.md` — Direct transfer

### Batch 02 — people pages + company pages
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `people/mark-hyman.md` — Direct transfer
  - `people/nick-warot.md` — Direct transfer
  - `people/niels.md` — Direct transfer
  - `people/peter-attia.md` — Direct transfer
  - `people/swit.md` — Direct transfer
  - `people/tanupol-virunhagarun.md` — Direct transfer
  - `people/william-guillaume.md` — Direct transfer
  - `people/zeth.md` — Direct transfer
  - `companies/acclime-thailand.md` — Direct transfer
  - `companies/aspire-coaching-physio.md` — Direct transfer

### Batch 03 — company pages
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `companies/aspire.md` — Direct transfer
  - `companies/bnh-hospital.md` — Direct transfer
  - `companies/bodycypher.md` — Direct transfer
  - `companies/ezra.md` — Direct transfer
  - `companies/grail.md` — Direct transfer
  - `companies/hum-clinic.md` — Direct transfer
  - `companies/ipc-international.md` — Direct transfer
  - `companies/mainscape.md` — Direct transfer
  - `companies/measureup.md` — Direct transfer
  - `companies/novi-health.md` — Direct transfer

### Batch 04 — company pages + legal research
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `companies/prewell-clinic.md` — Direct transfer
  - `companies/quest-diagnostics.md` — Direct transfer
  - `companies/rabbitcare.md` — Direct transfer
  - `companies/sanwiz-lab.md` — Direct transfer
  - `companies/viatell.md` — Direct transfer
  - `companies/viome.md` — Direct transfer
  - `companies/vitallife-by-bumrungrad.md` — Direct transfer
  - `vault/2026-02/ingested/Corporate structuring playbook for a SEA healthtech expansion.md` — Direct transfer
  - `vault/2026-02/ingested/Launching a prototype with minimal legal structure.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting with Tanapote on Jan 30th 2026.md` — Direct transfer

### Batch 05 — legal research
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/Thailand regulatory and legal roadmap for a health tech dual-entity startup.md` — Direct transfer
  - `vault/2026-03/ingested/bodycypher-legal-master-braindump-2026-03-10.md` — Direct transfer
  - `vault/2026-03/ingested/bodycypher-legal-master-braindump-addendum-2026-03-10.md` — Direct transfer
  - `vault/2026-03/ingested/bodycypher-legal-questions-for-counsel-2026-03-09.md` — Direct transfer
  - `vault/2026-03/ingested/email-tanapote-incorporation-questions-2026-03-18.md` — Direct transfer
  - `vault/2026-03/ingested/foreign-owned-healthtech-thailand-legal-viability.md` — Direct transfer
  - `vault/2026-03/ingested/founders-cap-table-gentlemans-agreement-2026-03-17.md` — Direct transfer
  - `vault/2026-03/ingested/legal-opinion-ipc-tanapote-2026-03-09.md` — Direct transfer
  - `vault/2026-03/ingested/legal-status-2026-03-02.md` — Direct transfer
  - `vault/2026-03/ingested/moph-telemedicine-standards-notification-2021.md` — Direct transfer

### Batch 06 — meeting notes + legal research
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `vault/2026-03/ingested/thai-fda-samd-ai-regulatory-guide-oct-2024.md` — Direct transfer
  - `vault/2026-02/ingested/2026-02-20 Meeting with Tanapote Lawyer.md` — Direct transfer
  - `vault/2026-02/ingested/2026-02-23 Meeting with Acclime.md` — Direct transfer
  - `vault/2026-02/ingested/2026-02-23 Meeting with Swit.md` — Direct transfer
  - `vault/2026-02/ingested/2026-02-24 Meeting with Dr. C.md` — Direct transfer
  - `vault/2026-02/ingested/2026-02-27-context-extraction.md` — Direct transfer
  - `vault/2026-02/ingested/Antonio 2c8ac297948980b99a18d507cf95f4dc.md` — Direct transfer
  - `vault/2026-02/ingested/Call with Rochdy 2fcac29794898059aa41e4e663e7376f.md` — Direct transfer
  - `vault/2026-02/ingested/Marc-Antoine Olive 2c4ac297948980b4890ae465a25ada41.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting Dr W 306ac29794898016bb35e55ebff69f96.md` — Direct transfer

### Batch 07 — meeting notes
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/Meeting with CK 2f7ac297948980d98fcfcbbf91103855.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting with Dr C 30aac29794898037bd16c360a6b57343.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting with Dr Chawapon 2f6ac29794898094abd4d3c3d9b050e7.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting with Olivier 2f8ac297948980cf88d5c0c8d2832ec7.md` — Direct transfer
  - `vault/2026-02/ingested/Meeting with Tanapote 2f8ac297948980da87efe6b8790c50d1.md` — Direct transfer
  - `vault/2026-02/ingested/Niels Jan 22 2f0ac297948980ec8c4aec44038c629a.md` — Direct transfer
  - `vault/2026-02/ingested/Theo J 2c1ac297948980e7927ecf9df79b7d0c.md` — Direct transfer
  - `vault/2026-03/ingested/2026-03-02-context-extraction.md` — Direct transfer
  - `vault/2026-03/ingested/2026-03-03-dr-c-meeting.md` — Direct transfer
  - `vault/2026-03/ingested/2026-03-04-meeting-with-anton.md` — Direct transfer

### Batch 08 — meeting notes
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `vault/2026-03/ingested/2026-03-04-meeting-with-swit.md` — Direct transfer
  - `vault/2026-03/ingested/2026-03-06-weekly-reflection.md` — Direct transfer
  - `vault/2026-03/ingested/2026-03-23-kickoff-brainstorm-voice-memo.md` — Direct transfer
  - `vault/2026-03/ingested/david-berghaeuser-profile.md` — Direct transfer
  - `vault/2026-03/ingested/dr-c-relationship-status-2026-03-02.md` — Direct transfer
  - `vault/2026-03/ingested/meeting-dr-c-2026-03-10.md` — Direct transfer
  - `vault/2026-03/ingested/meeting-tanapote-ipc-2026-03-11.md` — Direct transfer
  - `vault/2026-03/ingested/voice-memo-anton-equity-shares-2026-03-11.md` — Direct transfer
  - `vault/2026-03/ingested/voice-memo-legal-strategy-singapore-incorporation-2026-03-27.md` — Direct transfer
  - `vault/2026-03/ingested/voice-memo-war-council-review-2026-03-16.md` — Direct transfer

### Batch 09 — customer research
- **Confidence:** High confidence
- **Mode:** Direct transfer
- **Mix:** move-now 10, review 0, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/Bangkok Health Clinic Review Analysis.md` — Direct transfer
  - `vault/2026-02/ingested/Thai Consumer Health Checkup Research.md` — Direct transfer
  - `vault/2026-02/ingested/What users actually think about blood test reports and AI health plans.md` — Direct transfer
  - `vault/2026-02/ingested/blood-testing-biohacking-communities.md` — Direct transfer
  - `vault/2026-02/ingested/bodycypher_early_access_survey-v2.md` — Direct transfer
  - `vault/2026-02/ingested/cr4-target-customer-profiles-draft.md` — Direct transfer
  - `vault/2026-02/ingested/customer-sentiment-synthesis.md` — Direct transfer
  - `vault/2026-02/ingested/customer-sentiment-wellness-checkups-bangkok.md` — Direct transfer
  - `vault/2026-02/ingested/gemini-youtube.md` — Direct transfer
  - `vault/2026-03/ingested/ifm-intake-questionnaire.md` — Direct transfer

### Batch 10 — growth docs + pitch docs
- **Confidence:** Mixed confidence
- **Mode:** Mixed — follow per-file labels
- **Mix:** move-now 9, review 1, rewrite 0
- **Files:**
  - `vault/2026-03/ingested/survey-export-2026-03-02.md` — Direct transfer
  - `vault/2026-02/ingested/customer-success-funnel.md` — Direct transfer
  - `vault/2026-02/ingested/sales-funnel.md` — Direct transfer
  - `vault/2026-02/ingested/user-lifecycle.md` — Direct transfer
  - `vault/2026-03/ingested/bodycypher-branding-guidelines.md` — Direct transfer
  - `vault/2026-02/ingested/bodycypher-pitch-deck-v2.md` — Direct transfer
  - `vault/2026-02/ingested/pitch-deck.md` — Direct transfer
  - `vault/2026-03/ingested/bodycypher-story-deck-v3.md` — Direct transfer
  - `vault/2026-03/ingested/dr-chawapon-kidhirunkul.md` — Direct transfer
  - `companies/doctor-anywhere.md` — Review first

### Batch 11 — company pages + product research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `companies/function-health.md` — Review first
  - `companies/insidetracker.md` — Review first
  - `companies/mito-health.md` — Review first
  - `companies/n-health.md` — Review first
  - `companies/nhealth.md` — Review first
  - `companies/siphox-health.md` — Review first
  - `companies/vitalab-thailand.md` — Review first
  - `companies/vitalab.md` — Review first
  - `vault/2026-02/ingested/Bioresonance hair testing is pseudoscience.md` — Review first
  - `vault/2026-02/ingested/action-plan-benchmarking.md` — Review first

### Batch 12 — product research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/biological-age-research.md` — Review first
  - `vault/2026-02/ingested/biomarker-data-sources-research.md` — Review first
  - `vault/2026-02/ingested/biomarkers_all-ranges.md` — Review first
  - `vault/2026-02/ingested/biomarkers_reference-ranges.md` — Review first
  - `vault/2026-02/ingested/bodycypher-blood-panel-v2.md` — Review first
  - `vault/2026-02/ingested/bodycypher-panel-v2.md` — Review first
  - `vault/2026-02/ingested/kirobio.md` — Review first
  - `vault/2026-02/ingested/loinc-adoption-thailand.md` — Review first
  - `vault/2026-02/ingested/loinc-mapping-engine.md` — Review first
  - `vault/2026-02/ingested/mystery-shopping-bdms-wellness-v2.md` — Review first

### Batch 13 — product research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/mystery-shopping-nhealth.md` — Review first
  - `vault/2026-02/ingested/mystery-shopping-pathlab.md` — Review first
  - `vault/2026-02/ingested/mystery-shopping-vitalab.md` — Review first
  - `vault/2026-02/ingested/mystery-shopping-vitals.md` — Review first
  - `vault/2026-02/ingested/nhanes-optimal-reference-ranges-research.md` — Review first
  - `vault/2026-02/ingested/nhealth-lab-quote-QT260174.md` — Review first
  - `vault/2026-02/ingested/ornament-health.md` — Review first
  - `vault/2026-02/ingested/product-review-insidetracker.md` — Review first
  - `vault/2026-02/ingested/product-review-kiro-bio.md` — Review first
  - `vault/2026-02/ingested/product-review-ornament-health.md` — Review first

### Batch 14 — product research + market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/review-siphox-health.md` — Review first
  - `vault/2026-02/ingested/siphoxhealth-v2.md` — Review first
  - `vault/2026-02/ingested/vitalab-supplement-analysis.md` — Review first
  - `vault/2026-02/ingested/vitalab-test-list.md` — Review first
  - `vault/2026-03/ingested/bodycypher-blood-panel-v2-dr-chawapon-nhealth-quote.md` — Review first
  - `vault/2026-03/ingested/bodycypher-landing-page-2026-03-02.md` — Review first
  - `vault/2026-03/ingested/insidetracker-blood-results-dashboard_95c87e7fc272.md` — Review first
  - `vault/2026-03/ingested/insidetracker-blood-results-sections_2026-01-22.md` — Review first
  - `vault/2026-03/ingested/nhealth-b2c-pricing-2026-01-20.md` — Review first
  - `vault/2026-02/ingested/01_superpower.md` — Review first

### Batch 15 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/02_functionhealth.md` — Review first
  - `vault/2026-02/ingested/11_bdms_wellness.md` — Review first
  - `vault/2026-02/ingested/Viome_Competitive_Analysis_for_BodyCypher.md` — Review first
  - `vault/2026-02/ingested/addlife.md` — Review first
  - `vault/2026-02/ingested/bdms-wellness.md` — Review first
  - `vault/2026-02/ingested/bioniq.md` — Review first
  - `vault/2026-02/ingested/bodycypher-market-sizing-v1.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-0cba26fc-fca7-4dff-84ca-ebd87a41a934_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-27bf3caf-476b-4278-bdb3-ebf5cccb2ade_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-2cee0b6d-70c2-40b4-989b-0f602b69f8b4_text_markdown.md` — Review first

### Batch 16 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/compass_artifact_wf-48b7c132-f09d-4381-b71e-2e5639f326b0_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-4b7477e7-3e12-46ff-b969-c1e485dc6120_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-81d92cae-1864-4c50-a05d-bed6ef564a7e_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-9bdcd6d8-3f97-4876-9416-9447656fc80a_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-b61dca90-9721-4868-bacc-00c74cab41dd_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-bbd076f7-5185-4d42-8322-528a802736db_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-c0e9a37e-2845-480e-bc6f-3e9fbf459015_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-c87ee1ab-23b1-47f8-9bdb-854a95b473e1_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-e7c11208-8ae7-4879-8361-5f558e55fc8d_text_markdown.md` — Review first
  - `vault/2026-02/ingested/compass_artifact_wf-eb39e90d-c049-4aac-9f37-e6f2f9fc328c_text_markdown.md` — Review first

### Batch 17 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/compass_artifact_wf-f808004a-1124-4e87-8289-184d9a1ebdcc_text_markdown.md` — Review first
  - `vault/2026-02/ingested/docker-anywhere.md` — Review first
  - `vault/2026-02/ingested/emagene-life.md` — Review first
  - `vault/2026-02/ingested/everlab.md` — Review first
  - `vault/2026-02/ingested/everlywell.md` — Review first
  - `vault/2026-02/ingested/fullscript.md` — Review first
  - `vault/2026-02/ingested/function-health.md` — Review first
  - `vault/2026-02/ingested/genixpro.md` — Review first
  - `vault/2026-02/ingested/healthmatters.md` — Review first
  - `vault/2026-02/ingested/hims.md` — Review first

### Batch 18 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/hum-clinic.md` — Review first
  - `vault/2026-02/ingested/inside-tracker.md` — Review first
  - `vault/2026-02/ingested/international-competitor-synthesis.md` — Review first
  - `vault/2026-02/ingested/intouch-medicare.md` — Review first
  - `vault/2026-02/ingested/kantesti.md` — Review first
  - `vault/2026-02/ingested/lab-plus.md` — Review first
  - `vault/2026-02/ingested/letsgetchecked.md` — Review first
  - `vault/2026-02/ingested/life-force.md` — Review first
  - `vault/2026-02/ingested/looloo.md` — Review first
  - `vault/2026-02/ingested/lucis.md` — Review first

### Batch 19 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/market-sizing-v3.md` — Review first
  - `vault/2026-02/ingested/measureup.md` — Review first
  - `vault/2026-02/ingested/medical-line-lab.md` — Review first
  - `vault/2026-02/ingested/medpro-thailand.md` — Review first
  - `vault/2026-02/ingested/menscape.md` — Review first
  - `vault/2026-02/ingested/menscape_competitive_analysis.md` — Review first
  - `vault/2026-02/ingested/mito.md` — Review first
  - `vault/2026-02/ingested/novi-health.md` — Review first
  - `vault/2026-02/ingested/okcapsule.md` — Review first
  - `vault/2026-02/ingested/persona-nutrition.md` — Review first

### Batch 20 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/pillpack.md` — Review first
  - `vault/2026-02/ingested/prenuvo.md` — Review first
  - `vault/2026-02/ingested/sam-thailand-dtc-blood-testing.md` — Review first
  - `vault/2026-02/ingested/sam-thailand-preventive-health-market.md` — Review first
  - `vault/2026-02/ingested/sanwizlab.md` — Review first
  - `vault/2026-02/ingested/siphox-health-siphoxhealth-v2.md` — Review first
  - `vault/2026-02/ingested/som-bangkok.md` — Review first
  - `vault/2026-02/ingested/som-health-tech-growth-benchmarks.md` — Review first
  - `vault/2026-02/ingested/superpower-autopilot-launch.md` — Review first
  - `vault/2026-02/ingested/superpower-early-access-email.md` — Review first

### Batch 21 — market research
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 10, rewrite 0
- **Files:**
  - `vault/2026-02/ingested/superpower-galleri-email-2026-02-27.md` — Review first
  - `vault/2026-02/ingested/superpower.md` — Review first
  - `vault/2026-02/ingested/tam-sea-dtc-blood-testing.md` — Review first
  - `vault/2026-02/ingested/tam-sea-wellness-preventive-healthcare.md` — Review first
  - `vault/2026-02/ingested/tempus-ai.md` — Review first
  - `vault/2026-02/ingested/thailand-competitor-synthesis.md` — Review first
  - `vault/2026-02/ingested/thainakarin.md` — Review first
  - `vault/2026-02/ingested/transcend-clinic.md` — Review first
  - `vault/2026-02/ingested/viome.md` — Review first
  - `vault/2026-02/ingested/vita-lab.md` — Review first

### Batch 22 — market research + email marketing
- **Confidence:** Medium confidence
- **Mode:** Review before merge
- **Mix:** move-now 0, review 9, rewrite 1
- **Files:**
  - `vault/2026-02/ingested/vitallife.md` — Review first
  - `vault/2026-02/ingested/vitals-thailand.md` — Review first
  - `vault/2026-02/ingested/vitamine.md` — Review first
  - `vault/2026-02/ingested/wild-health.md` — Review first
  - `vault/2026-03/ingested/blood-testing-longevity-fundraises-2025-2026.md` — Review first
  - `vault/2026-03/ingested/competitor-founding-teams-analysis.md` — Review first
  - `vault/2026-03/ingested/superpower-email-gift-bogo-2026-02-28.md` — Review first
  - `vault/2026-03/ingested/superpower-email-what-should-you-test-2026-03-05.md` — Review first
  - `vault/2026-03/ingested/superpower-email-clinician-testimonial.md` — Review first
  - `strategy/decypher.md` — Rewrite

### Batch 23 — strategy pages + docs pages
- **Confidence:** Rewrite batch
- **Mode:** Rewrite in destination
- **Mix:** move-now 0, review 0, rewrite 10
- **Files:**
  - `strategy/fundraise.md` — Rewrite
  - `strategy/gtm.md` — Rewrite
  - `strategy/legal.md` — Rewrite
  - `strategy/market.md` — Rewrite
  - `strategy/operations.md` — Rewrite
  - `strategy/product.md` — Rewrite
  - `docs/bodycypher-micro-products-brainstorm-2026-03-20.md` — Rewrite
  - `docs/bodycypher-vision-deck-v1-draft.md` — Rewrite
  - `docs/panel-studio-prd.md` — Rewrite
  - `docs/prd-ocr-benchmark-tool.md` — Rewrite

### Batch 24 — missing + generated docs
- **Confidence:** Rewrite batch
- **Mode:** Rewrite in destination
- **Mix:** move-now 0, review 0, rewrite 6
- **Files:**
  - `vault/2026-03/generated/2026-03-23-kickoff-meeting-plan.md` — Rewrite
  - `vault/2026-03/generated/open-source-health-dashboard-research-brief.md` — Rewrite
  - `vault/2026-02/ingested/bodycypher_document_tracker_v5.md` — Rewrite
  - `vault/2026-02/ingested/product-brief-bodycypher-2026-01-28.md` — Rewrite
  - `vault/2026-02/ingested/product-brief.md` — Rewrite
  - `vault/2026-03/ingested/bodycypher-blood-panel-comparison.md` — Rewrite

## Skip list
- `CLAUDE.md` — Out of scope — vault operating doc
- `README.md` — Out of scope — vault operating doc
- `VAULT-GUIDE.md` — Out of scope — vault operating doc
- `docs/obsidian-bases-setup.md` — Out of scope — Obsidian setup doc
- `docs/superpowers/plans/2026-03-22-vault-entity-enrichment.md` — Out of scope — old agent planning doc
- `docs/superpowers/specs/2026-03-22-vault-entity-enrichment-design.md` — Out of scope — old agent planning doc
- `scripts/extract-entities.md` — Out of scope — tooling prompt
- `vault/2026-02/ingested/deep-research-biomarker-prompt-template.md` — Out of scope — template/prompt, not knowledge
- `vault/2026-02/ingested/mystery-shopping-template.md` — Out of scope — template/prompt, not knowledge
- `vault/2026-02/ingested/product-review-template.md` — Out of scope — template/prompt, not knowledge
- `vault/2026-02/ingested/prompt_single_company_v2.md` — Out of scope — template/prompt, not knowledge

## Recommended next step after review
1. Approve or edit the classification model.
2. Approve or reorder the first 3-5 batches.
3. Execute Batch 01 only after the current planning baseline is committed/pushed cleanly in `second-brain`.
4. Re-check the classification after every 3-5 merged PRs.

## One-line handover prompt
Read `projects/the-vault-pr-batch-plan.md` and `projects/the-vault-transfer-inventory.md`, then prepare the next approved 10-file migration PR from `the-vault` into `second-brain` without modifying the source vault.

## Timeline
- 2026-04-19 — Rebuilt the vault transfer plan from scratch as a direct knowledge-transfer plan: no archive-first model, no tooling/QMD migration, file-level confidence labels, and 24 ranked PR batches. [Source: William voice note + live repo inspection]
