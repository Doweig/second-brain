# The Vault Review-First Migration

> Executive summary: The active `the-vault` migration stance is now review-first inside `the-vault`, not immediate archive import into `second-brain`. The work starts by defining move / don't-move rules, then flagging documents in the source vault, and only afterward migrating approved material into GBrain-native pages.

## State
- **Status:** Current migration execution stance as of 2026-04-20.
- **Primary workspace:** `~/orba-health/the-vault` for the rules / inventory / flagging phases.
- **Stage model:** 1) decide migration rules, 2) flag documents in `the-vault` as move / don't move, 3) migrate approved material into `second-brain` later.
- **Second-brain role:** Remains the eventual durable destination, not the current planning home for the review phase.
- **Historical context:** The earlier archive-first pages in this repo remain useful as reference, but they are no longer the default next step.
- **Board signal:** The old archive-batch / canonical-overlay tasks were removed from `ops/tasks.md`, which means the current task board is no longer treating the archive-first plan as active execution. [Source: local repo inspection, 2026-04-21]

## Open Threads
- Decide the exact root-level planning folder name and documentation shape inside `the-vault`.
- Turn the review-first rules into a full move / don't-move inventory without recreating duplicate company knowledge already present in `knowledge`.
- Decide how approved items will map back into GBrain-native homes once the vault review is done.
- Decide whether any part of the older archive-first material in this repo should remain as fallback reference only or be retired more explicitly.

## See Also
- [Second Brain](./second-brain.md)
- [The Vault Salvage Plan](./the-vault-salvage-plan.md)
- [The Vault PR Batch Migration Plan](./the-vault-pr-batch-plan.md)
- [Tasks](../ops/tasks.md)
- [the-vault source staging](../sources/the-vault/README.md)

---

## Timeline
- 2026-04-19 — `second-brain` recorded an archive-first / canonical-overlay migration plan for `the-vault` and associated PR batching. [Source: local repo history + project pages, 2026-04-19]
- 2026-04-20 — William changed the migration direction: stop centering the work in `second-brain`, create planning docs inside `the-vault`, define rules first, flag move / don't-move documents there, and migrate only after that review. [Source: session recall, 2026-04-20 05:45 Discord]
- 2026-04-20 — The `second-brain` task board removed the archive-batch / canonical-overlay items, which reinforced that the archive-first plan was no longer the active execution path. [Source: session recall, 2026-04-20 09:11 Discord; corroborated by local repo inspection, 2026-04-21]