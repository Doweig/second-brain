# The Vault Salvage Plan

> Executive summary: Historical reference page for the 2026-04-19 **bulk historical import + canonical overlay** plan. This is no longer the active execution path after the later shift to [The Vault Review-First Migration](./the-vault-review-first-migration.md), but it remains useful as a fallback/reference strategy.

## State
- **Current status:** Preserved as a historical/reference plan, not the active next step after the 2026-04-20 shift back to vault-first review. [Source: session recall, 2026-04-20 05:45 Discord; corroborated by local repo inspection, 2026-04-21]
- `the-vault` currently contains 247 markdown files: 183 under `vault/`, 28 under `companies/`, 18 under `people/`, 7 under `strategy/`, and 7 under `docs/`. [Source: local repo inspection, 2026-04-19]
- `second-brain` currently contains 31 markdown files and is still mostly scaffold plus a few operating pages. [Source: local repo inspection, 2026-04-19]
- `knowledge` currently contains 241 markdown files, and at least 31 exact filename stems overlap with `the-vault`, so bulk import would create obvious duplication. [Source: local repo inspection, 2026-04-19]
- The raw ingest is mostly not canonical-ready: `vault/` is dominated by 80 market-research files, 36 product-research files, 30 meeting-notes files, and 14 legal-research files; 176 of the 183 ingested markdown files are still marked `raw`. [Source: local repo inspection, 2026-04-19]
- William's updated preference is to get the whole vault into `second-brain` first as a historical base layer, then improve structure and retrieval on top of that. [Source: William, voice note, 2026-04-19]

## Migration Rules
- Keep the source vault untouched. Migration is additive only.
- Bulk-import the markdown vault as a **historical layer**, not as already-clean canonical truth.
- Preserve original relative paths and dates wherever possible so old context stays queryable.
- Put preserved markdown under `archive/the-vault/` and preserved supporting artifacts under `sources/the-vault/`.
- Treat `people/`, `companies/`, `projects/`, `org/`, `ideas/`, and other resolver-native directories as the **canonical overlay layer** that will be improved over time.
- Duplicates versus `knowledge` are acceptable in the archive layer; avoid duplicate promotion into the canonical overlay unless the page carries private founder / relationship / historical context that belongs in the personal brain.
- Do not rely on recency happening magically: preserve dates in frontmatter/timeline so temporal queries like `latest`, `recent`, `history`, and `when` can resolve correctly.

## Phase 1 — Full Historical Import
- Import the whole markdown vault into `second-brain` under `archive/the-vault/`, preserving the old top-level structure (`people/`, `companies/`, `strategy/`, `docs/`, `vault/YYYY-MM/...`).
- Preserve non-markdown artifacts from `vault/**/raw/` under `sources/the-vault/full-import/` with the same relative paths.
- Preserve original dates from frontmatter / filenames instead of restamping pages to today.
- Accept that this layer will contain duplication, old QMD-era structure, and rough notes; that is fine because its job is recall, not cleanliness.

## Phase 2 — Canonical Overlay Batch 01
1. `archive/the-vault/companies/bodycypher.md` -> `companies/bodycypher.md`
2. `archive/the-vault/people/william-guillaume.md` -> `people/william-guillaume.md`
3. `archive/the-vault/strategy/product.md` -> `projects/bodycypher-product-strategy.md`
4. `archive/the-vault/strategy/market.md` -> `org/bodycypher-market-positioning.md`
5. `archive/the-vault/docs/bodycypher-vision-deck-v1-draft.md` -> `writing/bodycypher-vision.md`
6. `archive/the-vault/docs/bodycypher-micro-products-brainstorm-2026-03-20.md` -> `ideas/bodycypher-micro-product-ideas.md`
- This batch proves the overlay pattern after the historical layer exists. [Source: local repo inspection, 2026-04-19]

