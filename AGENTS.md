# Minimal LLM Wiki Schema

This repository is a small, Obsidian-friendly knowledge base for collected items such as prompts, contexts, debugger configs, and project setup snippets.

## Directory Layout
- `raw/` contains immutable source files. Read from here, never rewrite files here.
- `wiki/items/` contains one generated note per ingested raw source.
- `wiki/index.md` is the main catalog. Read this file first when answering questions.
- `wiki/log.md` is the append-only activity log.

## Non-Negotiable Rules
- Never modify, rename, or delete files under `raw/`.
- Prefer Obsidian wiki links such as `[[raw/launch.json]]` and `[[wiki/items/vscode-python-debugger]]`.
- Keep `wiki/index.md` short and scannable. Each entry should stay to one sentence.
- Use practical categories by default: `Contexts`, `Prompts`, `VS Code / Debugger`, and `Project Setup`.
- Add a new category only when at least two items justify it.
- Default to one note in `wiki/items/` for every newly ingested raw source.
- Existing raw-only entries are acceptable during bootstrap, but every future ingest must create the item note in the same turn.
- During ingest, present the planned category, note path, draft note content, draft index entry, and draft log entry to the user first, then wait for feedback before modifying any wiki files.

## Item Note Template
Every note in `wiki/items/` must use this frontmatter shape:

```yaml
---
title: Short Title
type: item
category: Category Name
raw_source: raw/path.ext
tags:
  - tag-one
  - tag-two
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

Every item note must use these sections in this order:
1. `## What It Is`
2. `## When To Use`
3. `## Key Details`
4. `## Related Items`

## Workflow: Ingest
When I say `ingest raw/<path>`:
1. Read the source file from `raw/`.
2. Decide the best practical category and draft the planned wiki changes.
3. Present the proposed modifications to the user before editing any files. This preview must include the category, the note path, the draft note content, the exact `wiki/index.md` line, and the exact `wiki/log.md` entry.
4. Discuss the draft with the user and incorporate feedback.
5. Only after the discussion, create or update exactly one note in `wiki/items/`.
6. Update `wiki/index.md` with a one-line entry that starts with the raw link and, when available, ends with `Note: [[wiki/items/...]]`.
7. Append a machine-parseable log entry to `wiki/log.md` using `## [YYYY-MM-DD] ingest | filename`.
8. Never modify the raw source itself.

## Workflow: Query
When I ask a question:
1. Read `wiki/index.md` first.
2. Read relevant notes in `wiki/items/`.
3. Read raw files only when the index and notes are not enough.
4. Answer with Obsidian-style citations where useful.
5. If the answer would be valuable later, offer to file it back into `wiki/items/` or another wiki page.

## Workflow: Lint
When I say `lint`:
1. Check for uncategorized items.
2. Check for duplicate notes that describe the same raw source.
3. Check for broken wiki-links.
4. Check for stale or vague one-line descriptions in `wiki/index.md`.
5. Check for raw files that are missing matching notes after ingest.
