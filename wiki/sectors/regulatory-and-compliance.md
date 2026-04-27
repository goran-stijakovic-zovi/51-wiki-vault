---
type: sector
name: Regulatory and compliance
sources: 1
last_updated: 2026-04-27
---

# Regulatory and compliance

> *Vendors that provide compliance, sanctions-screening, transaction-monitoring, and regulatory-reporting tooling for digital-asset operators — sitting between issuers / custodians / payment vendors and the regulators that govern them.*

## Definition

This sector covers vendors whose product is the **compliance layer** for digital-asset operations: blockchain analytics for sanctions-screening, transaction monitoring (KYT — Know Your Transaction), regulatory reporting, suspicious-activity detection, and travel-rule compliance. Their direct buyers are operators in adjacent sectors (issuers, custodians, payment processors, exchanges) who need to demonstrate compliance to their own regulators. Their indirect buyers are the regulators themselves, who often subscribe to compliance-vendor analytics directly.

This sector is named on the public 51 deck as a distinct research category (Slide 10 filter labels include "Regulatory & Compliance"). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

_(populated as public vendor sources are ingested. Target in this Session 1: [[chainalysis]] (source 8).)_

## Governing concepts

- [[mica-compliance]] — the EU regulatory frame; compliance vendors map their tooling to MiCA's authorization and reporting requirements. _(Page emerges from source 3 — EU MiCA public summary.)_
- [[bitlicense]] — the NYDFS regulatory frame; compliance vendors map their tooling to BitLicense reporting requirements. _(Page emerges from source 6 — NYDFS BitLicense list.)_
- [[citation-discipline]] — compliance outputs are the canonical example of citable, defensible analytics for regulator audiences.

## Notable regulatory frame

This sector both **uses** regulatory frameworks (the vendor's product maps client activity to regulator-defined categories) and **is regulated by** them (compliance vendors handling personal data are themselves subject to GDPR, financial-sector data regulations, etc.). The two-sided relationship makes this the most graph-dense sector in the schema.

## Cross-sector connections

- [[stablecoin-issuers]] — issuers use compliance vendors for sanctions screening on their token transfers.
- [[custody]] — custodians use compliance vendors for KYT on inbound deposits.
- [[payment-and-settlement]] — payment vendors use compliance vendors for travel-rule compliance and AML monitoring.

## Open questions

- Where does the boundary lie between "compliance vendor" (third-party tooling) and "regulator" (the authority itself)? Both produce structured outputs about who's compliant; only one issues licenses.
- How does the sector model the increasing convergence between compliance vendors and law-enforcement / national-security buyers? Some vendors serve both regulator-subscribers and government clients; the public-disclosure boundary matters for Path A wiki ingestion.

## Sources cited

- [[51-deck-april-2026]]
