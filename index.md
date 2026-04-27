# Index

This file is maintained by Claude Code. It catalogs every wiki page with a one-line summary, organized by entity type. Read this first when answering a query to scope the search.

> Counts in parentheses are page counts in that section.

## Vendors (4)

- [[circle]] — centralized US- and EUR-pegged stablecoin issuer (USDC, EURC); 1:1 redemption with majority of reserves in SEC-registered 2a-7 USDXX MMF managed by BlackRock; weekly + monthly disclosure with Deloitte attestation since fiscal 2022; reporting since 2018; NYDFS BitLicense + MTL since 2015-09; BMA; MiCA registration not surfaced; USDC NOT on NYDFS Greenlist. (2 sources)
- [[sky-protocol]] — DeFi-native USD-pegged protocol (USDS, sUSDS, stUSDS, SKY); smart-contract-governed by SKY tokenholders; public interface operated by Skybase International; architectural contrast with Circle on every dimension. Aliases: makerdao.
- [[bitgo]] — institutional digital-asset custody and infrastructure provider; multi-jurisdictional subsidiary structure with NYDFS Limited Purpose Trust Charter (since 2021-03) AND OCC National Trust Bank Charter (BitGo Bank & Trust, N.A.); first custody-sector vendor in the wiki. (2 sources)
- [[chainalysis]] — institutional-grade blockchain compliance and investigation platform; first compliance-sector vendor in the wiki. Multi-product surface (KYT, Reactor, Risk Assessment, Hexagate, Alterya). 1,500+ customers; 9 of top 10 crypto exchanges; 45+ regulators worldwide. SaaS model, not a regulated digital-asset entity. (1 source)

## Concepts (26)

- [[karpathy-llm-wiki]] — the meta-pattern: a persistent, structured, LLM-maintained wiki that compiles knowledge once and keeps it current.
- [[raw-immutable-layer]] — first layer: curated source documents the LLM only reads from, never modifies.
- [[wiki-curated-layer]] — second layer: LLM-owned interlinked markdown pages updated as new sources arrive.
- [[schema-as-program]] — third layer: the schema file (`CLAUDE.md`) treated as the program the LLM executes.
- [[ingest-query-lint-operations]] — the three operations against the substrate: ingest a source, query the wiki, lint for drift.
- [[self-improving-substrate]] — compounding property: maintenance cost approaches zero, so the wiki gets richer with each ingest.
- [[citation-discipline]] — structural property across substrate / issuer / compliance-vendor layers. (5 sources)
- [[institutional-digital-asset-buyer]] — the audience this wiki's domain template is designed to serve.
- [[retail-grade-intelligence-gap]] — institutional digital-asset decisions get made on tools built for adjacent domains.
- [[counterparty-graph-research]] — research pattern: traverse named regulators, settlement partners, integration partners as a graph.
- [[mica-compliance]] — EU regulatory frame for crypto-assets (Reg 2023/1114); four categories (ART, EMT, "other", CASPs); Article 143 transitional period ends 1 July 2026.
- [[asset-referenced-token]] — MiCA Title III: tokens referencing baskets, commodities, multiple fiat, or other crypto-assets.
- [[e-money-token]] — MiCA Title IV: single-fiat-pegged tokens (USDC, EURC, USDS are EMT-archetype). (2 sources)
- [[crypto-asset-service-provider]] — MiCA Title V: custody, exchange, transfer, execution, advice, portfolio management, placement.
- [[crypto-asset-white-paper]] — MiCA disclosure primitive; iXBRL machine-readable from 2025-12-23; ESMA does NOT review/approve content.
- [[proof-of-reserves]] — structural transparency primitive for centralized stablecoin issuers; NOT universal in DeFi-native protocols. (2 sources)
- [[2a-7-government-money-market-fund]] — US-securities-law primitive: SEC-registered MMF restricted to government securities; the Circle Reserve Fund (USDXX).
- [[non-custodial-interface-vs-issuer]] — DeFi-native architectural pattern: smart-contract issuer + separate interface operator that disclaims control.
- [[dao-governance]] — decentralized governance via tokenholder voting; Sky's governance model.
- [[bitlicense]] — NYDFS virtual-currency regime (23 NYCRR Part 200); 5 activity categories; surety bond min $500K. (2 sources)
- [[limited-purpose-trust-charter]] — alternative NYDFS path; permits fiduciary powers + bundled MTL; preferred for custody vendors.
- [[nydfs-greenlist]] — explicit list of 8 NYDFS-approved coins (BTC, ETH, GUSD, GYEN, ZUSD, RLUSD, USDW, GOLD); USDC notably absent.
- [[occ-national-trust-bank-charter]] — federal US regulatory path; OCC-issued; multi-state operating scope; bank-like regulatory perimeter without FDIC.
- [[qualified-custodian]] — federal regulatory status under SEC Custody Rule (Rule 206(4)-2).
- [[kyt-know-your-transaction]] — real-time blockchain transaction screening for compliance; canonical compliance-vendor product category.
- [[on-chain-analytics]] — the technical primitive (clustering heuristics + ML + cross-chain tracing) on which KYT and other compliance-vendor products are built.

