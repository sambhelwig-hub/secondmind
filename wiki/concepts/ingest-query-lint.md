---
title: "Ingest, Query, Lint"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [workflow, operations, core]
sources: [karpathy-llm-wiki]
status: complete
---

# Ingest, Query, Lint

## Definition

The three core operations that drive the [[llm-wiki-pattern]].

## Explanation

### Ingest

Process a new raw source into the wiki. The LLM reads the source, creates a summary page, identifies entities and concepts, updates or creates their wiki pages, updates the index and log, and reports what changed. A single ingest can touch 10-15 pages. Can be done one source at a time (with human involvement) or in batches.

### Query

Ask a question against the wiki. The LLM reads the index to find relevant pages, reads those pages, and synthesizes an answer with citations. Key insight: valuable answers should be filed back into the wiki (as analysis or comparison pages) so that explorations compound alongside ingested sources.

### Lint

Health-check the wiki. Look for contradictions between pages, stale claims superseded by newer sources, orphan pages with no inbound links, concepts mentioned but lacking their own page, missing cross-references, and data gaps. The LLM suggests fixes; the human approves them.

## Examples

- **Ingest**: "Process this article about transformer architectures" → source page + 5 entity updates + 3 concept updates + index + log.
- **Query**: "How does attention differ from recurrence?" → synthesized answer from wiki pages → optionally filed as a comparison page.
- **Lint**: "Health-check the wiki" → "Found 3 orphan pages, 1 contradiction between X and Y, concept Z mentioned 4 times but has no page."

## Related Concepts

- [[llm-wiki-pattern]] — the system these operations serve
- [[compiled-knowledge]] — ingest is the compilation step

## Sources

- [[karpathy-llm-wiki]]

## Open Questions

- What's the right cadence for lint? After every N ingests? On demand?
- Should query answers be auto-filed or always ask the human?
