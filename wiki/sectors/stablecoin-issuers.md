---
type: sector
name: Stablecoin issuers
sources: 1
last_updated: 2026-04-27
---

# Stablecoin issuers

> *Vendors that issue digital tokens designed to maintain a stable value relative to a reference asset (typically a fiat currency, sometimes a basket or commodity). The institutional-buyer question is which issuer to trust as a counterparty.*

## Definition

A stablecoin issuer is a vendor — corporate, foundation, or protocol — that produces a digital token whose value is intended to track a reference unit (most commonly the US dollar). Issuance models vary: some issuers maintain centrally-held cash-and-equivalent reserves and attest to them periodically; others rely on over-collateralized on-chain crypto positions governed by smart contracts; others combine the two. The institutional-buyer question is rarely "which token has the best UX" and almost always **"which issuer's reserve and regulatory posture meets my risk threshold."**

This sector is named on the public 51 deck as a distinct research category (Slide 10's filter labels include "Stablecoin Issuer"). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

_(populated as public vendor sources are ingested. Targets in this Session 1: [[circle]] (source 4), [[sky-protocol]] (source 5).)_

## Governing concepts

- [[proof-of-reserves]] — the central transparency requirement for centrally-issued stablecoins. _(Page emerges from source 4 — Circle's reserve attestation.)_
- [[mica-compliance]] — the EU regulatory frame for asset-referenced and e-money tokens. _(Page emerges from source 3 — EU MiCA public summary.)_
- [[counterparty-graph-research]] — the research pattern that maps issuer → reserve custodian → audit firm → regulator chains.
- [[citation-discipline]] — license-clean attestation reporting is the base case for institutional-grade issuer research.

## Notable regulatory frame

_(populated as regulator sources are ingested. EU MiCA (source 3) and NYDFS BitLicense (source 6) both apply to issuers operating in their respective jurisdictions.)_

## Cross-sector connections

- [[custody]] — issuers depend on custodians for reserve safekeeping; the relationship is one of the densest in the counterparty graph.
- [[regulatory-and-compliance]] — issuers are subject to regulator authorization and to compliance-vendor screening.
- [[payment-and-settlement]] — stablecoins are settlement primitives; some issuers also operate payment rails.

## Open questions

- Where does the "stablecoin issuer" boundary lie when an issuer also runs a settlement business (e.g. a vendor on slide 7's Card Rails category that also issues a token)? Should the vendor get two sector wiki-links?
- DeFi-native issuers (Sky / Aave / others) operate without a corporate counterparty in the traditional sense. How does the institutional-buyer screening framework adapt? _(Question to revisit after source 5 — Sky Protocol.)_
- The deck's slide 10 filter lists 42 vendors in this sector — what's the public-source-only sub-set the wiki can populate from genuinely public materials? _(Operational question for the seed-source ingest order.)_

## Sources cited

- [[51-deck-april-2026]]
