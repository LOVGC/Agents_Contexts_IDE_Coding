---
title: LLM Wiki Research Journal Variant
type: item
category: Prompts
raw_source: raw/llm wiki updated version (with a directory that contains my own notes, i.e. mini-project).md
tags:
  - llm-wiki
  - prompt-example
  - research
  - journal
  - obsidian
created: 2026-04-13
updated: 2026-04-13
---

## What It Is

A prompt variant for setting up an LLM-maintained research wiki with a dedicated `raw/my_own_journal` area for human-authored notes, structured subfolders, and a roadmap journal that supports day-level ingestion tracking.

## When To Use

Use this when you want the wiki to combine imported sources with your own ongoing research notes and development diary, and you want the agent to mark individual roadmap days as ingested after filing them into the wiki.

## Key Details

- Extends the general LLM wiki pattern into a research-specific setup with a topic placeholder that should be customized for the user's project.
- Adds an explicit `raw/my_own_journal` structure for knowledge frameworks, papers, learnings, writings, coding material, and a research roadmap journal.
- Describes a set of human-authored writing files for real-world problem, research problem, related work and gaps, proposed method, and limitations or future work.
- Requires a discussion-first workflow for both ingest and lint so the agent reads the material, discusses emphasis with the user, and only then updates the wiki.
- Specifies that roadmap entries are date-headed and that a day should be marked as `ingested` after its content has been processed into the knowledge base.

## Related Items

- [[raw/llm_wiki.md]]
- [[raw/llm wiki for reasearch example.md]]
- [[wiki/items/llm-wiki-bootstrap-template]]
- [[wiki/items/llm-wiki-research-example]]
