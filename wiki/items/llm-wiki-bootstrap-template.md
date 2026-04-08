---
title: LLM Wiki Bootstrap Template
type: item
category: Prompts
raw_source: raw/llm_wiki.md
tags:
  - llm-wiki
  - bootstrap
  - prompt-template
  - obsidian
created: 2026-04-08
updated: 2026-04-08
---

## What It Is

A template-style prompt and idea document for initializing a personal LLM-maintained wiki knowledge base, especially for organizing collected prompts, contexts, debugger configs, and project setup snippets.

## When To Use

Use this when you want an agent to help set up a lightweight Obsidian-friendly knowledge base that keeps raw files immutable, generates structured wiki notes, maintains a concise index, and supports ingest, query, and lint workflows.

## Key Details

- Frames the knowledge base as three layers: raw sources, generated wiki pages, and a schema file such as `AGENTS.md`.
- Emphasizes a persistent wiki that accumulates synthesis over time instead of re-deriving everything with ad hoc retrieval.
- Recommends an ingest workflow where the agent reads a raw source, creates a note, updates the index, and appends to a log.
- Suggests `index.md` as the main catalog and `log.md` as an append-only chronological record.
- Includes guidance for adapting the pattern to a minimal item-index use case rather than a large multi-page research wiki.
- Ends with a concrete request to set up the directory structure, create the schema file, and walk through the first ingest.

## Related Items

- [[raw/launch.json]]
- [[wiki/items/vscode-python-debugger]]
- [[raw/use_uv.md]]
