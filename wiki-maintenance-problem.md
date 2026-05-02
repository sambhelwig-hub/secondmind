---
title: "Wiki Maintenance Problem"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [core-insight, knowledge-management, failure-mode]
sources: [karpathy-llm-wiki]
status: draft
---

# Wiki Maintenance Problem

## Definition

The phenomenon where human-maintained wikis and knowledge bases are abandoned because the maintenance burden grows faster than the value they provide.

## Explanation

The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping: updating cross-references, keeping summaries current, noting contradictions, maintaining consistency across pages. As a wiki grows, the number of pages that need updating on each new addition grows too. Eventually the cost of maintenance exceeds the human's willingness to do it, and the wiki stagnates or dies.

This is why the [[llm-wiki-pattern]] works: LLMs eliminate the maintenance constraint. They don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass. The maintenance cost drops to near zero, so the wiki can compound indefinitely.

This was also the unsolved piece of [[vannevar-bush|Bush's]] [[memex]] vision — who builds and maintains the associative trails?

## Examples

- Corporate wikis that start strong and decay within months as no one updates them.
- Personal note-taking systems (Notion, Roam, Obsidian) that become graveyards of unlinked, stale notes.
- Fan wikis that survive only because they have dedicated volunteer communities doing constant maintenance.

## Related Concepts

- [[llm-wiki-pattern]] — the solution
- [[memex]] — the historical antecedent with the same unsolved problem
- [[compiled-knowledge]] — the compilation step is where maintenance happens

## Sources

- [[karpathy-llm-wiki]]

## Open Questions

- Are there categories of maintenance that LLMs still do poorly? (e.g., subjective editorial judgment, resolving genuine ambiguity)
- Does the pattern introduce new failure modes — e.g., LLM drift, hallucinated cross-references?
