---
type: concept
name: Wiki curated layer
sources: 1
last_updated: 2026-04-27
---

# Wiki curated layer

> *The second layer of the [[karpathy-llm-wiki]]: a directory of LLM-owned, interlinked markdown pages — summaries, entity pages, concept pages, comparisons — kept current as new sources arrive.*

## What it means

The `wiki/` directory is where the synthesis lives. Entity pages (vendors, concepts, sectors, sources, people, firms in this vault) are written and updated by the LLM, never by the user. Each page accumulates citations across sources and gets denser without anyone being told to refresh it. The cross-references that make a knowledge base actually useful — wiki-links between concepts, vendors, and the sources that cite them — are maintained automatically.

The user reads this layer; the LLM writes it. Karpathy's framing: "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "The wiki — a directory of LLM-generated markdown files… The LLM owns this layer entirely. It creates pages, updates them when new sources arrive, maintains cross-references, and keeps everything consistent. You read it; the LLM writes it."

## Mechanism / how it works

The LLM's discipline over this layer comes from the schema (see [[schema-as-program]]). The schema names the entity types, their folders, their slug rules, and their frontmatter shapes. When ingesting a new source, the LLM creates or updates pages within those constraints; when running [[ingest-query-lint-operations|lint]], it enforces them.

A single source ingest typically touches 10–15 pages — the source page itself, plus the entity pages (vendors / concepts / sectors / people / firms) the source cites. This many-page cascade is what compounds the substrate: each new source gets integrated with everything that came before.

The user is responsible for source curation, the calibration questions, and direction of analysis. The LLM is responsible for everything else: summarization, cross-referencing, filing, and bookkeeping.

## Related concepts

- [[raw-immutable-layer]] — what this layer reads from.
- [[schema-as-program]] — the discipline mechanism.
- [[ingest-query-lint-operations]] — the three operations through which this layer evolves.
- [[self-improving-substrate]] — the property that compounds across ingests.
- [[karpathy-llm-wiki]] — parent pattern.

## Related vendors / sectors

_(pre-domain)_

## Open questions

- Where does the boundary lie between an entity-page update and a new entity page? The Karpathy gist leaves this to the schema; this vault's CLAUDE.md sets the bar at "substantive treatment in a single source, OR mention in 2+ sources" before promoting a passing reference into its own page.

## Sources cited

- [[karpathy-llm-wiki-gist]]
