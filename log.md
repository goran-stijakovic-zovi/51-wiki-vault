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

## [2026-04-27] lint | first-pass after-ingest-4 lint | _lint-2026-04-27
- 7 findings (4 informational, 3 actionable). Path A leakage check: PASS.
- Forward references to upcoming-ingest pages (bitgo, fireblocks, chainalysis, sky-protocol, nydfs, bitlicense, qualified-custodian, mpc-key-management, regulator-nydfs-bitlicense-list, bankruptcy-remote-segregation, bma) flagged as informational F1 — will resolve through ingests 5–8.
- Schema iteration applied: see [[2026-04-27 schema commit]] below

## [2026-04-27] schema | iterate after ingest-4 lint | CLAUDE.md + firm.md template + 3 fix commits
- Expanded `_templates/firm.md` `kind:` enumeration: `regulator | audit-firm | asset-manager | bank | custodian-firm | parent-company | consulting-firm | ratings-agency | other`
- Added "Firm kinds" subsection to CLAUDE.md documenting the canonical enumeration + `other` escape-hatch rule
- Fixed F2 `[[source-page-name]]` placeholder in citation-discipline.md → real example `[[karpathy-llm-wiki-gist]]`
- Fixed F3 orphan pages: added `[[andrej-karpathy]]` cross-reference on karpathy-llm-wiki-gist source page; added `[[esma]]` and `[[european-commission]]` cross-references on regulator-eu-mica-esma-hub source page
- F5 (vendor public_status: schema richness) deferred to after-ingest-8 lint when more vendors are populated

