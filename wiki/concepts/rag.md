---
title: "Retrieval-Augmented Generation (RAG)"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [llm, architecture, retrieval, baseline]
sources: [karpathy-llm-wiki]
status: draft
---

# Retrieval-Augmented Generation (RAG)

## Definition

A pattern where an LLM retrieves relevant chunks from a document collection at query time and generates an answer based on those chunks. The dominant approach for connecting LLMs to external knowledge.

## Explanation

In a RAG system, documents are split into chunks, embedded into vectors, and stored in a vector database. When a user asks a question, the system retrieves the most relevant chunks, feeds them to the LLM as context, and the LLM generates an answer. Products like NotebookLM, ChatGPT file uploads, and most enterprise AI systems work this way.

The limitation: every query starts from scratch. The LLM rediscovers knowledge on every question. There's no accumulation, no synthesis across sources, no persistent structure. Ask a question requiring five documents and the LLM has to find and piece them together every time.

The [[llm-wiki-pattern]] addresses this by having the LLM compile knowledge into a persistent wiki rather than re-deriving it at query time. See [[compiled-knowledge]] for the core distinction.

## Examples

- NotebookLM
- ChatGPT file uploads
- Enterprise RAG pipelines (LangChain, LlamaIndex, etc.)

## Related Concepts

- [[llm-wiki-pattern]] — the alternative approach
- [[compiled-knowledge]] — the key distinction: compiled vs. re-derived

## Sources

- [[karpathy-llm-wiki]] — positions RAG as the baseline the LLM Wiki pattern improves upon

## Open Questions

- RAG and compiled knowledge aren't mutually exclusive — could a hybrid approach work? (e.g., wiki for core knowledge, RAG for long-tail queries)
- At what scale does RAG outperform index-based navigation?
