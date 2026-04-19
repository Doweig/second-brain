# The Vault PR Batch Migration Plan

> **For Hermes:** Use the `github-pr-workflow` skill. Execute one batch at a time. Never mix batches. Keep each migration PR to 5-10 moved vault files.

**Goal:** Move `the-vault` into `second-brain` through small, reviewable PRs so William can approve, reject, or trim specific files before merge.

**Architecture:** Archive-first import. Each PR copies 5-10 markdown files from `~/orba-health/the-vault` into `~/orba-health/second-brain/archive/the-vault/<same-relative-path>` unchanged, preserving path and historical date context. Canonical GBrain-native rewrites happen only after the archive batch is merged.

**Tech Stack:** git, GitHub PRs, `gh`, markdown, GBrain sync/extract.

---

## State
- `the-vault` currently contains 247 markdown files: 183 under `vault/`, 28 under `companies/`, 18 under `people/`, 7 under `strategy/`, and 7 under `docs/`. [Source: local repo inspection, 2026-04-19]
- `second-brain` remote is `git@github.com:Doweig/second-brain.git`. [Source: `git remote -v`, 2026-04-19]
- `second-brain` `main` is currently ahead of `origin/main` by 2 commits and the repo is dirty with migration-planning files, so batch branches should not start until the planning baseline is landed or otherwise isolated. [Source: `git branch -vv` and `git status --short`, 2026-04-19]
- William wants 5-10 files per PR so he can review each chunk pre-merge and request removals or changes file-by-file. [Source: William, voice note, 2026-04-19]

## Non-Negotiable Rules
- Source vault is read-only. Never move, edit, or delete files inside `~/orba-health/the-vault`.
- Each migration PR copies **5-10 markdown files** only.
- Destination for archive PRs is always `archive/the-vault/<same-relative-path>`.
- Preserve filenames, dates, frontmatter, and old structure in archive PRs.
- Do **not** rewrite into canonical `people/`, `companies/`, `projects/`, `org/`, etc. during archive PRs.
- Do **not** include `CLAUDE.md`, `README.md`, `VAULT-GUIDE.md`, `.mcp.json`, or `docs/superpowers/...` in archive PRs.
- Keep each PR topically coherent so William can review it as one idea-cluster.
- If William rejects specific files in review, remove those files from the branch and push an update; do not argue with the review.
- After each merged PR, run GBrain maintenance against `second-brain` so the archive layer becomes queryable incrementally.

## Prep Step — land a clean baseline first
This is **not** a migration batch PR.

### Step 1: Clean the repo state
Either:
- open one prep PR for the current planning files, or
- commit/push them to the intended base branch before starting batch PRs.

Current dirty files seen during planning:
- `ops/tasks.md`
- `projects/second-brain.md`
- `projects/the-vault-salvage-plan.md`
- `sources/the-vault/`

### Step 2: Start from clean `main`

Run:
```bash
cd ~/orba-health/second-brain
git checkout main
git pull origin main
git status --short
```

Expected: no uncommitted changes before creating the first batch branch.

## PR Naming Convention
- Branch: `vault-batch-XX-short-slug`
- PR title: `the-vault batch XX: short slug`
- Commit message: `archive: import the-vault batch XX short slug`

Examples:
- `vault-batch-01-founder-core`
- `the-vault batch 01: founder core`
- `archive: import the-vault batch 01 founder core`

## Per-PR Execution Template

### Step 1: Create a branch
```bash
cd ~/orba-health/second-brain
git checkout main
git pull origin main
git checkout -b vault-batch-XX-short-slug
```

### Step 2: Copy the batch files unchanged
Example shape:
```bash
mkdir -p archive/the-vault/people archive/the-vault/companies archive/the-vault/strategy archive/the-vault/docs
cp ~/orba-health/the-vault/people/example.md ~/orba-health/second-brain/archive/the-vault/people/
```

For `vault/...` files, preserve the full nested path:
```bash
mkdir -p archive/the-vault/vault/2026-03/ingested
cp ~/orba-health/the-vault/vault/2026-03/ingested/example.md ~/orba-health/second-brain/archive/the-vault/vault/2026-03/ingested/
```