## Sectors (4)

- [[stablecoin-issuers]] — centralized-vs-DeFi-native architectural contrast (Circle vs. Sky); MiCA + NYDFS regulatory frames. (5 sources, 2 vendors)
- [[custody]] — three US regulatory paths (state BitLicense, state Limited Purpose Trust Charter, federal OCC National Trust Bank Charter) compared in tabular form; MiCA Title V CASP for EU. (4 sources, 1 vendor)
- [[regulatory-and-compliance]] — two-regime regulator-side comparison + compliance-vendor product categories table; first compliance-sector vendor populated. (4 sources, 1 vendor)
- [[payment-and-settlement]] — BitLicense + MTL canonical dual-licensing config. (3 sources)

## Sources (8)

- [[karpathy-llm-wiki-gist]] — Andrej Karpathy, GitHub Gist (2025). Canonical statement of the LLM Wiki pattern.
- [[51-deck-april-2026]] — Marc Baumann / Fiftyone Group LLC, public April 2026 deck. Audience-framing only.
- [[regulator-eu-mica-esma-hub]] — ESMA MiCA hub. EU regulatory frame for crypto-asset markets.
- [[vendor-circle-transparency-page-2026-04]] — Circle's public transparency page. 1:1 redemption, USDXX 2a-7 MMF, two-tier disclosure cadence, Deloitte audits, NYDFS + BMA licenses.
- [[vendor-sky-money-landing-2026-04]] — Sky Protocol's public interface. Skybase / Sky Protocol structural separation; DAO governance via SKY tokenholders.
- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS BitLicense + Trust Charter regime; Regulated Entities list; Greenlist.
- [[vendor-bitgo-homepage-2026-04]] — BitGo's public homepage. OCC national trust bank charter; corporate structure; product taxonomy; explicit non-FDIC/SIPC disclosure.
- [[vendor-chainalysis-homepage-2026-04]] — Chainalysis public homepage. KYT + Reactor + Risk Assessment products; on-chain analytics methodology; "court admissible" data positioning; 1,500+ customers.

## People (3)

- [[andrej-karpathy]] — author of the LLM Wiki gist.
- [[marc-baumann]] — Founder, 51 Group; author of the public 51 Terminal April deck.
- [[mike-belshe]] — CEO and Co-Founder, BitGo. Named in 51 deck (slide 13) and BitGo homepage. (2 sources)

## Firms (8)

- [[fiftyone-group-llc]] — publisher of the public 51 Terminal April deck; operator of 51 Terminal product (proprietary out-of-scope).
- [[esma]] — European Securities and Markets Authority; EU-level coordinator of MiCA.
- [[european-commission]] — proposer of MiCA; anchor-only.
- [[blackrock]] — manager of the Circle Reserve Fund (USDXX), SEC-registered 2a-7 MMF.
- [[deloitte]] — Big Four; Circle's independent auditor since fiscal 2022.
- [[skybase-international]] — operator of sky.money interface for Sky Protocol; "independent Sky Agent."
- [[nydfs]] — New York State Department of Financial Services; central US-state digital-asset regulator.
- [[occ]] — Office of the Comptroller of the Currency (US Treasury); federal regulator that chartered BitGo Bank & Trust, N.A.
