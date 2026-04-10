---
title: LLM Wiki for Research Example
type: item
category: Prompts
raw_source: raw/llm wiki for reasearch example.md
tags:
  - llm-wiki
  - prompt-example
  - research
  - knowledge-base
  - obsidian
created: 2026-04-10
updated: 2026-04-10
---

## What It Is

A prompt example for setting up an LLM-maintained research wiki knowledge base focused on an individual research project. It adapts the broader "LLM Wiki" idea into a practical workflow for tracking project overview, research questions, baseline methods, proposed methods, experiment design, and ongoing development notes.

## When To Use

Use this when you want to build a personal, Obsidian-friendly research wiki where an LLM helps maintain structured notes from prompts, papers, prior notes, and codebases. It is especially useful when you want a human-in-the-loop ingest workflow where the agent first reads and discusses new material with you before updating the wiki.

## Key Details

- Positions the wiki as a persistent layer between immutable raw sources and future queries, so knowledge compounds instead of being re-derived every time.
- Specifies a minimal research-oriented wiki structure centered on project overview, research questions, problem formulation, baseline methods, proposed method, experiment design, and a daily development log.
- Emphasizes that the wiki should reflect the user's evolving understanding of the project and be revised as practical experience and experimental knowledge grow.
- Calls for ingesting a range of source types, including personal notes, useful papers, and relevant codebases, with all items organized and summarized in `index.md`.
- Requires a discussion-first workflow for both ingest and lint: the LLM should read and understand the material, discuss what to emphasize with the user, and only then update the knowledge base.

## Related Items

- [[raw/llm_wiki.md]]
- [[raw/LLM wiki for research team.md]]
- [[wiki/items/llm-wiki-bootstrap-template]]
- [[wiki/items/llm-wiki-research-team]]
