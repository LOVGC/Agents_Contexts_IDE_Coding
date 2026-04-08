---
title: LLM Wiki for Research Team
type: item
category: Prompts
raw_source: raw/LLM wiki for research team.md
tags:
  - llm-wiki
  - prompt-example
  - research-team
  - meetings
created: 2026-04-08
updated: 2026-04-08
---

## What It Is

A prompt example for setting up a minimal LLM-maintained wiki for a research team. It adapts the general "LLM Wiki" pattern into a practical workflow for tracking research goals, baseline methods, proposed methods, meeting notes, and source summaries.

## When To Use

Use this when you want an LLM agent to help maintain a lightweight, Obsidian-friendly research wiki that grows over time from meeting transcripts, papers, blog posts, and web pages. It is especially useful when the team wants a repeatable ingest workflow with human feedback before updates are committed into the wiki.

## Key Details

- Frames the wiki as a persistent artifact between immutable raw sources and user queries.
- Emphasizes LLM-assisted maintenance of summaries, cross-references, index updates, and chronological logs.
- Recommends a human-in-the-loop ingest flow where the LLM first reads and summarizes a source, discusses the summary with the user, incorporates feedback, and only then updates the wiki.
- Tailors the workflow to a research team context with recurring meeting-script ingest under `raw/meetings` plus additional ingest for papers, blogs, and webpages.
- Prioritizes a simple schema and directory structure that is sufficient for recording project goals, research questions, baseline methods, and proposed methods under active investigation.

## Related Items

- [[raw/llm_wiki.md]]
- [[raw/llm_wiki_stem_cell.md]]
- [[wiki/items/llm-wiki-bootstrap-template]]
- [[wiki/items/llm-wiki-developmental-system]]
