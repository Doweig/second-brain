# the-vault PR batch handover

> Reusable handoff prompt for opening the next reviewable `the-vault` archive PR into `second-brain`.

## State
- Use this prompt when a future agent needs to execute the next migration batch from `projects/the-vault-pr-batch-plan.md`.
- The prompt assumes the source vault stays read-only and that each PR copies only 5-10 markdown files.
- Detailed file selection, naming, and review rules live in the migration-plan page rather than here.

## Prompt
```text
Follow `projects/the-vault-pr-batch-plan.md` and open the next 5-10-file `the-vault` archive PR into `second-brain`, preserving original paths/dates and leaving the source vault untouched.
```

## See Also
- [The Vault PR Batch Migration Plan](../projects/the-vault-pr-batch-plan.md)
- [The Vault Salvage Plan](../projects/the-vault-salvage-plan.md)

---

## Timeline
- 2026-04-19 — Added as the minimal reusable handoff prompt for archive-batch execution. [Source: local repo update, 2026-04-19]
