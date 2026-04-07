# LLM Wiki as a Developmental System

A pattern for building personal knowledge bases using LLMs.

This is an idea file designed to be copy-pasted into your own LLM agent (for example OpenAI Codex, Claude Code, OpenCode / Pi, or similar). Its goal is to communicate a high-level pattern. The exact implementation should be worked out collaboratively between you and the agent.

## The core idea

Most people's experience with LLMs and documents looks like RAG: you upload a collection of files, the LLM retrieves relevant chunks at query time, and generates an answer. This works, but the LLM is rediscovering knowledge from scratch on every question. There is no accumulation. Ask a subtle question that requires synthesizing five documents, and the LLM has to find and piece together the relevant fragments every time. Nothing is built up.

The idea here is different. Instead of only retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki — a structured, interlinked collection of markdown files that sits between you and the raw sources. When you add a new source, the LLM does not just index it for later retrieval. It reads it, extracts the key information, integrates it into the existing wiki, updates entity and concept pages, revises summaries, notes contradictions, and strengthens or challenges the evolving synthesis. The knowledge is compiled once and then kept current, not re-derived on every query.

That is already a big shift. But this document argues for one more step.

The wiki should not only accumulate knowledge. It should also be able to revise the *schema by which that knowledge is organized*.

In other words: the wiki should behave less like a static filing cabinet and more like a developmental system.

## The stem-cell idea

A fixed schema is useful early on, but it can also trap the wiki inside the user's early understanding of a domain.

When you first learn a subject, your categories are often shallow, local, and task-driven. Later, after reading more and seeing more examples, you may realize that the domain is better organized around deeper and more general axes. What looked like the right structure at the beginning may turn out to be just one temporary developmental stage.

For example, someone learning deep learning might initially organize their notes around:

- classification
- regression
- MLPs
- linear algebra

Later, with more exposure, they may realize that a better organizing structure is:

- data and data-generating assumptions
- model architecture and inductive bias
- training and optimization
- evaluation, metrics, and generalization

The key point is that learning is not just the accumulation of more facts inside a fixed structure. Learning also changes the structure itself.

This is the stem-cell analogy.

A stem cell is not valuable because it is undefined forever. It is valuable because it retains the capacity to differentiate into more specialized forms as development proceeds. Likewise, a good knowledge system should not be fully rigid at the start. It should retain the capacity to reorganize itself as the user's understanding becomes deeper, broader, and more abstract.

So the schema should not be treated as a fixed specification. It should be treated as a developmental artifact.

## The upgraded claim

The original LLM wiki idea says that the wiki is persistent and compounding, and that the schema should co-evolve with the user and the LLM over time.

This document makes that idea explicit and operational:

> The LLM should not only maintain the wiki. It should also periodically reflect on whether the current schema still matches the user's evolving understanding, and when appropriate, propose or perform schema migrations.

This turns co-evolution from an informal attitude into a system behavior.

## Architecture

There are still three main layers, but the third one becomes much more important.

**Raw sources** — your curated collection of source documents. Articles, papers, books, images, datasets, notes, transcripts. These are immutable. The LLM reads from them but never modifies them. This is your source of truth.

**The wiki** — a directory of LLM-generated markdown files. Summaries, entity pages, concept pages, comparisons, syntheses, timelines, glossaries, question pages, and so on. The LLM owns this layer entirely. It creates pages, updates them when new sources arrive, maintains cross-references, and keeps the wiki internally coherent. You read it; the LLM writes it.

**The schema** — a document (for example `CLAUDE.md` or `AGENTS.md`) that tells the LLM how the wiki is structured, what conventions it should follow, what kinds of pages exist, how sources should be ingested, how questions should be answered, how claims should be cited, and how maintenance should be performed.

But here is the important change:

**The schema itself must include rules for its own evolution.**

It should not just say how the current wiki is organized. It should also say:

- how to detect that the current organization is breaking down
- how to notice emerging conceptual axes
- how to propose or perform restructurings
- how to preserve history when the structure changes
- how to distinguish low-risk local edits from high-risk global migrations

In that sense, the schema is not just a configuration file. It is a developmental program.

## Stable core, plastic structure

A good developmental wiki should not be completely fluid. Some things should remain stable, while others should remain plastic.

