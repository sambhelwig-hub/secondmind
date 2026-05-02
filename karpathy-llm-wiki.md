---
title: "LLM Wiki — Andrej Karpathy"
type: source
created: 2026-05-02
updated: 2026-05-02
tags: [llm, knowledge-management, wiki, obsidian, rag, personal-knowledge-base]
author: "Andrej Karpathy"
url: "https://gist.github.com/karpathy/1dd0294ef9567971c1e4348a90d69285"
status: complete
---

# LLM Wiki — Andrej Karpathy

> **Author:** Andrej Karpathy
> **Date:** ~April 2026
> **URL:** https://gist.github.com/karpathy/1dd0294ef9567971c1e4348a90d69285

## Summary

Karpathy proposes a pattern called "LLM Wiki" for building personal knowledge bases where the LLM is not just a query engine (as in [[rag|RAG]]) but an active wiki maintainer. Instead of re-deriving knowledge from raw documents on every question, the LLM incrementally builds a persistent, interlinked collection of markdown files — a compiled knowledge layer that sits between the human and the raw sources.

The architecture has three layers: **raw sources** (immutable documents the LLM reads from), **the wiki** (LLM-generated and maintained markdown pages), and **the schema** (a config file like CLAUDE.md that defines structure and workflows). The human curates sources and asks questions; the LLM handles all the bookkeeping — summarizing, cross-referencing, filing, flagging contradictions, and maintaining consistency.

Three core operations drive the system: **ingest** (process a new source into the wiki, touching 10-15 pages), **query** (answer questions by reading wiki pages, optionally filing answers back), and **lint** (health-check for contradictions, orphans, stale content, and gaps).

The key insight is that wikis fail because maintenance cost outpaces value for humans. LLMs eliminate that constraint — they don't get bored, don't forget cross-references, and can update dozens of files in one pass. The maintenance cost drops to near zero, so the wiki actually compounds over time.

Karpathy draws a lineage to [[vannevar-bush|Vannevar Bush's]] Memex (1945) — a private, curated knowledge store with associative trails. The piece Bush couldn't solve was who does the maintenance. LLMs handle that.

## Key Takeaways

- RAG retrieves and re-derives; LLM Wiki compiles and compounds. The wiki is a persistent artifact, not an ephemeral retrieval step.
- The LLM is the writer and maintainer of the wiki. The human never (or rarely) writes wiki pages directly.
- A single source ingest can touch 10-15 wiki pages — summaries, entities, concepts, cross-references, the index, the log.
- Good query answers should be filed back into the wiki so explorations compound alongside ingested sources.
- Two navigation files: `index.md` (content catalog) and `log.md` (chronological record). The index replaces RAG at moderate scale (~100 sources, hundreds of pages).
- The schema file (CLAUDE.md / AGENTS.md) is the critical configuration — it turns the LLM from a generic chatbot into a disciplined wiki maintainer.
- Obsidian is the recommended IDE for browsing the wiki in real time alongside the LLM agent.

## Entities Mentioned

- [[andrej-karpathy]] — author of the pattern
- [[vannevar-bush]] — historical precedent (Memex, 1945)

## Concepts Discussed

- [[llm-wiki-pattern]] — the core pattern described
- [[rag]] — the conventional approach this pattern improves upon
- [[compiled-knowledge]] — knowledge compiled once vs. re-derived on every query
- [[memex]] — Bush's 1945 vision of a personal knowledge store
- [[wiki-maintenance-problem]] — why human-maintained wikis fail
- [[ingest-query-lint]] — the three core operations

## Notable Quotes

- "The wiki is a persistent, compounding artifact."
- "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."
- "Humans abandon wikis because the maintenance burden grows faster than the value."
- "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## Connections

This is the founding document of this wiki. All structural decisions trace back to it.

## Open Questions

- How well does the index-based navigation scale beyond hundreds of pages? At what point is search infrastructure (e.g. [[qmd]]) necessary?
- How should multi-user wikis handle conflicting edits or different editorial perspectives?
- What's the best strategy for ingesting non-text sources (images, audio, video)?
- How do you handle version control and rollback when the LLM makes a bad update?
