---
type: sector
name: Regulatory and compliance
sources: 4
last_updated: 2026-04-27
---

# Regulatory and compliance

> *Vendors that provide compliance, sanctions-screening, transaction-monitoring, and regulatory-reporting tooling for digital-asset operators — sitting between issuers / custodians / payment vendors and the regulators that govern them.*

## Definition

This sector covers vendors whose product is the **compliance layer** for digital-asset operations: blockchain analytics for sanctions-screening, transaction monitoring (KYT — Know Your Transaction), regulatory reporting, suspicious-activity detection, and travel-rule compliance. Their direct buyers are operators in adjacent sectors (issuers, custodians, payment processors, exchanges) who need to demonstrate compliance to their own regulators. Their indirect buyers are the regulators themselves, who often subscribe to compliance-vendor analytics directly.

This sector is named on the public 51 deck as a distinct research category (Slide 10 filter labels include "Regulatory & Compliance"). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

- [[chainalysis]] — institutional-grade blockchain compliance and investigation platform; the wiki's first compliance-sector vendor. Multi-product surface: KYT (transaction monitoring), Reactor (investigation), Risk Assessment (Address Screening / VASP Risking / Sentinel), emerging security (Hexagate, Alterya). Customer base: 1,500+ entities including 9 of top 10 crypto exchanges and 45+ regulators worldwide. Sourced from [[vendor-chainalysis-homepage-2026-04]].

## Compliance-vendor product categories

The compliance-vendor side of this sector decomposes into three operational product categories that map onto regulator-side requirements:

| Product category | Regulator-side anchor | Vendor in wiki |
|---|---|---|
| **[[kyt-know-your-transaction|KYT (Know Your Transaction)]]** — real-time transaction monitoring | NYDFS 23 NYCRR Part 504; FATF Travel Rule; MiCA Title V CASP supervisory obligations | [[chainalysis]] (KYT product) |
| **Investigation / fund-tracing** — multi-chain forensics | Law enforcement / regulator enforcement actions | [[chainalysis]] (Reactor product) |
| **Risk assessment** — wallet / VASP / token risk profiling | OFAC sanctions screening; FATF VASP definitions | [[chainalysis]] (Address Screening / VASP Risking / Sentinel) |

The structural primitive underlying all three is [[on-chain-analytics]] — clustering heuristics + ML applied to public blockchain transaction data at scale, with cross-chain tracing across bridges, mixers, DEX swaps, and DeFi protocols.

The compliance-vendor business model is **SaaS** — Chainalysis is not a regulated digital-asset entity itself (no [[bitlicense|BitLicense]], no [[limited-purpose-trust-charter|trust charter]], no [[occ-national-trust-bank-charter|OCC charter]]); it sells products to regulated entities that need to satisfy their own regulator obligations. This is structurally distinct from issuers and custodians.

## Governing concepts

- [[mica-compliance]] — the EU regulatory frame; compliance vendors map their tooling to MiCA's authorisation, supervision, and reporting requirements across all four regulatory categories ([[asset-referenced-token]], [[e-money-token]], "other crypto-assets," [[crypto-asset-service-provider]]).
- [[crypto-asset-service-provider]] — Title V supervisory regime; compliance vendors are heavy consumers of CASP-side reporting requirements (transaction monitoring, conduct-of-business, suitability) and often operate as CASPs themselves where their product includes order-handling.
- [[crypto-asset-white-paper]] — iXBRL machine-readable disclosures are a structured-data input compliance vendors can directly consume.
- [[bitlicense]] — NYDFS's central virtual-currency-regulatory primitive; compliance vendors map their tooling to BitLicense reporting requirements (23 NYCRR Part 200 + 23 NYCRR Part 504 transaction monitoring + cybersecurity).
- [[limited-purpose-trust-charter]] — NYDFS's alternative regulatory path for fiduciary-powers vendors.
- [[nydfs-greenlist]] — the parallel coin-side approval mechanism; relevant to vendors offering specific stablecoins.
- [[kyt-know-your-transaction]] — the canonical compliance-vendor product category; real-time transaction monitoring.
- [[on-chain-analytics]] — the technical primitive on which KYT and other compliance-vendor products are built.
- [[citation-discipline]] — compliance outputs are the canonical example of citable, defensible analytics for regulator audiences. Chainalysis's "court admissible" positioning is structural citation discipline at the compliance-vendor product layer.

## Notable regulatory frame

- **EU MiCA** ([[regulator-eu-mica-esma-hub]]) — central EU frame. ESMA + EBA + national competent authorities form the supervisory triad. The interim MiCA register (weekly CSV) is the public source of truth for MiCA-registered status.
- **NYDFS BitLicense + Limited Purpose Trust Charter** ([[regulator-nydfs-bitlicense-page-2026-04]]) — central US-state frame. Two parallel authorisation paths: BitLicense (23 NYCRR Part 200) for transactional vendors, [[limited-purpose-trust-charter|Limited Purpose Trust Charter]] for fiduciary-powers vendors. NYDFS Regulated Entities list is the regulator-side source of truth. NYDFS Greenlist ([[nydfs-greenlist]]) is the parallel coin-side surface.
- This sector both **uses** regulatory frameworks (the vendor's product maps client activity to regulator-defined categories) and **is regulated by** them (compliance vendors handling personal data are themselves subject to GDPR, financial-sector data regulations, etc.). The two-sided relationship makes this the most graph-dense sector in the schema.

## Two regulatory regimes compared

| Dimension | EU MiCA | NYDFS (NY-state) |
|---|---|---|
| Source | [[regulator-eu-mica-esma-hub]] | [[regulator-nydfs-bitlicense-page-2026-04]] |
| Regulator | [[esma]] (coordinator) + national competent authorities | [[nydfs]] |
| Issuer regimes | ART (Title III), EMT (Title IV) | BitLicense Part 200(5) "controlling/administering/issuing" |
| Service-provider regime | [[crypto-asset-service-provider]] (Title V) | BitLicense Parts 200(1)–(4); custody often under [[limited-purpose-trust-charter]] |
| Disclosure primitive | [[crypto-asset-white-paper]] (iXBRL machine-readable from 2025-12-23) | Application package via NMLS; Regulated Entities list publicly published |
| Coin-listing surface | Implicit (issuer-side white paper) | [[nydfs-greenlist]] (vendor-side mechanism) |
| Source of truth for vendor status | Interim MiCA register (weekly CSV) | Regulated Entities list (static table) |

## Cross-sector connections

- [[stablecoin-issuers]] — issuers use compliance vendors for sanctions screening on their token transfers.
- [[custody]] — custodians use compliance vendors for KYT on inbound deposits.
- [[payment-and-settlement]] — payment vendors use compliance vendors for travel-rule compliance and AML monitoring.

## Open questions

- Where does the boundary lie between "compliance vendor" (third-party tooling) and "regulator" (the authority itself)? Both produce structured outputs about who's compliant; only one issues licenses.
- How does the sector model the increasing convergence between compliance vendors and law-enforcement / national-security buyers? Some vendors serve both regulator-subscribers and government clients; the public-disclosure boundary matters for Path A wiki ingestion.

## Sources cited

- [[51-deck-april-2026]]
- [[regulator-eu-mica-esma-hub]]
- [[regulator-nydfs-bitlicense-page-2026-04]]
- [[vendor-chainalysis-homepage-2026-04]]
