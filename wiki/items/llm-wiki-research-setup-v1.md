---
title: LLM Wiki Research Setup v1
type: item
category: Prompts
raw_source: raw/llm_wiki_v1.md
tags:
  - llm-wiki
  - prompt-example
  - research
  - journal
  - obsidian
created: 2026-04-14
updated: 2026-04-14
---

## What It Is

A research-oriented adaptation of the general "LLM Wiki" idea that asks an agent to set up a personal project wiki, define an `AGENTS.md` schema, and support a discussion-first workflow for ingesting sources into an evolving knowledge base.

## When To Use

Use this when you want to build an Obsidian-friendly research wiki around a single project, with concise overview pages, a running development diary, organized ingest tracking, and human-in-the-loop discussion before the wiki is updated.

## Key Details

- Starts from Karpathy's broader LLM wiki pattern of immutable raw sources, an LLM-maintained wiki layer, and a schema file that defines workflows and conventions.
- Adapts that pattern to research by emphasizing a project overview page that tracks the real-world problem, research questions, formulation, baseline methods, proposed method, experiment design, current status, next steps, and milestones.
- Calls for a separate development-log style page to record daily work, thoughts, and what should happen next.
- Requires `index.md` to stay organized and concise while covering ingested notes, papers, and codebases.
- Specifies a discussion-first workflow for ingest and lint, where the agent reads the material, discusses emphasis with the user, and only then updates the wiki.
- Proposes a structured `raw/my_own_journal` area for knowledge frameworks, papers, learnings, writings, coding material, and a roadmap journal with day-level tracking.
- Also suggests marking ingested roadmap sections or raw files with `(ingested)`, which is notable because that behavior would require a different raw-source policy than the current repo rules.

## Related Items

- [[raw/llm_wiki.md]]
- [[raw/llm wiki for reasearch example.md]]
- [[raw/llm wiki updated version (with a directory that contains my own notes, i.e. mini-project).md]]
- [[wiki/items/llm-wiki-bootstrap-template]]
- [[wiki/items/llm-wiki-research-example]]
- [[wiki/items/llm-wiki-research-journal-variant]]
