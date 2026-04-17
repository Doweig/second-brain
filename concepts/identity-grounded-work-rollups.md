# Identity-Grounded Work Rollups

> Executive summary: Personal standups and work rollups are only trustworthy when every source is filtered to the user's actual identity before synthesis. Repo-wide motion and channel-wide chatter are supporting evidence, not direct proof of personal work.

## State
- This is a core operating principle for William's standup and rollup workflows.
- The problem it solves is false attribution: drafts that summarize team or repo activity as if it were William's own work.
- Minimum identity checks implied by recent sessions:
  - Slack should resolve William's actual user identity and favor user-scoped retrieval.
  - GitHub should prefer authored PRs, commits, comments, and review activity over repo-wide recency.
  - Linear should prefer assigned or otherwise user-owned issues.
  - Local git should act as corroborating evidence, not the sole proof of authorship.
- This concept matters for both human-reviewed standups and future autonomous cron rollups.

## Open Threads
- Write down the canonical William identity mapping across Slack, GitHub, and Linear in one durable place.
- Decide what evidence threshold is sufficient when one system has weak attribution but another corroborates it.
- Encode the identity checks directly in automation so the workflow fails safe instead of hallucinating ownership.

## See Also
- [Personal Work Rollup Automation](../projects/personal-work-rollup-automation.md)
- [Second Brain](../projects/second-brain.md)
- [Second Brain Setup Reflection](../personal/2026-04-16-second-brain-setup-reflection.md)

---

## Timeline
- 2026-04-17 — A morning standup draft included repo activity the user said was not his own, which surfaced identity filtering as the core reliability problem. [Source: session recall, 2026-04-17 07:50 Discord]
- 2026-04-17 — A later workflow-design session made identity-grounded filtering the explicit prerequisite for automated 8 AM / 5 PM rollups across Slack, GitHub, Linear, and local git. [Source: session recall, 2026-04-17 14:40 Discord]
- 2026-04-17 — Cron/task-generation inspection reaffirmed that active Linear items can be listed mechanically, but trustworthy narration still needs a user-scoped lens before it becomes useful. [Source: session recall, 2026-04-17 17:35 Discord]
