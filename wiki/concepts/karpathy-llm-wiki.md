---
type: concept
name: Karpathy LLM Wiki
sources: 1
last_updated: 2026-04-27
---

# Karpathy LLM Wiki

> *A pattern for personal knowledge bases in which an LLM agent incrementally builds and maintains a structured, interlinked wiki sitting between the user and the raw sources.*

## What it means

A Karpathy LLM Wiki is **not** a retrieval-augmented chat over a pile of files. It is a persistent, structured artifact that the LLM compiles once and keeps current — a directory of interlinked markdown pages organized by entity type, with cross-references, contradictions flagged, and a schema file that tells the LLM how to maintain it. The user curates sources and asks questions; the LLM does all the bookkeeping.

The pattern is deliberately abstract — it specifies a shape (three layers, three operations) and leaves implementation specifics (directory layout, frontmatter, slug rules, page formats) to be co-evolved between the user and the LLM agent for the user's domain.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — the canonical statement of the pattern. Defines the three layers, three operations, and the principle that the wiki is "a persistent, compounding artifact."

## Mechanism / how it works

The pattern has three structural elements:

1. **A three-layer architecture** — see [[raw-immutable-layer]], [[wiki-curated-layer]], [[schema-as-program]].
2. **Three operations** — see [[ingest-query-lint-operations]].
3. **Two navigational primitives** — `index.md` (content-oriented catalog) and `log.md` (append-only chronological journal). At moderate scale (~100 sources, hundreds of pages) these replace the need for embedding-based RAG.

The compounding behavior comes from a fourth, derived property: maintenance cost approaches zero (the LLM does the bookkeeping that historically killed human-maintained wikis), so the substrate gets structurally richer with every ingest rather than decaying. See [[self-improving-substrate]].

## Related concepts

- [[raw-immutable-layer]] — first of the three layers.
- [[wiki-curated-layer]] — second of the three layers.
- [[schema-as-program]] — third of the three layers; the discipline mechanism.
- [[ingest-query-lint-operations]] — the operational surface.
- [[self-improving-substrate]] — the compounding property derived from near-zero maintenance cost.
- [[citation-discipline]] — the structural property that makes query answers defensible.

## Related vendors / sectors

_(this concept is pre-domain — it does not yet wiki-link to specific vendors or sectors. The whole point of this vault is to instantiate the pattern in the digital-asset vendor research domain; that instantiation appears across every vendor / sector / source page.)_

## Open questions

- At what corpus size does index-only navigation break down? Karpathy cites "moderate scale (~100 sources, ~hundreds of pages)" as the regime where this works without a search tool.
- For domains with proprietary mixed-source corpora (e.g. 51 Terminal's audit-context research), how does the pattern adapt to enforce citation-and-licensing discipline structurally? (This vault's Path A licensing posture is one answer.)

## Sources cited

- [[karpathy-llm-wiki-gist]]
