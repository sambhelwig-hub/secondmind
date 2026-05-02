# LLM Wiki — Schema & Operating Manual

> This file tells the LLM how to maintain this wiki. It is the single source of truth for structure, conventions, and workflows. Co-evolve it with the wiki as your needs change.

## Overview

This is a personal knowledge base maintained by an LLM. The human curates sources, directs analysis, and asks questions. The LLM does everything else: summarizing, cross-referencing, filing, updating, and maintaining consistency across the wiki.

## Directory Structure

```
llm-wiki/
├── CLAUDE.md              ← You are here. Schema & operating manual.
├── raw/                   ← Immutable source documents. LLM reads, never writes.
│   ├── assets/            ← Downloaded images, PDFs, attachments.
│   └── *.md               ← Clipped articles, notes, transcripts, etc.
├── wiki/                  ← LLM-generated & maintained markdown pages.
│   ├── index.md           ← Master catalog of all wiki pages.
│   ├── log.md             ← Chronological record of all operations.
│   ├── overview.md        ← High-level synthesis of everything in the wiki.
│   ├── sources/           ← One summary page per ingested source.
│   ├── entities/          ← Pages for people, projects, tools, organizations.
│   ├── concepts/          ← Pages for ideas, patterns, frameworks, terms.
│   ├── comparisons/       ← Side-by-side analyses (X vs Y).
│   └── analyses/          ← Filed query results, deep dives, syntheses.
└── templates/             ← Page templates for consistent structure.
    ├── source.md
    ├── entity.md
    ├── concept.md
    ├── comparison.md
    └── analysis.md
```

## Page Conventions

### Frontmatter

Every wiki page MUST have YAML frontmatter:

```yaml
---
title: Page Title
type: source | entity | concept | comparison | analysis | overview
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [tag1, tag2]
sources: [source-slug-1, source-slug-2]   # which raw sources inform this page
status: stub | draft | complete
---
```

### File Naming

- Use kebab-case: `vannevar-bush.md`, `rag-vs-compiled-knowledge.md`
- Source pages mirror the source filename: if raw source is `karpathy-llm-wiki.md`, wiki source page is `sources/karpathy-llm-wiki.md`
- Keep names short but unambiguous.

### Internal Links

- Use Obsidian wikilinks: `[[page-name]]` or `[[page-name|Display Text]]`
- Always link to entities and concepts on first mention in any page.
- Cross-reference liberally. Links are the connective tissue of the wiki.

### Sections

Pages should use consistent H2 sections. See templates for the canonical structure of each page type.

## Workflows

### 1. Ingest

Triggered when: the human adds a new source to `raw/` and asks the LLM to process it.

Steps:
1. **Read** the raw source completely.
2. **Discuss** key takeaways with the human. Ask what to emphasize.
3. **Create source page** in `wiki/sources/` using the source template.
4. **Identify entities** mentioned. For each:
   - If entity page exists → update it with new information, cite the source.
   - If entity page doesn't exist → create it using the entity template.
5. **Identify concepts** discussed. For each:
   - If concept page exists → update it, add new perspectives or evidence.
   - If concept page doesn't exist → create it using the concept template.
6. **Update `wiki/overview.md`** if the source materially changes the big picture.
7. **Update `wiki/index.md`** — add entries for all new pages.
8. **Append to `wiki/log.md`** — record what was ingested and what pages were created/updated.
9. **Report** to the human: summary of changes, list of pages touched, any contradictions or gaps found.

### 2. Query

Triggered when: the human asks a question.

Steps:
1. **Read `wiki/index.md`** to find relevant pages.
2. **Read relevant pages** and synthesize an answer.
3. **Cite sources** using wikilinks to wiki pages.
4. **Optionally file the answer** as a new page in `wiki/analyses/` or `wiki/comparisons/` if it has lasting value. Ask the human.
5. **Update index and log** if a new page was created.

### 3. Lint

Triggered when: the human asks for a health check, or periodically after every ~10 ingests.

Checks:
- **Contradictions**: pages that make conflicting claims.
- **Stale content**: claims that newer sources have superseded.
- **Orphan pages**: pages with no inbound links.
- **Missing pages**: entities or concepts mentioned but lacking their own page.
- **Missing cross-references**: pages that should link to each other but don't.
- **Data gaps**: questions the wiki can't answer well; suggest sources to find.
- **Index drift**: pages that exist on disk but aren't in the index (or vice versa).

Output: a lint report as a message to the human, with suggested fixes. Apply fixes after human approval.

## Principles

1. **The wiki is the product.** Chat is ephemeral; the wiki persists. Always ask: should this be filed?
2. **Compound, don't repeat.** Every ingest should make the wiki richer, not just bigger. Update existing pages; don't create duplicates.
3. **Link aggressively.** An unlinked page is a lost page. Every page should have inbound and outbound links.
4. **Cite everything.** Every claim in the wiki should trace back to a source page, which traces back to a raw source.
5. **Flag contradictions.** Don't silently overwrite. Note when new data conflicts with old and let the human decide.
6. **Prefer depth to breadth.** A few well-developed pages are more useful than many stubs.
7. **The human decides emphasis.** The LLM proposes; the human disposes. Always check before making major structural changes.

## Dataview Compatibility

Frontmatter is designed to work with Obsidian's Dataview plugin. Example queries:

```dataview
TABLE status, updated, length(sources) AS "Source Count"
FROM "wiki"
WHERE type = "concept"
SORT updated DESC
```

```dataview
LIST
FROM "wiki/sources"
WHERE contains(tags, "ai")
SORT created DESC
```

## Evolution

This schema is a living document. After every few sessions, review it together:
- Are the page types sufficient? Do you need new ones?
- Are the workflows working? What's friction?
- Are the conventions clear? What needs clarifying?
- What tools would help? Search, automation, visualization?

Update this file to reflect what you've learned.
