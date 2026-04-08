---
title: Log
type: concept
sources: []
related:
  - wiki/index.md
  - wiki/concepts/overview.md
created: 2026-04-07
updated: 2026-04-07
confidence: high
---

# Log

This is the append-only timeline of wiki activity.

Use headings in the format `## [YYYY-MM-DD] type | Title`.

## [2026-04-07] bootstrap | Minimal LLM wiki scaffold

Initialized the vault with:

- a root `AGENTS.md`
- `raw/` for immutable sources
- `wiki/index.md` as the navigation entrypoint
- `wiki/log.md` as the append-only activity log
- `wiki/overview.md` as the top-level synthesis page
- `wiki/sources/` for source summaries
- `wiki/topics/` for synthesized topic pages

## [2026-04-07] restructure | Align wiki to revised schema

Adjusted the wiki scaffold to match the current schema:

- added required YAML frontmatter to existing wiki pages
- replaced the loose `topics` structure with `concepts` and `entities`
- moved the overview page into `wiki/concepts/overview.md`
- updated `wiki/index.md` to catalog concepts, entities, source summaries, and comparisons
