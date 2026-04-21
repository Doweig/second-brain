---
type: archive-pointer
date: 2026-04-20
---

# Vault migration — 2026-04-20

On 2026-04-20, residual content was migrated from the old BodyCypher-era vault into this workspace.

## Source

The old vault lives on the remote host and via SSHFS locally:

- **Remote:** `doweig@bc-u24.tail34269b.ts.net:/home/doweig/the-vault`
- **Local SSHFS mount:** `/Users/doweig/the-vault` (when mounted)
- **Alternative local path used during this migration:** `/Users/doweig/dev/ai-agents/the-vault`

The vault self-described as *"Documentation vault for BodyCypher, a longevity and wellness checkup startup in Bangkok."* It is append-only and treated as an immutable archive. **No files were deleted or modified there during this migration** — everything was copied.

## Migration plan

The full plan (decisions per folder / per file, skip list, destination mapping) is at:

`/Users/doweig/.claude/plans/the-vault-my-old-personal-cozy-spring.md`

## What moved

- **people/** — 15 CRM stubs copied, 3 new stubs created from Notion exports (antonio, marc-antoine-olive, theo-j). Richer profiles for Dr. C and David Berghäuser merged from vault ingested docs. Public-figure stubs (Peter Attia, Andrew Huberman, Mark Hyman) intentionally skipped.
- **companies/** — 28 company stubs copied, including a rewritten `bodycypher.md` annotated with the solo-project → Orba Health history.
- **meetings/** — ~27 meeting / voice-memo files with Notion hash suffixes stripped and filenames normalized.
- **concepts/** — 119 research files across `biomarkers/`, `competitors/`, `mystery-shopping/`, `market/`, `customer-research/`, `thailand-healthtech-regulatory/`, `bodycypher-history/`. Duplicates content already graduated to the `knowledge/` company vault; preserved here as a complete snapshot of the author's thinking.
- **sources/** — 14 compass-artifact web-scrapes under `sources/compass-artifacts/`, plus 6 Superpower email captures at the root.
- **prompts/** — 2 reusable prompt templates (biomarker deep-research, single-company research).
- **personal/health/lab-results/** — 4 personal PDF lab results (Guillaume William). JPEG/BloodGPT interpretations intentionally not migrated.

## What was skipped

See §S of the plan file. Primary skip categories:

- Finalized BodyCypher strategy: `strategy/` (7 docs), vision deck, pitch deck v2, landing page, branding guidelines, early pitch/product-brief drafts.
- Public-figure people stubs: peter-attia, andrew-huberman, mark-hyman.
- Vault infrastructure: `scripts/`, superpowers specs, obsidian-bases-setup, root meta (README, CLAUDE, VAULT-GUIDE, .mcp.json).
- Deleted-on-request PRDs: panel-studio-prd, prd-ocr-benchmark-tool, bodycypher-micro-products-brainstorm.
- Unused templates: product-review-template, mystery-shopping-template, gemini-youtube.
- Raw competitor-marketing PDFs/images in `vault/*/raw/` — except the 4 personal Guillaume-William-labeled PDFs.

## After merging this branch

- `gbrain import /Users/doweig/dev/ai-agents/second-brain/ --no-embed && gbrain embed --stale` to re-index the new content for search.
- Consider closing the older `vault-batch-01-people-pages` remote branch — it was a pre-plan attempt with a different scope (included Huberman, which the current plan skips).
