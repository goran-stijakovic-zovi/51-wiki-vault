# Index

This file is maintained by Claude Code. It catalogs every wiki page with a one-line summary, organized by entity type. Read this first when answering a query to scope the search.

> Counts in parentheses are page counts in that section.

## Vendors (0)

_(none yet — populated by ingest)_

## Concepts (15)

- [[karpathy-llm-wiki]] — the meta-pattern: a persistent, structured, LLM-maintained wiki that compiles knowledge once and keeps it current.
- [[raw-immutable-layer]] — first layer: curated source documents the LLM only reads from, never modifies.
- [[wiki-curated-layer]] — second layer: LLM-owned interlinked markdown pages updated as new sources arrive.
- [[schema-as-program]] — third layer: the schema file (`CLAUDE.md`) treated as the program the LLM executes.
- [[ingest-query-lint-operations]] — the three operations against the substrate: ingest a source, query the wiki, lint for drift.
- [[self-improving-substrate]] — compounding property: maintenance cost approaches zero, so the wiki gets richer with each ingest.
- [[citation-discipline]] — structural property: every claim wiki-links to a source page; for institutional buyers, citation and licensing-clean output are the same property. (2 sources)
- [[institutional-digital-asset-buyer]] — the audience this wiki's domain template is designed to serve: consulting & advisory, corporate strategy, foundations & ecosystems, institutional allocators.
- [[retail-grade-intelligence-gap]] — the structural mismatch in which institutional digital-asset decisions get made on tools built for retail traders, VC dealflow, generic enterprise market research, or on-chain analytics.
- [[counterparty-graph-research]] — research pattern: traverse a vendor's named regulators, settlement partners, integration partners as a graph rather than read in isolation.
- [[mica-compliance]] — the EU regulatory frame for crypto-assets (Regulation (EU) 2023/1114); four categories: ART, EMT, "other crypto-assets," CASPs; transitional period under Article 143 ends 1 July 2026.
- [[asset-referenced-token]] — MiCA Title III: tokens referencing baskets, commodities, multiple fiat currencies, or other crypto-assets.
- [[e-money-token]] — MiCA Title IV: tokens referencing a single official currency (USD-pegged, EUR-pegged stablecoins).
- [[crypto-asset-service-provider]] — MiCA Title V: entities providing custody, exchange, transfer, execution, advice, portfolio management, or placement on crypto-assets in the EU.
- [[crypto-asset-white-paper]] — MiCA disclosure primitive; iXBRL machine-readable from 23 December 2025; ESMA does NOT review or approve content.

## Sectors (4)

- [[stablecoin-issuers]] — vendors issuing digital tokens designed to maintain stable value relative to a reference asset; institutional-buyer question is which issuer to trust as a counterparty. (2 sources — deck + ESMA MiCA)
- [[custody]] — vendors holding digital assets for institutional clients; typically the most regulation-heavy sector. (2 sources)
- [[regulatory-and-compliance]] — vendors providing compliance, sanctions-screening, transaction-monitoring tooling; sit between operators and regulators. (2 sources)
- [[payment-and-settlement]] — vendors operating digital-asset rails for moving value between institutions: exchanges, on/off-ramps, settlement networks, card programs, remittance corridors. (2 sources)

## Sources (3)

- [[karpathy-llm-wiki-gist]] — Andrej Karpathy, GitHub Gist (2025). The canonical statement of the LLM Wiki pattern.
- [[51-deck-april-2026]] — Marc Baumann / Fiftyone Group LLC, public April 2026 deck. Audience-framing source only (Path A — no reproduction of 51 product internals).
- [[regulator-eu-mica-esma-hub]] — ESMA MiCA hub. The EU regulatory frame for crypto-asset markets.

## People (2)

- [[andrej-karpathy]] — author of the LLM Wiki gist; anchor-only page in this wiki.
- [[marc-baumann]] — Founder, 51 Group; author of the public 51 Terminal April deck used as audience-framing.

## Firms (3)

- [[fiftyone-group-llc]] — publisher of the public 51 Terminal April deck; operator of the 51 Terminal product (proprietary product output is out-of-scope for this Path A wiki).
- [[esma]] — European Securities and Markets Authority; EU-level coordinator of MiCA; keeper of the interim MiCA register.
- [[european-commission]] — proposer of MiCA; anchor-only.