### Step 3: Commit and push
```bash
git add archive/the-vault
git commit -m "archive: import the-vault batch XX short slug"
git push -u origin HEAD
```

### Step 4: Open the PR
```bash
gh pr create \
  --title "the-vault batch XX: short slug" \
  --body "## Summary
- Imports the next review batch from the-vault into archive/the-vault/
- Preserves original filenames, paths, and historical dates
- No canonical rewrites in this PR

## Files
- file 1
- file 2
- file 3

## Review ask for William
- Mark any file to drop from this batch
- Mark any file to defer to a later PR
- Approve when the batch looks right" 
```

### Step 5: After merge, refresh the brain
```bash
git checkout main
git pull origin main
gbrain sync --repo ~/orba-health/second-brain --no-pull --no-embed
gbrain extract links ~/orba-health/second-brain
gbrain extract timeline ~/orba-health/second-brain
```

## Batch Sequence

### PR 01 — founder core
**Branch:** `vault-batch-01-founder-core`

**Files (7):**
- `companies/bodycypher.md`
- `people/william-guillaume.md`
- `people/art-chawapon-kidhirunkul.md`
- `people/art-tanapote.md`
- `people/anton.md`
- `strategy/product.md`
- `strategy/market.md`

### PR 02 — founder network A
**Branch:** `vault-batch-02-founder-network-a`

**Files (7):**
- `people/dan-aspire.md`
- `people/david-berghaeuser.md`
- `people/gift.md`
- `people/kojchakorn.md`
- `people/nick-warot.md`
- `people/niels.md`
- `people/swit.md`

### PR 03 — founder network B
**Branch:** `vault-batch-03-founder-network-b`

**Files (7):**
- `people/andrew-huberman.md`
- `people/jiri-dvorak.md`
- `people/jonathan-swerdlin.md`
- `people/mark-hyman.md`
- `people/peter-attia.md`
- `people/tanupol-virunhagarun.md`
- `people/zeth.md`

### PR 04 — strategy and vision
**Branch:** `vault-batch-04-strategy-and-vision`

**Files (7):**
- `strategy/decypher.md`
- `strategy/gtm.md`
- `strategy/fundraise.md`
- `strategy/operations.md`
- `strategy/legal.md`
- `docs/bodycypher-vision-deck-v1-draft.md`
- `docs/bodycypher-micro-products-brainstorm-2026-03-20.md`

### PR 05 — product and tool docs
**Branch:** `vault-batch-05-product-and-tool-docs`

**Files (5):**
- `docs/panel-studio-prd.md`
- `docs/prd-ocr-benchmark-tool.md`
- `docs/obsidian-bases-setup.md`
- `vault/2026-03/generated/open-source-health-dashboard-research-brief.md`
- `vault/2026-03/generated/2026-03-23-kickoff-meeting-plan.md`

### PR 06 — company cluster A
**Branch:** `vault-batch-06-company-cluster-a`

**Files (7):**
- `companies/acclime-thailand.md`
- `companies/aspire.md`
- `companies/aspire-coaching-physio.md`
- `companies/bnh-hospital.md`
- `companies/ipc-international.md`
- `companies/prewell-clinic.md`
- `companies/rabbitcare.md`

### PR 07 — company cluster B
**Branch:** `vault-batch-07-company-cluster-b`

**Files (7):**
- `companies/doctor-anywhere.md`
- `companies/function-health.md`
- `companies/insidetracker.md`
- `companies/mito-health.md`
- `companies/n-health.md`
- `companies/nhealth.md`
- `companies/vitalab.md`

### PR 08 — company cluster C
**Branch:** `vault-batch-08-company-cluster-c`

**Files (7):**
- `companies/vitalab-thailand.md`
- `companies/ezra.md`
- `companies/grail.md`
- `companies/hum-clinic.md`
- `companies/mainscape.md`
- `companies/measureup.md`
- `companies/novi-health.md`

