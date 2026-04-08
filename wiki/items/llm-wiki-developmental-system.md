---
title: LLM Wiki as a Developmental System
type: item
category: Prompts
raw_source: raw/llm_wiki_stem_cell.md
tags:
  - llm-wiki
  - idea-file
  - schema-evolution
  - knowledge-base
created: 2026-04-08
updated: 2026-04-08
---

## What It Is

An idea file for giving an LLM agent a high-level pattern: build a persistent wiki that not only accumulates knowledge from raw sources, but also revises its own schema as the user's understanding evolves.

## When To Use

Use this when you want an agent to implement a more adaptive LLM wiki system where the organization itself can mature over time instead of staying fixed to the user's earliest categories.

## Key Details

- Positions the document as an idea file to be copied into an LLM agent and collaboratively turned into a concrete implementation.
- Extends the basic LLM wiki pattern by arguing that the schema should be a developmental artifact, not a fixed specification.
- Introduces two extra operations beyond ingest, query, and lint: `reflect` and `migrate`.
- Treats the schema as something that should include rules for detecting strain, proposing restructurings, and preserving migration history.
- Distinguishes a stable core, such as immutable raw sources and traceable provenance, from plastic structure, such as page types, categories, and organizing axes.
- Emphasizes graph-first organization so the knowledge base can support multiple views instead of overcommitting to one rigid tree.
- Recommends preserving developmental history through schema history and migration records rather than silently replacing old structures.

## Related Items

- [[raw/llm_wiki.md]]
- [[wiki/items/llm-wiki-bootstrap-template]]
- [[raw/use_uv.md]]