## Phase 3 — Canonical Overlay Expansion
- `archive/the-vault/strategy/gtm.md` -> `org/bodycypher-go-to-market.md`
- `archive/the-vault/strategy/fundraise.md` -> `deals/bodycypher-fundraise-strategy.md`
- `archive/the-vault/strategy/operations.md` -> `org/bodycypher-operations.md`
- `archive/the-vault/strategy/legal.md` -> `org/bodycypher-legal-structure.md` plus supporting artifacts under `sources/the-vault/legal/`
- `archive/the-vault/strategy/decypher.md` -> `projects/decypher.md`
- `archive/the-vault/docs/panel-studio-prd.md` -> `projects/panel-configurator.md`
- `archive/the-vault/docs/prd-ocr-benchmark-tool.md` -> `projects/ocr-benchmark-tool.md`
- Normalize the 18 archived `people/` pages into canonical `people/` pages over time; these are unique by exact filename stem versus `knowledge`. [Source: local repo inspection, 2026-04-19]
- Review the 28 archived `companies/` pages in two buckets:
  - promote when they matter to founder history, relationships, or institutional memory (`bodycypher`, `acclime-thailand`, `aspire`, `aspire-coaching-physio`, `ipc-international`, `prewell-clinic`)
  - leave archival-only when `knowledge` already holds the canonical operating page (`doctor-anywhere`, `function-health`, `mito-health`, `nhealth`, `siphox-health`, `vitalab`) [Source: local repo inspection, 2026-04-19]
- Manually review near-duplicates where slugs differ (for example `insidetracker` vs `inside-tracker`) before promoting.

## Phase 4 — Retrieval / Triage Rules
- Use the archive layer for broad recall and history.
- Use the canonical overlay for the current answer when there is a conflict.
- When asking temporal questions (`latest`, `recent`, `history`, `when`), rely on preserved dates/timeline entries rather than assuming the DB will automatically infer recency.
- Leave company market research archival-only when `knowledge` already holds the canonical version.

## Explicit Non-Canonical List
- `CLAUDE.md`, `README.md`, `VAULT-GUIDE.md`, `.mcp.json`
- `docs/superpowers/...` implementation plans and specs for old vault tooling
- old QMD / Obsidian workflow assumptions as canonical architecture
- duplicated market-research pages that are already better maintained in `knowledge`
- these can still exist in the archive layer; they just should not become the canonical overlay by default

## Execution Loop
1. Bulk-copy markdown from `~/orba-health/the-vault` into `~/orba-health/second-brain/archive/the-vault/`, preserving relative paths.
2. Bulk-copy raw attachments from `vault/**/raw/` into `~/orba-health/second-brain/sources/the-vault/full-import/`, preserving relative paths.
3. Run:

```bash
gbrain sync --repo ~/orba-health/second-brain --no-pull --no-embed
gbrain extract links ~/orba-health/second-brain
gbrain extract timeline ~/orba-health/second-brain
gbrain features --json
```

4. Spot-check broad historical retrieval across archived pages.
5. Then execute Canonical Overlay Batch 01.
6. Continue promoting only the pages that deserve a living canonical home.

## Open Threads
- Whether raw supporting artifacts should stay in one `sources/the-vault/full-import/` tree or be split into topic-specific subtrees after the first archive batches land.
- Whether `strategy/legal.md` should become one org page or be split into legal structure + founder allocation + clinic path pages.
- Whether `companies/bodycypher.md` or `projects/bodycypher-history.md` should be the main anchor for the BodyCypher era.
- How aggressively to convert old `[[wikilinks]]` into new canonical slugs versus keeping them only in preserved source copies.
- Whether `docs/obsidian-bases-setup.md` is worth preserving at all beyond raw provenance.
- Whether cross-repo retrieval against `knowledge` should stay a Hermes-layer workflow instead of trying to co-load both repos into one shared GBrain namespace.

## See Also
- [Second Brain](./second-brain.md)
- [The Vault Review-First Migration](./the-vault-review-first-migration.md)
- [The Vault PR Batch Migration Plan](./the-vault-pr-batch-plan.md)
- [the-vault source staging](../sources/the-vault/README.md)
- [Resolver](../RESOLVER.md)
- [Schema](../schema.md)
- [Tasks](../ops/tasks.md)

---

## Timeline
- 2026-04-19 — Inspected `the-vault`, `knowledge`, and `second-brain`; confirmed a 247 / 241 / 31 markdown split, strong company-KB overlap, and a raw-heavy source vault. [Source: local repo inspection, 2026-04-19]
- 2026-04-19 — Initial recommendation favored selective promotion first because of strong overlap with `knowledge` and a raw-heavy source vault. [Source: local repo inspection, 2026-04-19]
- 2026-04-19 — William updated the preferred strategy to bulk historical import first, then layer canonical rewrites on top, with source dates preserved for temporal retrieval. [Source: William, voice note, 2026-04-19]
- 2026-04-20 — William later changed the active migration stance again, moving execution back to a review-first workflow inside `the-vault`; this page remains as the preserved archive-first alternative/reference. [Source: session recall, 2026-04-20 05:45 Discord]
