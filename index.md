# Index

This file is maintained by Claude Code. It catalogs every wiki page with a one-line summary, organized by entity type. Read this first when answering a query to scope the search.

> Counts in parentheses are page counts in that section.

## Vendors (1)

- [[circle]] — centralized US- and EUR-pegged stablecoin issuer (USDC, EURC); 1:1 redemption guarantee with majority of reserves in the SEC-registered 2a-7 Circle Reserve Fund (USDXX) managed by BlackRock; weekly + monthly disclosure cadence with Deloitte attestation since fiscal 2022; reporting history since 2018; NYDFS + BMA licensed; MiCA registration status not surfaced on transparency page.

## Concepts (17)

- [[karpathy-llm-wiki]] — the meta-pattern: a persistent, structured, LLM-maintained wiki that compiles knowledge once and keeps it current.
- [[raw-immutable-layer]] — first layer: curated source documents the LLM only reads from, never modifies.
- [[wiki-curated-layer]] — second layer: LLM-owned interlinked markdown pages updated as new sources arrive.
- [[schema-as-program]] — third layer: the schema file (`CLAUDE.md`) treated as the program the LLM executes.
- [[ingest-query-lint-operations]] — the three operations against the substrate: ingest a source, query the wiki, lint for drift.
- [[self-improving-substrate]] — compounding property: maintenance cost approaches zero, so the wiki gets richer with each ingest.
- [[citation-discipline]] — structural property: every claim wiki-links to a source page; for institutional buyers, citation and licensing-clean output are the same property. (3 sources)
- [[institutional-digital-asset-buyer]] — the audience this wiki's domain template is designed to serve: consulting & advisory, corporate strategy, foundations & ecosystems, institutional allocators.
- [[retail-grade-intelligence-gap]] — the structural mismatch in which institutional digital-asset decisions get made on tools built for retail traders, VC dealflow, generic enterprise market research, or on-chain analytics.
- [[counterparty-graph-research]] — research pattern: traverse a vendor's named regulators, settlement partners, integration partners as a graph rather than read in isolation.
- [[mica-compliance]] — the EU regulatory frame for crypto-assets (Regulation (EU) 2023/1114); four categories: ART, EMT, "other crypto-assets," CASPs; transitional period under Article 143 ends 1 July 2026.
- [[asset-referenced-token]] — MiCA Title III: tokens referencing baskets, commodities, multiple fiat currencies, or other crypto-assets.
- [[e-money-token]] — MiCA Title IV: tokens referencing a single official currency (USD-pegged, EUR-pegged stablecoins). Circle's USDC and EURC are EMT-archetype. (2 sources)
- [[crypto-asset-service-provider]] — MiCA Title V: entities providing custody, exchange, transfer, execution, advice, portfolio management, or placement on crypto-assets in the EU.
- [[crypto-asset-white-paper]] — MiCA disclosure primitive; iXBRL machine-readable from 23 December 2025; ESMA does NOT review or approve content.
- [[proof-of-reserves]] — the structural transparency primitive for centrally-issued stablecoins: weekly self-published + monthly third-party attestation + (where strong) regulator-grounded reserve vehicle.
- [[2a-7-government-money-market-fund]] — US-securities-law primitive: SEC-registered MMF restricted to government securities; used by Circle as the reserve-vehicle grounding for USDXX.

## Sectors (4)

- [[stablecoin-issuers]] — vendors issuing digital tokens designed to maintain stable value relative to a reference asset; institutional-buyer question is which issuer to trust as a counterparty. (3 sources, 1 vendor: Circle)
- [[custody]] — vendors holding digital assets for institutional clients; typically the most regulation-heavy sector. (2 sources)
- [[regulatory-and-compliance]] — vendors providing compliance, sanctions-screening, transaction-monitoring tooling; sit between operators and regulators. (2 sources)
- [[payment-and-settlement]] — vendors operating digital-asset rails for moving value between institutions: exchanges, on/off-ramps, settlement networks, card programs, remittance corridors. (2 sources)

## Sources (4)

- [[karpathy-llm-wiki-gist]] — Andrej Karpathy, GitHub Gist (2025). The canonical statement of the LLM Wiki pattern.
- [[51-deck-april-2026]] — Marc Baumann / Fiftyone Group LLC, public April 2026 deck. Audience-framing source only (Path A — no reproduction of 51 product internals).
- [[regulator-eu-mica-esma-hub]] — ESMA MiCA hub. The EU regulatory frame for crypto-asset markets.
- [[vendor-circle-transparency-page-2026-04]] — Circle's public transparency page. Articulates the 1:1 redemption guarantee, USDXX 2a-7 MMF reserve vehicle, two-tier disclosure cadence, Deloitte audit relationship, NYDFS + BMA licenses.

## People (2)

- [[andrej-karpathy]] — author of the LLM Wiki gist; anchor-only page in this wiki.
- [[marc-baumann]] — Founder, 51 Group; author of the public 51 Terminal April deck used as audience-framing.

## Firms (5)

- [[fiftyone-group-llc]] — publisher of the public 51 Terminal April deck; operator of the 51 Terminal product (proprietary product output is out-of-scope for this Path A wiki).
- [[esma]] — European Securities and Markets Authority; EU-level coordinator of MiCA; keeper of the interim MiCA register.
- [[european-commission]] — proposer of MiCA; anchor-only.
- [[blackrock]] — manager of the Circle Reserve Fund (USDXX), the SEC-registered 2a-7 government money market fund holding the majority of USDC reserves.
- [[deloitte]] — Big Four; Circle's independent auditor since fiscal 2022; performs monthly USDC reserve attestations under AICPA standards.
