# Schema

## Founding principles

- One primary home per page.
- Every important directory has a local README explaining what belongs there.
- Pages separate current synthesis from evidence.
- Cross-links are preferred over duplication.

## Page shape

A standard brain page should usually look like this:

```md
# Title

> Executive summary: the current state in one short paragraph.

## State
- Key facts that are currently true

## Open Threads
- Active unresolved items

## See Also
- Related pages

---

## Timeline
- YYYY-MM-DD — sourced event or observation
```

## Above / below the line

- Above the horizontal rule: compiled truth, rewritten as knowledge improves.
- Below the horizontal rule: dated evidence, timeline, transcript fragments, notes, and source trace.

## Identity

- Use canonical kebab-case slugs as filenames.
- People pages live in `people/`; company pages live in `companies/`.
- Store per-entity raw API payloads in `.raw/` sidecars under the relevant directory.

## Tasks

Tasks live in `ops/tasks.md` and follow the GBrain priority model:
- P0 — urgent
- P1 — today
- P2 — this week
- P3 — backlog

## Inbox

`inbox/` is temporary holding space. Anything that stays there for long is a schema signal.