### PR 09 — company cluster D
**Branch:** `vault-batch-09-company-cluster-d`

**Files (6):**
- `companies/quest-diagnostics.md`
- `companies/sanwiz-lab.md`
- `companies/siphox-health.md`
- `companies/viatell.md`
- `companies/viome.md`
- `companies/vitallife-by-bumrungrad.md`

### PR 10 — legal archive A
**Branch:** `vault-batch-10-legal-archive-a`

**Files (7):**
- `vault/2026-02/ingested/Corporate structuring playbook for a SEA healthtech expansion.md`
- `vault/2026-02/ingested/Launching a prototype with minimal legal structure.md`
- `vault/2026-02/ingested/Meeting with Tanapote on Jan 30th 2026.md`
- `vault/2026-02/ingested/Thailand regulatory and legal roadmap for a health tech dual-entity startup.md`
- `vault/2026-03/ingested/legal-status-2026-03-02.md`
- `vault/2026-03/ingested/bodycypher-legal-master-braindump-2026-03-10.md`
- `vault/2026-03/ingested/bodycypher-legal-master-braindump-addendum-2026-03-10.md`

### PR 11 — legal archive B
**Branch:** `vault-batch-11-legal-archive-b`

**Files (7):**
- `vault/2026-03/ingested/bodycypher-legal-questions-for-counsel-2026-03-09.md`
- `vault/2026-03/ingested/email-tanapote-incorporation-questions-2026-03-18.md`
- `vault/2026-03/ingested/foreign-owned-healthtech-thailand-legal-viability.md`
- `vault/2026-03/ingested/founders-cap-table-gentlemans-agreement-2026-03-17.md`
- `vault/2026-03/ingested/legal-opinion-ipc-tanapote-2026-03-09.md`
- `vault/2026-03/ingested/moph-telemedicine-standards-notification-2021.md`
- `vault/2026-03/ingested/thai-fda-samd-ai-regulatory-guide-oct-2024.md`

### PR 12 — meeting core A
**Branch:** `vault-batch-12-meeting-core-a`

**Files (8):**
- `vault/2026-02/ingested/2026-02-20 Meeting with Tanapote Lawyer.md`
- `vault/2026-02/ingested/2026-02-23 Meeting with Acclime.md`
- `vault/2026-02/ingested/2026-02-23 Meeting with Swit.md`
- `vault/2026-02/ingested/2026-02-24 Meeting with Dr. C.md`
- `vault/2026-03/ingested/2026-03-03-dr-c-meeting.md`
- `vault/2026-03/ingested/2026-03-04-meeting-with-anton.md`
- `vault/2026-03/ingested/2026-03-04-meeting-with-swit.md`
- `vault/2026-03/ingested/meeting-tanapote-ipc-2026-03-11.md`

### PR 13 — meeting core B
**Branch:** `vault-batch-13-meeting-core-b`

**Files (7):**
- `vault/2026-03/ingested/meeting-dr-c-2026-03-10.md`
- `vault/2026-03/ingested/voice-memo-anton-equity-shares-2026-03-11.md`
- `vault/2026-03/ingested/voice-memo-war-council-review-2026-03-16.md`
- `vault/2026-03/ingested/voice-memo-legal-strategy-singapore-incorporation-2026-03-27.md`
- `vault/2026-03/ingested/2026-03-06-weekly-reflection.md`
- `vault/2026-03/ingested/dr-c-relationship-status-2026-03-02.md`
- `vault/2026-03/ingested/david-berghaeuser-profile.md`

### PR 14 — customer research A
**Branch:** `vault-batch-14-customer-research-a`

**Files (6):**
- `vault/2026-02/ingested/Bangkok Health Clinic Review Analysis.md`
- `vault/2026-02/ingested/Thai Consumer Health Checkup Research.md`
- `vault/2026-02/ingested/What users actually think about blood test reports and AI health plans.md`
- `vault/2026-02/ingested/blood-testing-biohacking-communities.md`
- `vault/2026-02/ingested/bodycypher_early_access_survey-v2.md`
- `vault/2026-02/ingested/cr4-target-customer-profiles-draft.md`

