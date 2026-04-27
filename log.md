# Log

Append-only chronological journal. Every ingest, query, and lint operation gets one entry.

Format: `## [YYYY-MM-DD] <op> | <one-line summary>`

---

## [2026-04-27] init | Vault scaffolded — CLAUDE.md, templates, raw/ subdirs, README.md, index.md, log.md

## [2026-04-27] ingest | LLM Wiki (Karpathy gist) | karpathy-llm-wiki-gist
- Pages touched: 1 source + 7 concepts + 1 person = 9 new
- Concepts created: karpathy-llm-wiki, raw-immutable-layer, wiki-curated-layer, schema-as-program, ingest-query-lint-operations, self-improving-substrate, citation-discipline
- People created: andrej-karpathy (anchor-only)
- Deferred (single-source, not yet substantively-developed enough): compounding-artifact-vs-rag, index-and-log-as-navigation, query-answer-as-new-source — re-evaluate when a second source touches them
- Open questions raised: schema-iteration cadence; ephemeral-source citation patterns; substrate value vs. corpus size curve
- Path A check: PASS — gist is fully public, no proprietary content concerns

## [2026-04-27] ingest | 51 Terminal — Product Overview (April 2026) | 51-deck-april-2026
- Path A scope: framing-only. Banner on source page documents the redactions.
- Pages touched: 1 source + 3 new concepts + 4 new sectors + 1 new person + 1 new firm + 1 deepened concept = 11 new pages, 1 update
- New concepts: institutional-digital-asset-buyer, retail-grade-intelligence-gap, counterparty-graph-research
- New sectors (skeletons): stablecoin-issuers, custody, regulatory-and-compliance, payment-and-settlement
- New people: marc-baumann (anchor-only)
- New firms: fiftyone-group-llc (anchor-only)
- Deepened: citation-discipline (now 2 sources; added licensing-clean-output framing for institutional buyers)
- Path A redactions documented on the source page: Trust Score values, pillar weights "(90%)", "1300+ vendors / 95 datapoints / 500+ datapoints" product-scale claims, vendor-per-category counts, named vendor lists from slides 7 and 10, slide 11 competitor matrix specifics, slide 12 client-result stats, slide 13 individual expert-network biographical pages (will only graduate to people pages if a later source substantively cites them)
- Path A check: PASS — banner documented; no proprietary numbers reproduced; framing-only discipline held

## [2026-04-27] ingest | ESMA — Markets in Crypto-Assets Regulation (MiCA) hub | regulator-eu-mica-esma-hub
- Pages touched: 1 source + 5 new concepts + 2 new firms + 4 deepened sectors = 8 new pages, 4 updates
- New concepts: mica-compliance (substantive — the central EU regulatory frame), asset-referenced-token (Title III), e-money-token (Title IV), crypto-asset-service-provider (Title V), crypto-asset-white-paper (disclosure primitive with iXBRL requirement)
- New firms: esma (regulator — first regulator firm page in the wiki), european-commission (anchor-only)
- Deepened (now 2 sources each): stablecoin-issuers, custody, regulatory-and-compliance, payment-and-settlement — added MiCA frame sections with cross-links to ART, EMT, CASP, white-paper concepts
- Schema observation tracked for lint-after-ingest-4: Article 143 transitional period (until 1 July 2026) creates a "MiCA in transition" status distinct from "MiCA-registered" — `public_status:` frontmatter may need a sub-state value like ["MiCA-transitional"] or a `mica_transitional_until: 2026-07-01` field. Will resolve when first MiCA-touching vendor enters the wiki (Circle source 4 likely).
- Schema observation tracked: ESMA's iXBRL white-paper format is a candidate Tier-3 fetcher target — could in principle auto-populate vendor `public_status:` from the ESMA register CSV. Noted in scripts/_README.md future-fetcher list.
- Path A check: PASS — ESMA hub is a public regulator page; no IP concerns

## [2026-04-27] ingest | Circle USDC Transparency & Reserves (public page, fetched April 2026) | vendor-circle-transparency-page-2026-04
- Pages touched: 1 source + 1 vendor (FIRST vendor page!) + 2 new concepts + 2 new firms + 3 deepened pages = 6 new pages, 3 updates
- New vendor: circle — first vendor page in the wiki. Sector=stablecoin-issuers; role=stablecoin-issuer; public_status populated with NYDFS Money Transmitter, NYDFS VCBA, BMA Digital Asset Business; named counterparties: BlackRock (fund manager), Deloitte (auditor), NYDFS (regulator pending source 6), BMA (regulator)
- New concepts: proof-of-reserves (substantive — sector-defining transparency primitive), 2a-7-government-money-market-fund (US-securities-law primitive)
- New firms: blackrock (asset-manager — kind value), deloitte (audit-firm)
- Deepened: stablecoin-issuers (now 3 sources, 1 vendor populated), e-money-token (now 2 sources — Circle is EMT-archetype), citation-discipline (now 3 sources — Circle's two-tier disclosure regime as canonical implementation)
- Path A redactions documented on source page: $277B bridge-volume scale claim, current-month reserve composition snapshots, daily issuance/redemption summaries (point-in-time data)
- Schema observation: vendor `public_status:` got its first real population. Captured Circle's USDXX → SEC-2a-7 grounding via a parenthetical "(via USDXX)" qualifier in the value. Worth flagging at lint as a candidate for richer schema (e.g. separate `regulatory_relationships:` field) if more vendors surface similar nuance.
- Schema observation: `firm.kind: asset-manager` is a new kind value (BlackRock); not previously in the firm-template enumeration. Working as ad-hoc; flag at lint for the canonical kind enumeration update.
- Substantive negative finding: Circle's transparency page does NOT mention MiCA. EU-side disclosure layer absent. Captured as open question on circle, e-money-token, and the source pages.
- Path A check: PASS — Circle's transparency page is fully public; structural / policy claims captured; point-in-time financial snapshots not reproduced
