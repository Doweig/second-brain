# the-vault source staging

> Historical/archive-first staging note for raw `the-vault` material. This directory concept remains useful if archive import resumes, but it is not the current active migration workflow.

## State
- This directory is for provenance, attachments, and preserved originals — not canonical pages. [Source: local repo design decision, 2026-04-19]
- This staging layout belongs to the older archive-first plan and is currently reference-only while the active migration workflow has moved back to review-first planning inside `the-vault`. [Source: session recall, 2026-04-20 05:45 Discord; corroborated by local repo inspection, 2026-04-21]
- If archive import resumes, preserved markdown should live under `archive/the-vault/` while non-markdown and raw supporting artifacts land under `sources/the-vault/full-import/` or later topic-specific subtrees here. [Source: migration planning pages, 2026-04-19]

## Rules
- Migration is additive only.
- Markdown originals belong in `archive/the-vault/`, not in this directory.
- Preserve non-markdown originals under stable subtrees that mirror the source path (for example `full-import/vault/2026-03/raw/...`).
- Canonical knowledge belongs elsewhere in the brain according to `RESOLVER.md`.
- If a file already lives canonically in `knowledge`, prefer a link or summary over duplication.

## See Also
- [The Vault Review-First Migration](../../projects/the-vault-review-first-migration.md)
- [The Vault PR Batch Migration Plan](../../projects/the-vault-pr-batch-plan.md)
- [The Vault Salvage Plan](../../projects/the-vault-salvage-plan.md)
- [Resolver](../../RESOLVER.md)

---

## Timeline
- 2026-04-19 — Created a dedicated source-staging area for `the-vault` salvage batches so originals can be preserved without becoming canonical brain pages. [Source: William approval + local repo update, 2026-04-19]
- 2026-04-19 — The migration direction shifted to archive-first import, with raw supporting artifacts planned under `sources/the-vault/full-import/` while markdown history lands under `archive/the-vault/`. [Source: William voice note + local repo planning pages, 2026-04-19]
- 2026-04-20 — The active migration stance moved back to review-first planning inside `the-vault`, so this staging area is currently preserved as reference rather than active work. [Source: session recall, 2026-04-20 05:45 Discord]
