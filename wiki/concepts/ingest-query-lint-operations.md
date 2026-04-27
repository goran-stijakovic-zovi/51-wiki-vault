---
type: concept
name: Ingest, query, lint operations
sources: 1
last_updated: 2026-04-27
---

# Ingest, query, lint operations

> *The three operations a [[karpathy-llm-wiki]] supports against its substrate: ingest a new source, query the substrate, lint it for drift.*

## What it means

The wiki is not a passive document store — it is a substrate with a small operational surface. Three operations run against it:

- **Ingest**: read a raw source, discuss takeaways with the user, write a source page, update or create relevant entity pages, update `index.md`, append to `log.md`. A single ingest can touch 10–15 pages.
- **Query**: read `index.md` first to scope, drill into relevant pages, follow wiki-links, return a synthesized answer with citations to specific wiki pages. Good answers can be filed back as new wiki pages so explorations compound alongside ingested sources.
- **Lint**: health-check the substrate. Find contradictions, orphan pages, concepts mentioned in 3+ pages without their own page, stale claims (`last_updated` > 90 days AND newer sources contradict). Write findings to a dated lint file; propose changes; wait for approval before applying.

These three operations are the entire surface area the user interacts with. Together with the schema (see [[schema-as-program]]), they make the LLM a disciplined maintainer.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "Ingest. You drop a new source into the raw collection… Query. You ask questions against the wiki… Lint. Periodically, ask the LLM to health-check the wiki."

## Mechanism / how it works

Each operation has a procedural definition in the schema (see this vault's `CLAUDE.md`). The procedures are:

**Ingest** — interactive: read raw → propose 3–5 takeaways and entity classifications → wait for user's "go" → write source page + entity pages → update index + log → commit → brief report.

**Query** — read index → follow links → synthesize cited answer → optionally offer to file the answer as a new page. Append a log entry summarizing the query.

**Lint** — scan the wiki for the standard drift patterns; write findings to `wiki/_lint-<YYYY-MM-DD>.md`; do not auto-fix. Lint is the closest the pattern gets to an automated eval suite.

The interactivity of ingest is structural, not optional. The "discuss takeaways → go → write" gate is what keeps the substrate aligned with the user's intent and prevents the LLM from over-fragmenting (creating a concept page from every passing mention). It also surfaces calibration questions early, which feed schema iteration (see [[schema-as-program]]).

## Related concepts

- [[karpathy-llm-wiki]] — parent pattern.
- [[schema-as-program]] — defines the operational procedures.
- [[wiki-curated-layer]] — what these operations write to.
- [[citation-discipline]] — the structural property query answers carry forward.
- [[self-improving-substrate]] — the compounding effect of running ingest repeatedly.

## Related vendors / sectors

_(pre-domain — these operations apply to any domain instantiation)_

## Open questions

- Lint is described in the gist as "primitive" — at what corpus size does it warrant a dedicated automated tool (cron + scripted checks) rather than an interactive operation invoked on demand?
- The "file good answers back as wiki pages" branch of the query operation creates a class of synthetic pages distinct from ingested-source pages. How should they be flagged in frontmatter (e.g. `synthetic: true`) and treated by future lint passes?

## Sources cited

- [[karpathy-llm-wiki-gist]]
