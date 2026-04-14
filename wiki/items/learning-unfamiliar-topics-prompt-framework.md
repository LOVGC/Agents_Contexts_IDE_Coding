---
title: Learning Unfamiliar Topics Prompt Framework
type: item
category: Prompts
raw_source: raw/learning unfamiliar topics prompts.md
tags:
  - prompt
  - learning
  - active-recall
  - mental-models
created: 2026-04-14
updated: 2026-04-14
---

## What It Is

A prompt framework for learning an unfamiliar topic by first grounding an LLM in core source material and then using structured questions to map the field and test real understanding.

## When To Use

Use this when you are entering a new topic and want a fast way to understand its core concepts, identify where experts disagree, and check whether your understanding goes beyond memorized facts.

## Key Details

- Opens with basic orientation questions such as what the topic is, how it works, and why it is needed.
- Recommends feeding the LLM foundational material first, such as textbooks, lecture slides, video scripts, or papers.
- Uses expert-level questions to extract shared mental models and major points of disagreement in the field.
- Adds a depth test by asking for questions that distinguish genuine understanding from surface memorization.
- Suggests an immediate follow-up on wrong answers: explain why the answer is wrong and what is missing.
- Includes a short rationale tied to active recall, desirable difficulty, and learning conceptual structure before details.

## Related Items

- [[raw/summary_prompts.md]]
- [[wiki/items/chapter-summary-prompt]]
- [[wiki/items/llm-wiki-bootstrap-template]]
