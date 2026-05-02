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

---

## [2026-05-02] ingest | Finance Careers Overview — Ned

Ingested Ned's finance careers video transcript.

**Source:** `raw/ned-finance-careers.md`

**Pages created (14):**
- `wiki/sources/ned-finance-careers.md` — source summary
- `wiki/entities/ned.md` — founder of 365 Financial Analyst
- `wiki/entities/pwc.md` — PwC (Big Four consulting firm)
- `wiki/concepts/corporate-finance.md` — accounting and analysis roles
- `wiki/concepts/investment-banking.md` — capital raising and M&A
- `wiki/concepts/investment-management.md` — VC and PE
- `wiki/concepts/traditional-banking.md` — lending and credit
- `wiki/concepts/financial-services.md` — consulting and auditing
- `wiki/concepts/ma-analyst.md` — M&A specialist role
- `wiki/concepts/venture-capital-analyst.md` — early-stage investing
- `wiki/concepts/private-equity-analyst.md` — mature company investing
- `wiki/entities/kpmg.md` — stub (Big Four)
- `wiki/entities/ey.md` — stub (Big Four)
- `wiki/entities/deloitte.md` — stub (Big Four)

**Pages updated:**
- `wiki/index.md` — added 14 new pages
- `wiki/overview.md` — updated themes and state
- `wiki/log.md` — this entry

**Cross-linking:**
- All new finance concepts reference each other
- New entity pages (Ned, PwC, etc.) linked in source summary

**Observations:**
- The source provides a broad taxonomy of finance careers (six domains) that can be expanded deeply in future ingests.
- Ned emphasizes a recurring theme: university doesn't teach practical skills, only theory.

---

## [2026-05-02] ingest | Financial Modeling Guide for Beginners — Financial Edge

Ingested Financial Edge's comprehensive financial modeling guide.

**Source:** `raw/financial-modeling-guide.md`

**Pages created (9):**
- `wiki/sources/financial-modeling-guide.md` — source summary
- `wiki/entities/financial-edge.md` — finance education company
- `wiki/concepts/financial-modeling.md` — core concept and definition
- `wiki/concepts/three-statement-model.md` — Income Statement + Balance Sheet + Cash Flow
- `wiki/concepts/dcf-model.md` — Discounted Cash Flow valuation
- `wiki/concepts/lbo-model.md` — Leveraged Buyout structuring
- `wiki/concepts/ma-model.md` — M&A financial analysis
- `wiki/concepts/excel-financial-modeling.md` — Technical skills and Excel formulas
- `wiki/concepts/model-assumptions.md` — Forecasting and sensitivity analysis
- `wiki/concepts/financial-model-best-practices.md` — Design, documentation, maintenance

**Pages updated:**
- `wiki/index.md` — added 9 new pages, 1 new entity
- `wiki/log.md` — this entry

**Critical Insight:**
This source fills the **skills gap** that Ned identified in his career video: universities teach finance careers and concepts but not the practical technical skills. Financial modeling is used across all finance roles — investment banking, corporate finance, PE, VC. This source provides the foundational knowledge.

**Connections:**
- Links financial modeling to [[ma-analyst|M&A analyst]] and [[private-equity-analyst|PE analyst]] roles
- Explains the technical foundations of [[corporate-finance|corporate finance]], [[investment-banking|investment banking]]
- Validates [[ned-finance-careers|Ned's]] emphasis on practical skills

**Wiki Growth:**
- Total pages: 45 (up from 27)
- Sources: 3
- Entities: 8
- Concepts: 22