### Stable core

These are the constraints that should usually stay fixed:

- Raw sources are never rewritten.
- Important claims should remain traceable to sources.
- Major changes to the wiki structure should be logged.
- Old pages should not vanish silently; use redirects, aliases, or migration notes where possible.
- The wiki should remain human-readable and inspectable at all times.
- The LLM should preserve provenance, revision history, and internal consistency.

### Plastic structure

These are the parts that should be allowed to evolve:

- page types
- top-level categories
- naming conventions
- the main organizing axes of the domain
- whether knowledge is grouped by tasks, mechanisms, entities, stages, questions, or viewpoints
- which concepts deserve their own pages
- which pages are first-class and which should be demoted to examples or case studies

The point is not to make everything unstable. The point is to keep the right parts flexible.

## Organization should be graph-first, not tree-first

A developmental system should avoid overcommitting to a single rigid tree structure too early.

Folders are useful, but they can freeze one particular view of the domain. As understanding grows, the same material may need to be seen from multiple perspectives. A concept might belong simultaneously to data, modeling, optimization, and evaluation. A method might be both a case study and an instance of a broader principle.

So the primary unit should be the page, and the primary structure should be links, tags, typed relations, and multiple views over the same set of pages. The directory tree can still exist, but it should be treated as one projection of the knowledge graph, not the ontology itself.

## Operations

The original LLM wiki pattern has three key operations: ingest, query, and lint. A developmental wiki needs two more: reflect and migrate.

### Ingest

You add a new source to the raw collection and tell the LLM to process it.

A typical flow:

- read the source
- discuss the important takeaways with you
- create or update a source summary page
- update relevant concept and entity pages
- add cross-references
- update the index
- append an entry to the log

A single source may touch many pages. The wiki becomes richer with each ingestion.

### Query

You ask questions against the wiki.

The LLM reads the index and relevant pages, synthesizes an answer, cites sources, and returns the result in an appropriate form: a markdown page, comparison table, chart, slide deck, note, or analysis. Good answers can themselves be filed back into the wiki as new pages.

This matters because good questions often reveal missing structure. A query is not just a request for output. It is also a probe into the current shape of the wiki.

### Lint

Periodically, the LLM should health-check the wiki. Look for:

- contradictions between pages
- stale claims superseded by newer sources
- orphan pages
- missing cross-references
- important concepts that lack their own pages
- unexplained repeated patterns
- inconsistent naming
- missing provenance

Lint keeps the wiki healthy at the content level.

### Reflect

This is the new operation.

Periodically, the LLM should also reflect on the *schema itself*.

Questions to ask include:

- Does the current taxonomy still match how the user is actually reasoning about the domain?
- Are many pages awkwardly split across categories?
- Are there repeated cross-links that suggest a missing higher-level abstraction?
- Are new conceptual axes emerging across multiple sources and queries?
- Is the wiki still organized around early, shallow categories that no longer carry much explanatory power?
- Are there recurring user explanations that do not fit the current schema well?

This is schema-lint.

The goal is not constant reorganization. The goal is to detect when the current structure has become a bottleneck.

### Migrate

When reflection reveals that the schema has materially drifted from the user's understanding, the LLM can propose or perform a migration.

A migration might include:

- introducing a new page type
- creating a new top-level view
- merging overlapping pages
- splitting an overloaded page into a concept page and several case-study pages
- reclassifying pages under new organizing axes
- demoting old categories to historical views
- creating aliases or redirects from old names to new ones
- writing migration notes so the evolution remains legible

Large migrations should be explicit and reviewable. Small migrations can often happen automatically.

## When should the LLM trigger reflection?

The schema should define concrete triggers, for example:

- after every N ingested sources
- after a burst of queries that repeatedly cross unrelated parts of the tree
- when the same concept is repeatedly explained in multiple places
- when many pages end up in catch-all categories like `misc` or `notes`
- when new recurring patterns appear across sources
- when the user starts explaining the domain with a new abstraction that is not reflected in the wiki
- when the graph structure shows strong clusters that the current schema does not recognize

These triggers do not force a migration. They only force a check.

## What should reflection produce?

Reflection should not just generate vague thoughts. It should produce concrete artifacts, such as:

