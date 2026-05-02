---
title: "LLM Wiki Pattern"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [pattern, llm, knowledge-management, core]
sources: [karpathy-llm-wiki]
status: complete
---

# LLM Wiki Pattern

## Definition

A pattern for building personal knowledge bases where an LLM incrementally builds and maintains a persistent wiki of interlinked markdown files, rather than re-deriving knowledge from raw documents on every query (as in [[rag|RAG]]).

## Explanation

The pattern inverts the typical RAG workflow. Instead of storing raw documents and retrieving relevant chunks at query time, the LLM reads each new source, extracts key information, and **compiles** it into an evolving wiki — updating entity pages, concept summaries, cross-references, and the overall synthesis. The result is [[compiled-knowledge]]: knowledge built up once and kept current, not re-derived every time.

The architecture has three layers:

1. **Raw sources** — immutable source documents (articles, papers, notes). The LLM reads from this layer but never writes to it.
2. **The wiki** — LLM-generated markdown pages organized by type (sources, entities, concepts, comparisons, analyses). The LLM owns this layer entirely.
3. **The schema** — a configuration document (e.g. CLAUDE.md) defining structure, conventions, and workflows.

Three operations drive the system: [[ingest-query-lint|ingest, query, and lint]].

The human's role is to curate sources, direct analysis, and ask good questions. The LLM handles all bookkeeping — the work that causes human-maintained wikis to be abandoned (see [[wiki-maintenance-problem]]).

## Examples

- **Personal**: tracking goals, health, self-improvement across journal entries, articles, podcast notes.
- **Research**: deep-diving a topic over months, building a comprehensive wiki with an evolving thesis.
- **Book reading**: building a companion wiki with characters, themes, and plot threads as you read.
- **Business**: internal wiki fed by Slack threads, meeting transcripts, project docs, customer calls.
- **Any accumulative domain**: competitive analysis, due diligence, trip planning, course notes.

## Related Concepts

- [[rag]] — the conventional approach this pattern improves upon
- [[compiled-knowledge]] — the core insight: compile once, query many
- [[memex]] — the 1945 historical antecedent
- [[wiki-maintenance-problem]] — why this pattern works where human wikis fail
- [[ingest-query-lint]] — the three core operations

## Sources

- [[karpathy-llm-wiki]] — the founding document

## Open Questions

- What's the ceiling for this pattern in terms of wiki size before search infrastructure becomes necessary?
- How well does it generalize beyond single-user knowledge bases to team settings?
- Can multiple LLMs maintain the same wiki, or do you need a single maintainer?
