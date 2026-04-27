---
type: source
name: LLM Wiki
source_url: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
publication: GitHub Gist (karpathy)
author: Andrej Karpathy
published: 2025-12 (gist last-modified — original publication date)
ingested: 2026-04-27
paywalled: false
---

# LLM Wiki

> _Source: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f_

## Summary

Karpathy's gist describes a pattern for personal knowledge bases in which an LLM agent **incrementally builds and maintains a structured wiki** sitting between the user and the raw source documents. The pattern contrasts itself explicitly with conventional RAG: rather than retrieve fragments from raw sources at query time and re-derive synthesis on every question, the LLM compiles knowledge once into interlinked markdown pages and keeps them current as new sources arrive. The result is "a persistent, compounding artifact" — cross-references already in place, contradictions already flagged, synthesis reflecting everything ingested.

The architecture has three layers: `raw/` (immutable inputs the LLM only reads), `wiki/` (markdown pages the LLM owns and updates), and a schema file (e.g. `CLAUDE.md` for Claude Code or `AGENTS.md` for Codex) that tells the LLM how the wiki is structured and what conventions to follow. The schema is what makes the LLM "a disciplined wiki maintainer rather than a generic chatbot," and the human and LLM co-evolve it as they figure out what works.

Three operations run against the wiki: **ingest** (read source → discuss takeaways → write/update pages → update index + log), **query** (read index to scope → drill into pages → return cited synthesis, with the option to file good answers back as new pages), and **lint** (health-check for contradictions, orphans, stale claims, missing concepts, missing cross-references). Two navigational primitives — `index.md` (content-oriented catalog) and `log.md` (append-only chronological journal) — replace the need for embedding-based RAG infrastructure at moderate scale (~100 sources, hundreds of pages).

Karpathy frames the labor division explicitly: the human curates sources, asks questions, and thinks; the LLM does the bookkeeping (cross-references, summary refresh, consistency maintenance) that has historically killed human-maintained wikis. The cost of maintenance approaches zero, so the wiki keeps getting richer instead of decaying. He places this in the lineage of Vannevar Bush's 1945 Memex — "a personal, curated knowledge store with associative trails between documents" — and notes the part Bush couldn't solve was who does the maintenance.

The gist is intentionally abstract: it communicates the pattern, leaves implementation specifics (directory layout, schema conventions, page formats, tooling) to the user and their LLM agent to instantiate together for the user's domain.

## Key claims

1. **The wiki is a persistent, compounding artifact, not a query-time retrieval cache.** — > "the wiki is a persistent, compounding artifact. The cross-references are already there. The contradictions have already been flagged. The synthesis already reflects everything you've read."
2. **Three-layer architecture: raw / wiki / schema.** — > "There are three layers: Raw sources… The wiki… The schema."
3. **The schema makes the LLM disciplined.** — > "This is the key configuration file — it's what makes the LLM a disciplined wiki maintainer rather than a generic chatbot."
4. **Three operations: ingest, query, lint.** — > "Ingest. You drop a new source into the raw collection… Query. You ask questions against the wiki… Lint. Periodically, ask the LLM to health-check the wiki."
5. **At moderate scale, index + log replace embedding-based RAG.** — > "This works surprisingly well at moderate scale (~100 sources, ~hundreds of pages) and avoids the need for embedding-based RAG infrastructure."
6. **Maintenance is the work, and the LLM does it for free.** — > "Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass."
7. **Good query answers can be filed back as new wiki pages.** — > "good answers can be filed back into the wiki as new pages."

## Concepts cited

- [[karpathy-llm-wiki]] — the meta-pattern this gist defines.
- [[raw-immutable-layer]] — the source-of-truth layer the LLM only reads from.
- [[wiki-curated-layer]] — the LLM-owned interlinked-markdown layer.
- [[schema-as-program]] — the schema file (`CLAUDE.md`) treated as the program the LLM executes.
- [[ingest-query-lint-operations]] — the three operations that run against the wiki.
- [[self-improving-substrate]] — the property that maintenance cost approaches zero, so the wiki keeps compounding.
- [[citation-discipline]] — every claim wiki-links to a source page; query answers carry citations.

## Vendors discussed

_(none — the gist is pattern-level, not domain-specific)_

## Sectors touched

_(none — pre-domain)_

## Notable quotes

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping."

> "The idea is related in spirit to Vannevar Bush's Memex (1945) — a personal, curated knowledge store with associative trails between documents. … The part he couldn't solve was who does the maintenance. The LLM handles that."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## Open questions raised

- The pattern explicitly leaves "implementation specifics … to depend on your domain." For digital-asset vendor research, what does that translate to concretely — entity types, frontmatter shapes, slug rules? (Answered structurally by this vault's `CLAUDE.md` schema; lived-experience answer accumulates with each ingest.)
- At what corpus size does the index-only navigation approach break down and require a search tool like `qmd`?
- The gist mentions filing good query answers back into the wiki — under what conditions does that warrant a new entity page vs. an append to an existing one?

## External references

- Tolkien Gateway (https://tolkiengateway.net/wiki/Main_Page) — cited as an example of a community-built fan wiki demonstrating depth via interlinks.
- `qmd` (https://github.com/tobi/qmd) — local search engine for markdown files; cited as an optional CLI/MCP tool for larger wikis.
- Vannevar Bush, Memex (1945) — cited as the conceptual ancestor.

## Cross-references

_(none yet — this is the first source in the vault)_
