# Personal Work Rollup Automation

> Executive summary: William wants Hermes to prepare morning and evening personal work rollups using Linear, Slack, GitHub, and local git, but the automation only becomes trustworthy once identity filtering is enforced across every source.

## State
- **Goal:** Prepare an 8 AM Bangkok planning draft and a 5 PM Bangkok wrap-up draft.
- **Inputs:** Assigned Linear issues, user-attributable GitHub activity, user-scoped Slack activity, and local repo history.
- **Current status:** Partially designed; cron/task-refresh plumbing exists, but cross-system identity resolution is still the main blocker.
- **Board home:** `ops/tasks.md` remains the canonical task board inside the brain.
- **Operating stance:** Draft first and review before blind posting until the attribution model is trustworthy.
- **Dependency:** This project depends on the concept in [Identity-Grounded Work Rollups](../concepts/identity-grounded-work-rollups.md).

## Open Threads
- Resolve William's canonical identity mapping across Slack, GitHub, and Linear.
- Decide whether the morning/evening outputs stay review-first or graduate to autonomous delivery once trusted.
- Decide whether cron outputs should land in a main channel, a thread, or a hybrid pattern.
- Reconcile stale or incomplete `ops/tasks.md` state against fresh external evidence without over-attributing work.
- Decide how local git evidence should be weighted when Slack, GitHub, or Linear signals are sparse.

## See Also
- [Second Brain](./second-brain.md)
- [Identity-Grounded Work Rollups](../concepts/identity-grounded-work-rollups.md)
- [Tasks](../ops/tasks.md)

---

## Timeline
- 2026-04-17 — William asked for two recurring automations: a morning rollup at 8:00 AM Bangkok time and an evening wrap-up at 5:00 PM, sourced from Linear, Slack, GitHub, and local git. [Source: session recall, 2026-04-17 14:40 Discord]
- 2026-04-17 — A morning standup drafting session exposed that repo-level recency was not enough; the system mixed in other people's work and surfaced identity filtering as the key prerequisite. [Source: session recall, 2026-04-17 07:50 Discord]
- 2026-04-17 — Existing morning and evening standup review cron jobs were confirmed, and thread-aware delivery was investigated as a likely next refinement. [Source: session recall, 2026-04-17 17:35 Discord]