### PR 15 — customer research B
**Branch:** `vault-batch-15-customer-research-b`

**Files (5):**
- `vault/2026-02/ingested/customer-sentiment-synthesis.md`
- `vault/2026-02/ingested/customer-sentiment-wellness-checkups-bangkok.md`
- `vault/2026-02/ingested/gemini-youtube.md`
- `vault/2026-03/ingested/ifm-intake-questionnaire.md`
- `vault/2026-03/ingested/survey-export-2026-03-02.md`

### PR 16 — pitch and growth
**Branch:** `vault-batch-16-pitch-and-growth`

**Files (7):**
- `vault/2026-02/ingested/bodycypher-pitch-deck-v2.md`
- `vault/2026-02/ingested/pitch-deck.md`
- `vault/2026-03/ingested/bodycypher-story-deck-v3.md`
- `vault/2026-02/ingested/customer-success-funnel.md`
- `vault/2026-02/ingested/sales-funnel.md`
- `vault/2026-02/ingested/user-lifecycle.md`
- `vault/2026-03/ingested/bodycypher-branding-guidelines.md`

## Long-tail rule after PR 16
After the first 16 PRs, keep going with the same 5-10-file pattern:
1. Remaining `meeting-notes` with founder / legal / relationship context
2. `product-research` in topical chunks of 5-8 files
3. `market-research` last, because it has the highest overlap with `knowledge`

When building long-tail batches:
- choose one `(month, type)` bucket at a time
- sort oldest-to-newest inside the bucket
- keep one topic per PR
- if a candidate file clearly belongs only in `knowledge`, skip it and note the skip in the PR body

## Raw attachments rule
Do **not** bulk-import PDFs/images/screenshots as part of these markdown archive PRs.

Instead:
- move markdown pages first
- only import raw attachments later for accepted legal / meeting / founder-history batches
- keep those attachment PRs separate under `sources/the-vault/full-import/`

## Review protocol
William should be able to do one of four things on each PR:
- approve the whole batch
- ask to remove one or more files from the batch
- ask to rename / split the batch
- defer specific files to a later PR

The executing agent should update the branch accordingly, push again, and only merge after explicit approval.

## Transition to canonical overlay PRs
Do **not** start canonical overlay rewrites until at least PR 01-05 are merged.

Once there is enough historical base, create separate PRs that promote selected archived pages into living GBrain-native pages such as:
- `companies/bodycypher.md`
- `people/william-guillaume.md`
- `projects/bodycypher-product-strategy.md`
- `org/bodycypher-market-positioning.md`
- `writing/bodycypher-vision.md`

Those overlay PRs should be separate from archive-import PRs.

## Open Threads
- Land the current planning baseline on `main` before opening `vault-batch-01-founder-core`.
- Track any William-requested trims or deferrals inside the first review batch rather than widening batch scope.
- Decide when to start separate raw-attachment PRs under `sources/the-vault/full-import/`.

## See Also
- [Second Brain](./second-brain.md)
- [The Vault Salvage Plan](./the-vault-salvage-plan.md)
- [the-vault source staging](../sources/the-vault/README.md)
- [the-vault PR batch handover](../prompts/the-vault-pr-batch-handover.md)

## Files to update alongside this plan
- `projects/the-vault-salvage-plan.md` — strategy-level migration stance
- `projects/second-brain.md` — open thread / status
- `ops/tasks.md` — only the next actionable migration task, not the full backlog

## One-line handover prompt
Follow `projects/the-vault-pr-batch-plan.md` and open the next 5-10-file `the-vault` archive PR into `second-brain`, preserving original paths/dates and leaving the source vault untouched.

## Timeline
- 2026-04-19 — William requested a PR-driven migration plan with 5-10 files per PR so he can review and reject specific files pre-merge. [Source: William, voice note, 2026-04-19]
- 2026-04-19 — The first 16 archive batches were defined from live inspection of `the-vault`, with raw attachments deferred to later companion PRs. [Source: local repo inspection, 2026-04-19]
