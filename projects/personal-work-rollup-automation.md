# Personal Work Rollup Automation

> Executive summary: William currently prefers automated todo-board refreshes plus manual standup drafting. The system can summarize work inputs, but it should not autonomously narrate personal progress until identity filtering and Slack auth are reliable.

## State
- **Goal:** Keep `ops/tasks.md` fresh as the canonical board and use it as the review surface for manual standup drafting.
- **Current cadence:** Automated board refreshes at 08:00 / 16:00 Bangkok using the morning refresh path; no autonomous evening standup post is currently trusted.
- **Inputs:** Assigned Linear issues, user-attributable GitHub activity, user-scoped Slack activity, and local git evidence.
- **Current status:** Board-refresh plumbing exists and is running, but cross-system identity resolution remains the main blocker to autonomous rollups.
- **Board home:** `ops/tasks.md` remains the canonical task board inside the brain.
- **Safe failure mode:** When attribution or auth is uncertain, refresh the board and ask for human review instead of generating a confident personal standup.
- **Dependency:** This project depends on the concept in [Identity-Grounded Work Rollups](../concepts/identity-grounded-work-rollups.md).

## Open Threads
- Resolve William's canonical identity mapping across Slack, GitHub, and Linear.
- Decide whether to restore a separate evening review once attribution and auth are stable.
- Decide whether board refreshes should continue as chat-assisted review or eventually graduate to autonomous delivery.
- Reconcile stale or incomplete `ops/tasks.md` state against fresh external evidence without over-attributing work.
- Harden non-interactive Slack access so cron refreshes do not fail on interactive OAuth prompts.

## See Also
- [Second Brain](./second-brain.md)
- [Identity-Grounded Work Rollups](../concepts/identity-grounded-work-rollups.md)
- [Tasks](../ops/tasks.md)

---

## Timeline
- 2026-04-17 — William asked for two recurring automations: a morning rollup at 8:00 AM Bangkok time and an evening wrap-up at 5:00 PM, sourced from Linear, Slack, GitHub, and local git. [Source: session recall, 2026-04-17 14:40 Discord]
- 2026-04-17 — A morning standup drafting session exposed that repo-level recency was not enough; the system mixed in other people's work and surfaced identity filtering as the key prerequisite. [Source: session recall, 2026-04-17 07:50 Discord]
- 2026-04-17 — Existing morning and evening standup review cron jobs were confirmed, and thread-aware delivery was investigated as a likely next refinement. [Source: session recall, 2026-04-17 17:35 Discord]
- 2026-04-18 — The scheduled morning review faulted when Slack MCP OAuth required browser authorization in a non-interactive cron context, reinforcing that Slack-backed automation was still fragile. [Source: session recall, 2026-04-18 08:07 Discord]
- 2026-04-18 — The workflow shifted to todo-board refreshes at 08:00 / 12:00 / 16:00 Bangkok, using the morning refresh engine and leaving standup drafting manual in chat. [Source: session recall, 2026-04-18 22:09 Discord]
- 2026-04-19 — William narrowed the board-refresh cadence to 08:00 / 16:00 Bangkok while keeping standup drafting manual. [Source: session recall, 2026-04-19 15:06 Discord]
