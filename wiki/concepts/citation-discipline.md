---
type: concept
name: Citation discipline
sources: 3
last_updated: 2026-04-27
---

# Citation discipline

> *The structural property that every claim on a wiki page is wiki-linked to its source page, and every query answer carries citations because the substrate makes it the path of least resistance.*

## What it means

In a [[karpathy-llm-wiki]], citation is not a behavioral target the LLM is asked to hit — it is a structural property of the data layer. Every claim on an entity page wiki-links to a source page. Every query reads index, drills into pages, and returns an answer that quotes wiki-linked sources by construction. The LLM is not "told to cite"; citing is the cheapest way to assemble the answer.

This is the property that makes a wiki's outputs *defensible* to institutional buyers. A claim without a source link is visible as unsupported. A query answer without citations is a structural anomaly, not a behavioral lapse.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "When you ask questions against the wiki… The LLM searches for relevant pages, reads them, and synthesizes an answer with citations." The pattern treats citation as a default, not an option.
- [[51-deck-april-2026]] — Slide 4 lists "non-existent or poor-quality data" and "no licenses for external data use" as canonical status-quo failures of generic intelligence platforms. Slide 11 places "client deliverable licensing" as a capability axis. Together these establish that for an institutional-buyer audience, **citation discipline and licensing-clean output are the same property** — claims must be sourced *and* the sources must be redistributable.
- [[vendor-circle-transparency-page-2026-04]] — Circle's two-tier disclosure regime (weekly self-published holdings + monthly third-party Deloitte attestation under AICPA standards) is a real-world institutional implementation of structural citation discipline at the issuer layer. The reserve-vehicle grounding (the [[2a-7-government-money-market-fund|SEC-registered 2a-7 Circle Reserve Fund]] managed by [[blackrock]] with daily public portfolio reporting) adds a third structural-citation layer on top of the issuer's own.

## Mechanism / how it works

Citation becomes structural through three reinforcing rules:

1. **Wiki-link first, body second.** The schema's "every page starts with frontmatter, then prose" convention combines with the rule that wiki-links are mandatory for first-mentions of named entities. This forces the LLM to ground each claim before writing the surrounding paragraph.
2. **Source pages are first-class citizens.** Every ingested source gets its own page with verbatim Key Claims and Notable Quotes. Other pages link to the source, not to a URL or a free-text reference.
3. **Query operation reads index → pages → answer.** The query path *cannot* return text without traversing source pages, so citations are the natural output format.

In a domain like institutional research, this property is the difference between "the system claims X" and "the system claims X, with the verbatim quote sourced from [[karpathy-llm-wiki-gist]] in the wiki's source layer." The latter is auditable; the former is a hallucination risk.

The 51 deck adds a fourth layer specific to institutional buyers: **licensing-clean output**. A consulting firm assembling a client deliverable cannot redistribute analysis derived from data it has no license to redistribute. The wiki-pattern substrate addresses this by being explicit about the licensing posture of every source page (this vault is Path A — public sources only). A future fork of this template, ingesting contracted proprietary sources for internal use, would tag those source pages differently and gate redistribution at the schema level.

## Related concepts

- [[karpathy-llm-wiki]] — the pattern that makes citation structural.
- [[ingest-query-lint-operations]] — query is where citation discipline pays off.
- [[wiki-curated-layer]] — where the wiki-links live.
- [[schema-as-program]] — encodes the wiki-link discipline as a rule.
- [[self-improving-substrate]] — citation discipline is one of the five compounding mechanisms.

## Related vendors / sectors

_(pre-domain — but worth noting that this is the property that maps directly to the audit context's Layer 4 finding from `/Users/gstijakovic/Dev/Projects/51/51-llm-wiki-plan.md`: institutional buyers need citable answers; substrate-level citation discipline is the architecture proof for that requirement.)_

## Open questions

- How rigid should the no-bare-URL rule be? Karpathy's gist allows external references in source pages; this vault's schema enforces wiki-links in body prose but allows raw URLs in dedicated `## External references` sections.
- For domains with ephemeral sources (Slack threads, podcast clips), what's the equivalent of a stable wiki-link? Frozen quotes plus a fetched-on date? A locally archived transcript file?

## Sources cited

- [[karpathy-llm-wiki-gist]]
- [[51-deck-april-2026]]
- [[vendor-circle-transparency-page-2026-04]]