## [2026-04-27] ingest | Sky.money landing page (Sky Protocol public interface) | vendor-sky-money-landing-2026-04
- Pages touched: 1 source + 1 vendor (sky-protocol) + 2 new concepts + 1 new firm + 3 deepened pages = 5 new pages, 3 updates
- New vendor: sky-protocol — DeFi-native USD-pegged stablecoin protocol; second vendor in the wiki. public_status: [] (deliberately empty — no licenses surfaced; the contrast with Circle's populated list is the finding). aliases: [makerdao] (rebrand attribution from public domain; not stated on source page).
- New concepts: non-custodial-interface-vs-issuer (architectural separation pattern), dao-governance (decentralized tokenholder governance)
- New firms: skybase-international (kind: other — interface-operator role not yet canonical in the firm.kind enumeration; will graduate to canonical via schema iteration if a second DeFi-native protocol enters with the same role pattern)
- Deepened: stablecoin-issuers (now 4 sources, 2 vendors, with the centralized-vs-DeFi-native architectural contrast section), proof-of-reserves (now 2 sources — Sky as counter-example illustrating that proof-of-reserves regimes are not universal in DeFi-native protocols), citation-discipline (now 4 sources — Sky's structural disclaimers as the counter-pattern)
- Substantive negative findings well-captured: Sky's landing page does NOT surface collateralization details, audit firms, regulatory licenses, rebrand history, or the "Stars" sub-DAO structure. Each gap is an open question on the relevant page.
- Source-acquisition note: docs.sky.money returned HTTP 403; endgame.makerdao.com ECONNREFUSED; info.skyeco.com is JS-rendered and returned empty shell to fetcher; developers.skyeco.com homepage was navigation-only. Substantive technical content gated behind sub-pages that would need targeted fetching in a future ingest.
- Path A check: PASS — landing page is fully public; no IP concerns; rebrand history attributed to public domain with body note rather than reproduced as source-side claim

## [2026-04-27] ingest | NYDFS — Virtual Currency Businesses (BitLicense + Limited Purpose Trust Charter) | regulator-nydfs-bitlicense-page-2026-04
- Pages touched: 1 source + 1 firm + 3 concepts + 6 deepened pages = 5 new, 6 updates
- New firm: nydfs (kind: regulator, jurisdiction: US-NY) — central US-state digital-asset regulator
- New concepts (all substantive single-source promotions per the schema's "own section + multi-paragraph + regulatory weight" bar):
  - bitlicense — substantive: 23 NYCRR Part 200, five activity categories, five exemption categories, NMLS application, capital + surety bond ≥$500K, dual-licensing-with-MTL pattern
  - limited-purpose-trust-charter — alternative NY path; fiduciary-powers + bundled-MTL advantages over BitLicense; preferred path for custody vendors (BitGo, Coinbase Custody, Gemini)
  - nydfs-greenlist — 8-coin static list (BTC, ETH, GUSD, GYEN, ZUSD, RLUSD, USDW, GOLD); three paths to listing; DFS retains discretionary authority; coin-side mechanism distinct from vendor-side BitLicense
- Deepened: circle (now 2 sources — public_status: regulator-side cross-confirmed with 2015-09 license dates), regulatory-and-compliance (3 sources — added two-regime comparison table), custody (3 sources — added Limited Purpose Trust Charter as canonical custodian path), payment-and-settlement (3 sources — BitLicense + MTL canonical dual-licensing pattern), stablecoin-issuers (5 sources — added Greenlist mechanics + USDC absence finding), mica-compliance (cross-reference to BitLicense as US-state analogue with structural-difference framing)
- Schema observation: vendor `public_status:` field gained date qualifiers ("since 2015-09") for the first time. Tracked for after-ingest-8 lint as a candidate richer-schema move (separate `licenses:` structured field with type+jurisdiction+date+source).
- Substantive negative finding documented: USDC is NOT on NYDFS Greenlist as of 2026-04-27, despite Circle holding a BitLicense. Captured as open question on circle, nydfs-greenlist, and stablecoin-issuers.
- Path A check: PASS — NYDFS source is fully public regulator material

## [2026-04-27] ingest | BitGo public homepage | vendor-bitgo-homepage-2026-04
- Pages touched: 1 source + 1 vendor + 2 concepts + 1 firm + 1 person + 3 deepened pages = 6 new, 3 updates
- New vendor: bitgo — first custody-sector vendor in the wiki. public_status: NYDFS Limited Purpose Trust Charter (since 2021-03) + OCC National Trust Bank Charter (BitGo Bank & Trust, N.A.). Multi-jurisdictional subsidiary structure (BitGo Holdings → BitGo Bank & Trust N.A. + BitGo NY Trust Co LLC).
- New concepts:
  - occ-national-trust-bank-charter — substantive: federal US regulatory primitive distinct from state BitLicense / state trust charter; multi-state operating scope; bank-like regulatory perimeter without FDIC
  - qualified-custodian — substantive: federal SEC Custody Rule (Rule 206(4)-2); required for vendors serving SEC-registered investment advisers
- New firms: occ (kind: regulator, jurisdiction: US-Federal)
- New people: mike-belshe (2 sources — 51 deck slide 13 + BitGo homepage; CEO + Co-Founder of BitGo)
- Deepened: custody (now 4 sources — added comparative table of three US regulatory paths: state BitLicense, state Trust Charter, federal OCC charter), limited-purpose-trust-charter (cross-reference to OCC charter as federal analogue), bitlicense (cross-reference to OCC charter)
- Substantive findings: BitGo's recent OCC national trust bank charter conversion is the headline regulatory primitive from this ingest. The "three regulatory paths in US digital-asset custody" comparison is now load-bearing structure on the custody sector page.
- Schema observation: vendor `public_status:` is starting to lean into multi-line / multi-jurisdiction qualifiers (BitGo has 2 entries with subsidiary names + dates; Circle has 3 entries with subsidiary names + dates). The richer-schema candidate (separate `licenses:` field with type+jurisdiction+date+source) is increasingly justified. Still tracked for after-ingest-8 lint.
- Open questions captured: BitGo MPC architecture details, bankruptcy-remote segregation language, insurance coverage, SOC 1/2 / ISO 27001, state trust charters beyond NY, the Mike Belshe IPO letter content (SEC EDGAR S-1 future-ingest), MiCA EU posture, relationship to specific stablecoin issuers using BitGo for reserve custody
- Path A check: PASS — BitGo homepage is fully public

## [2026-04-27] ingest | Chainalysis public homepage | vendor-chainalysis-homepage-2026-04
- Pages touched: 1 source + 1 vendor + 2 concepts + 2 deepened pages = 4 new, 2 updates
- New vendor: chainalysis — first compliance-sector vendor in the wiki. SaaS model (NOT a regulated digital-asset entity); empty public_status: field. Multi-product surface: KYT, Reactor, Risk Assessment (Address Screening / VASP Risking / Sentinel), Hexagate, Alterya, Data Solutions.
- New concepts:
  - kyt-know-your-transaction — substantive: real-time transaction screening; canonical compliance-vendor product category. Anchored on Chainalysis KYT product.
  - on-chain-analytics — substantive: technical primitive (clustering heuristics + ML + cross-chain tracing) underlying KYT, Reactor, Risk Assessment.
- Deepened: regulatory-and-compliance (now 4 sources, 1 vendor — added compliance-vendor product categories table mapping product types to regulator-side anchors), citation-discipline (now 5 sources — added compliance-vendor product layer as third citation-discipline layer)
- Schema observation tracked for the after-ingest-8 lint: empty `public_status:` field for chainalysis is itself a finding (the vendor IS in the regulatory-and-compliance sector but doesn't itself hold regulatory licenses; the empty list communicates this structurally).
- Substantive findings: Chainalysis is the wiki's canonical institutional-grade compliance vendor. The compliance-vendor product categories table on the regulatory-and-compliance sector page connects regulator-side anchors (NYDFS Part 504, FATF Travel Rule, MiCA Title V, OFAC, FATF VASP) to vendor-side products (KYT, Reactor, Risk Assessment) — the wiki's first product-vs-regulator mapping.
- Path A discipline note: Chainalysis homepage names IRS as a tax-agency client. Reproduced as one of named-example-clients on both the source page and the vendor page; quantified PR claims ($34B frozen, 9 of top 10 exchanges, 45+ regulators, 1,500+ customers) reproduced verbatim. Specific named-government case studies elsewhere on chainalysis.com flagged as different licensing posture if future ingest proposed.
- Path A check: PASS — Chainalysis homepage is fully public

## [2026-04-27] lint | Session 1 final after-ingest-8 lint | _lint-2026-04-27 (updated)
- 8 findings total. 5 informational, 1 deferred (F2 — vendor public_status: richness — schema iteration deferred until 5th-or-6th-vendor pressure), 1 PASS check (F7 Path A leakage), 1 forward-reference-resolution-tracking (F8 — 6 of 11 resolved, 4 deferred to future sessions).
- Top-10 most-linked pages confirms architectural premise: citation-discipline (39), stablecoin-issuers (34), circle (34), regulator-nydfs source (31), Circle transparency source (28), mica-compliance (28), bitlicense (28).
- Multi-source concepts: 3 (citation-discipline at 5 sources, proof-of-reserves and e-money-token at 2 each).
- Zero orphans. Forward-references remaining: bankruptcy-remote-segregation, bma, mpc-key-management.
- No schema iteration applied in this lint commit. Schema feels stable at end-of-Session-1.
- Memory file at ~/.claude/projects/-Users-gstijakovic-Dev-Projects-51-wiki/memory/project_51_wiki.md updated with final-state vault summary.

## [2026-04-27] session-end | Session 1 complete | 8 ingests + 2 lints + 1 schema iteration
- Vault state: 63 wiki pages, 8 commits to main + 1 schema commit + 2 lint files (one updated), repo public at https://github.com/goran-stijakovic-zovi/51-wiki-vault.
- Session 2 (public deploy at 51.zoviconsulting.com) per kickoff doc Step 7 is out of scope here and triggered separately.
