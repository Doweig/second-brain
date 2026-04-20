# the-vault PR batch handover

> Historical handoff prompt for the archive-first `the-vault` PR batch workflow.

## State
- Use this prompt only if the archive-first plan in `projects/the-vault-pr-batch-plan.md` is reactivated.
- The active migration stance later shifted to [The Vault Review-First Migration](../projects/the-vault-review-first-migration.md), so this prompt is now preserved as reference rather than the default handoff. [Source: session recall, 2026-04-20 05:45 Discord]
- The prompt assumes the source vault stays read-only and that each PR copies only 5-10 markdown files.
- Detailed file selection, naming, and review rules live in the migration-plan page rather than here.

## Prompt
```text
Follow `projects/the-vault-pr-batch-plan.md` and open the next 5-10-file `the-vault` archive PR into `second-brain`, preserving original paths/dates and leaving the source vault untouched.
```

## See Also
- [The Vault Review-First Migration](../projects/the-vault-review-first-migration.md)
- [The Vault PR Batch Migration Plan](../projects/the-vault-pr-batch-plan.md)
- [The Vault Salvage Plan](../projects/the-vault-salvage-plan.md)

---

## Timeline
- 2026-04-19 — Added as the minimal reusable handoff prompt for archive-batch execution. [Source: local repo update, 2026-04-19]
- 2026-04-20 — Preserved as a historical prompt after the active migration stance shifted back to review-first planning inside `the-vault`. [Source: session recall, 2026-04-20 05:45 Discord]
