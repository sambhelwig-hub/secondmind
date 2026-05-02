---
title: "Log"
type: log
created: 2026-05-02
updated: 2026-05-02
---

# Wiki Log

Chronological record of all wiki operations. Each entry uses a consistent prefix for parseability:
`grep "^## \[" log.md | tail -5`

---

## [2026-05-02] init | Wiki Bootstrapped

Initialized the LLM Wiki structure based on the pattern described by Andrej Karpathy.

**Created:**
- `CLAUDE.md` — schema & operating manual
- Templates: source, entity, concept, comparison, analysis
- `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`

---

## [2026-05-02] ingest | LLM Wiki — Andrej Karpathy

Ingested Karpathy's LLM Wiki gist as the founding source.

**Source:** `raw/karpathy-llm-wiki.md`

**Pages created (10):**
- `wiki/sources/karpathy-llm-wiki.md` — source summary
- `wiki/entities/andrej-karpathy.md` — entity page
- `wiki/entities/vannevar-bush.md` — entity page
- `wiki/concepts/llm-wiki-pattern.md` — core pattern
- `wiki/concepts/rag.md` — baseline approach
- `wiki/concepts/compiled-knowledge.md` — key insight
- `wiki/concepts/memex.md` — historical antecedent
- `wiki/concepts/wiki-maintenance-problem.md` — why this works
- `wiki/concepts/ingest-query-lint.md` — core operations
- `wiki/overview.md` — wiki overview

**Pages updated:**
- `wiki/index.md` — all new pages added

**Observations:**
- The founding source is meta — it describes the very system we're building. Future sources will bring domain-specific content.
- Several tools mentioned (qmd, Marp, Dataview, Obsidian Web Clipper) could get entity pages as they become relevant.