- a short report on the current schema's limitations
- candidate new organizing axes
- proposed page migrations
- concepts that should be promoted to first-class pages
- concepts that should be demoted to examples, aliases, or historical artifacts
- the expected benefits and risks of restructuring
- a recommended action level: no action, small local edits, or large migration

That keeps reflection grounded.

## Preserve developmental history

One of the most important rules is this: when the wiki evolves, it should not erase its own developmental history.

Earlier structures are not necessarily mistakes. They may reflect earlier stages of understanding that were useful at the time. In many domains, that history is itself valuable.

So a developmental wiki should preserve records of major structural changes. For example:

- `schema/current.md`
- `schema/history/2026-04-07.md`
- `migrations/2026-04-07-task-centric-to-mechanism-centric.md`

This makes the user's own learning trajectory visible.

## Example: deep learning notes

Imagine a user who starts learning deep learning.

At first the wiki is organized around:

- classification
- regression
- MLPs
- optimization basics
- linear algebra background

This is fine. It matches the user's initial entry points.

After enough reading and experimentation, the LLM notices that the user's questions and notes are increasingly organized around a different structure:

- what assumptions are being made about the data
- what architectural priors are encoded in the model
- how training dynamics shape outcomes
- how evaluation differs from deployment objectives

The LLM runs reflection and concludes that the current task-centric schema is now limiting. It proposes a migration:

- keep the old task-centric pages as onboarding and historical views
- add a mechanism-centric top-level structure
- move many method pages under data / architecture / optimization / evaluation views
- rewrite the index to surface both beginner and advanced views
- add migration notes so the change is explicit

The result is not just a larger wiki. It is a more mature one.

## Avoid schema thrashing

A developmental system can also fail by changing too often.

The schema should not be rewritten every time the user learns one new idea or gets briefly excited about a new abstraction. The system needs some inertia.

A useful rule is:

- local edits can happen often
- global reorganizations should be rare

A new abstraction should usually appear repeatedly across sources, queries, and pages before it becomes part of the main schema.

In other words, the wiki should be adaptable without being unstable.

## Indexing and logging

Two special files still matter a lot.

**`index.md`** is content-oriented. It catalogs the wiki's current pages and views. In a developmental wiki, it may expose multiple top-level views of the same underlying graph: beginner view, mechanism-centric view, chronology view, question view, and so on.

**`log.md`** is chronological. It records ingests, queries, lint passes, reflections, and migrations. A useful convention is to keep entries machine-parseable, for example:

```md
## [2026-04-02] ingest | Batch Normalization paper
## [2026-04-05] reflect | Taxonomy strain in optimization pages
## [2026-04-07] migrate | task-centric -> mechanism-centric schema
```

The log gives both the user and the LLM a timeline of how the wiki evolved.

## Optional tooling

As the wiki grows, it may help to add small tools:

- search over markdown pages
- graph analysis to detect clusters and weakly connected regions
- scripts for alias generation and redirect management
- schema-diff tools
- page migration helpers
- dashboards for orphan pages, overloaded pages, and uncited claims

These are optional, but useful once the wiki becomes large enough that manual inspection is no longer enough.

## Why this works

The hard part of building a useful knowledge base is not only storing information. It is maintaining the relationships, summaries, cross-references, and structure as understanding evolves.

Humans are bad at this because the maintenance burden compounds. They read, think, and have insights, but they often do not go back and reorganize fifty pages to reflect a better conceptual structure.

LLMs are unusually well-suited to this kind of work. They can summarize, cross-reference, relink, rename, split, merge, and rewrite without getting bored. More importantly, they can help with *structural maintenance*, not just content maintenance.

That is the key upgrade here.

The human's job is to choose sources, ask good questions, notice what matters, and decide what kind of understanding they want to build.

The LLM's job is everything else: not just maintaining the current wiki, but helping the wiki remain developmentally aligned with the user's growing understanding.

## Note

This document is intentionally abstract. It describes a pattern, not a single implementation. The exact directory layout, page templates, relation types, migration thresholds, reflection cadence, and tooling should depend on the domain, the user, and the agent.

The important thing is the principle:

A good LLM wiki should not only accumulate knowledge. It should also preserve the capacity to reorganize itself as understanding deepens.

That is the stem-cell idea applied to knowledge systems.
