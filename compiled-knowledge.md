---
title: "Compiled Knowledge"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [core-insight, knowledge-management]
sources: [karpathy-llm-wiki]
status: draft
---

# Compiled Knowledge

## Definition

Knowledge that has been processed, synthesized, and integrated into a persistent structure once, rather than being re-derived from raw sources on every query.

## Explanation

The analogy is to compiled vs. interpreted code. In [[rag|RAG]], the LLM "interprets" raw documents at query time — finding relevant chunks and assembling an answer from scratch. In the [[llm-wiki-pattern]], the LLM "compiles" knowledge: it reads each source, extracts key information, synthesizes it with existing knowledge, and writes the result into wiki pages. The compiled wiki can then be queried efficiently without re-reading raw sources.

The trade-off: compilation requires upfront work (the ingest step), but queries against compiled knowledge are faster, more consistent, and benefit from cross-references that have already been built.

## Examples

- A wiki page on an entity that synthesizes information from 5 different sources is compiled knowledge.
- A RAG answer that retrieves chunks from the same 5 sources and generates a response on the fly is interpreted knowledge.

## Related Concepts

- [[rag]] — the "interpreted" approach
- [[llm-wiki-pattern]] — the system built on compiled knowledge
- [[ingest-query-lint]] — ingest is the compilation step

## Sources

- [[karpathy-llm-wiki]]

## Open Questions

- How do you handle "compiled" knowledge becoming stale when sources are updated?
- Is there a meaningful latency difference between querying a wiki vs. RAG at scale?
