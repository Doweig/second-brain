# Second Brain

> Personal knowledge system being rebooted as a clean GBrain-powered repo that unifies durable knowledge, task management, and conversational idea capture.

## State
- **Status:** Active setup and early operation
- **Stack:** Markdown repo + GBrain local brain + Hermes orchestration
- **Role split:** GBrain is the durable personal brain / indexing layer; Hermes is the conversational orchestration layer.
- **Primary goal:** Combine the knowledge density of the old vault with the operational sharpness of task-vault
- **Current repo:** `~/orba-health/second-brain`
- **Preferred chat surface:** Discord-first, with Telegram optional as a lighter side entry later.
- **Slack stance:** The desired end state is a private analyst / user-auth workflow, not a visible app-style bot as the default surface.
- **Voice capture:** Voice notes and spoken reflections are high-value inputs; TTS is deprioritized for now because recent experiments were frustrating.
- **Current daily ops rhythm:** `ops/tasks.md` is refreshed as a todo board at 08:00 / 12:00 / 16:00 Bangkok, while standup drafting stays manual in chat until attribution and Slack auth are trustworthy.
- **Embeddings:** Working in the current GBrain shell/runtime (`gbrain doctor --json` reported 91% coverage, 3 pages still missing embeddings on 2026-04-17)

## Open Threads
- Decide what to migrate first from `the-vault`
- Decide whether any part of `task-vault` should be preserved verbatim versus translated into GBrain task patterns
- Add initial seed pages so the brain contains real working context
- Make work rollups / standups identity-grounded across Slack, GitHub, Linear, and local git before trusting narrative automation
- Decide the durable Slack path that best matches the user-auth/private-analyst goal and does not break cron with interactive auth
- Backfill the 3 pages still missing embeddings coverage

## See Also
- [[README]]
- [[RESOLVER]]
- [[schema]]
- [[ops/tasks]]
- [Personal Work Rollup Automation](./personal-work-rollup-automation.md)
- [Identity-Grounded Work Rollups](../concepts/identity-grounded-work-rollups.md)

---

## Timeline
- 2026-04-16 — Created the `second-brain` repo and scaffolded it with the GBrain recommended structure.
- 2026-04-16 — Evaluated `the-vault`, `task-vault`, and GBrain; the direction became a hybrid that keeps Hermes as orchestrator and GBrain as the durable brain layer. [Source: session recall, 2026-04-16 16:09 Discord]
- 2026-04-16 — Imported the repo into GBrain and installed autopilot for continuous sync/maintenance.
- 2026-04-16 — Earlier setup check found shell-level `OPENAI_API_KEY` missing for GBrain embeddings.
- 2026-04-16 — Settled on a Discord-first operating surface, with Telegram treated as optional later rather than the main interface. [Source: session recall, 2026-04-16 08:59 Telegram]
- 2026-04-16 — Captured a private reflection on the setup day in [Second Brain Setup Reflection](../personal/2026-04-16-second-brain-setup-reflection.md). [Source: User, voice note, 2026-04-16]
- 2026-04-17 — Verified embeddings are working in the current shell/runtime (`gbrain doctor --json` reported 91% coverage, 3 pages still missing embeddings).
- 2026-04-17 — Reaffirmed that a user-auth / private-analyst Slack path is a better fit than a visible Slack bot for the intended workflow. [Source: session recall, 2026-04-16 12:08 Discord; reaffirmed in later recalls]
- 2026-04-17 — Identity-grounded work rollups became an explicit design requirement after standup drafting mixed repo activity with other people's work. [Source: session recall, 2026-04-17 07:50 and 14:40 Discord]
- 2026-04-18 — A scheduled morning review faulted when Slack MCP OAuth required browser authorization inside cron, which reinforced that non-interactive Slack-backed rollups are still fragile. [Source: session recall, 2026-04-18 08:07 Discord]
- 2026-04-18 — The current operating rhythm shifted toward todo-board refreshes at 08:00 / 12:00 / 16:00 Bangkok, with standup drafting kept manual in chat until attribution is trustworthy. [Source: session recall, 2026-04-18 22:09 Discord]
