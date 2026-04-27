---
type: concept
name: Schema as program
sources: 1
last_updated: 2026-04-27
---

# Schema as program

> *The third layer of the [[karpathy-llm-wiki]]: a schema file (e.g. `CLAUDE.md`) treated as the program that turns the LLM into "a disciplined wiki maintainer rather than a generic chatbot."*

## What it means

The schema names the entity types, the folders, the slug conventions, the frontmatter shapes, the operations, and the don'ts. It is loaded into the LLM's context at the start of every session and treated as authoritative — the LLM follows it the way an interpreter follows source code.

The schema is the lever that makes the difference between a wiki that stays consistent and a wiki that drifts. Without a schema, an LLM will improvise structure differently every session; with one, the structure becomes a stable contract.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "The schema — a document (e.g. CLAUDE.md for Claude Code or AGENTS.md for Codex) that tells the LLM how the wiki is structured… This is the key configuration file — it's what makes the LLM a disciplined wiki maintainer rather than a generic chatbot."

## Mechanism / how it works

The schema in this vault (`/Users/gstijakovic/Dev/Projects/51-wiki/Obsidian-vault/51-wiki-vault/CLAUDE.md`) does six things:

1. Names the **layers** (raw / wiki / index / log).
2. Declares the **domain** and the audience.
3. Lists the **entity types** in priority order with their folders.
4. Specifies **naming conventions** (slug rules per type, frontmatter fields).
5. Defines the three **operations** (ingest / query / lint) as numbered procedures.
6. Lists the **don'ts** — what the LLM must not do (here: ingest from `terminal.fiftyone.xyz`, reproduce 51 product output, ingest Goran-authored audit writing — see [[citation-discipline]] for the structural angle).

The schema **co-evolves** with the corpus. After ~4 seed ingests, the LLM is expected to propose a schema diff based on what worked — new entity types if needed, refined slug rules, additional frontmatter fields. This is "schema iteration" (Phase 8 of the `onboard-wiki` skill), and it is the mechanism by which the schema itself improves with corpus contact.

## Related concepts

- [[raw-immutable-layer]] — declared by the schema.
- [[wiki-curated-layer]] — disciplined by the schema.
- [[karpathy-llm-wiki]] — parent pattern.
- [[ingest-query-lint-operations]] — defined by the schema.

## Related vendors / sectors

_(pre-domain)_

## Open questions

- How aggressively should the schema be iterated? Frequent diffs risk schema-corpus skew (older pages drift from newer rules); rare diffs risk locking in early mistakes. The `onboard-wiki` workflow's heuristic — propose a diff after ~4 seed ingests, then again after the first ~12 — has not yet been pressure-tested across many domains.
- Should the schema live in the repo root, in `_meta/`, or in a frontmatter field on `index.md`? Karpathy's gist puts it at the root; this vault follows that convention.

## Sources cited

- [[karpathy-llm-wiki-gist]]
