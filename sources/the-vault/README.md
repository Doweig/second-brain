# the-vault source staging

> Raw source material preserved from `~/orba-health/the-vault` during the current archive-first migration into `second-brain`.

## State
- This directory is for provenance, attachments, and preserved originals — not canonical pages. [Source: local repo design decision, 2026-04-19]
- The current plan is to keep preserved markdown under `archive/the-vault/` while non-markdown and raw supporting artifacts land under `sources/the-vault/full-import/` or later topic-specific subtrees here. [Source: migration planning pages, 2026-04-19]
- The source vault remains the untouched system of record during migration. [Source: migration rule, 2026-04-19]

## Rules
- Migration is additive only.
- Markdown originals belong in `archive/the-vault/`, not in this directory.
- Preserve non-markdown originals under stable subtrees that mirror the source path (for example `full-import/vault/2026-03/raw/...`).
- Canonical knowledge belongs elsewhere in the brain according to `RESOLVER.md`.
- If a file already lives canonically in `knowledge`, prefer a link or summary over duplication.

## See Also
- [The Vault PR Batch Migration Plan](../../projects/the-vault-pr-batch-plan.md)
- [The Vault Salvage Plan](../../projects/the-vault-salvage-plan.md)
- [Resolver](../../RESOLVER.md)

---

## Timeline
- 2026-04-19 — Created a dedicated source-staging area for `the-vault` salvage batches so originals can be preserved without becoming canonical brain pages. [Source: William approval + local repo update, 2026-04-19]
- 2026-04-19 — The migration direction shifted to archive-first import, with raw supporting artifacts planned under `sources/the-vault/full-import/` while markdown history lands under `archive/the-vault/`. [Source: William voice note + local repo planning pages, 2026-04-19]
