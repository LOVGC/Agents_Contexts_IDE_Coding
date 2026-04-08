# LLM Wiki Schema

## Project Structure
- `raw/` - immutable source documents. NEVER modify.
- `wiki/index.md` - the single knowledge index. Keep a summary of each ingested file here.
- `wiki/log.md` - append-only ingest activity log.
- Legacy folders such as `wiki/sources/`, `wiki/concepts/`, `wiki/entities/`, and comparison pages are not part of the active workflow. Do not create or update them unless I explicitly ask.

## `wiki/index.md` Format
For each ingested file, maintain one section in `wiki/index.md` using this template:

```md
### raw/<filename>
Ingested: YYYY-MM-DD

Summary:
A short paragraph summarizing the file.

Key Takeaways:
- Point 1
- Point 2
- Point 3
```

- Keep exactly one section per ingested source file.
- If a file is re-ingested, update the existing section instead of adding a duplicate.
- No separate concept, entity, source-summary, or comparison pages are required.
- YAML frontmatter is not required for these per-file summary entries.

## Ingest Workflow
When I say "ingest [filename]":
1. Read the source file in `raw/`
2. Discuss key takeaways with me
3. Add or update that file's section in `wiki/index.md`
4. Append an entry to `wiki/log.md`
5. Do not create or update separate summary, concept, entity, or comparison pages unless I explicitly ask

## Query Workflow
When I ask a question:
1. Read `wiki/index.md` to find relevant file summaries
2. Answer from those summaries first
3. If the summaries are insufficient, read the relevant files in `raw/` and incorporate that information
4. Cite the relevant `wiki/index.md` section and source file paths plainly; `[[wiki-link]]` citations are not required
5. If the answer is worth saving, offer to update the relevant summary in `wiki/index.md`

## Lint Workflow
When I say "lint":
1. Check whether files that have been ingested are missing sections in `wiki/index.md`
2. Check for duplicate file sections in `wiki/index.md`
3. Check whether summaries are stale or inconsistent with the corresponding files in `raw/`
4. Check whether `wiki/log.md` and `wiki/index.md` are broadly consistent about what has been ingested
5. Suggest useful next ingest or cleanup tasks
