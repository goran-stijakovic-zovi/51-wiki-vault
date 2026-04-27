---
type: sector
name: Payment and settlement
sources: 2
last_updated: 2026-04-27
---

# Payment and settlement

> *Vendors that operate digital-asset rails for moving value between institutions — exchanges, on/off-ramps, stablecoin settlement networks, card programs, and cross-border remittance corridors.*

## Definition

This sector covers the vendors that turn digital assets into a settlement medium: exchanges and OTC desks for liquidity provision, on/off-ramps for fiat-to-crypto conversion, stablecoin-based settlement networks for institutional transfers, card-rail programs for retail-facing payments, and cross-border remittance corridors. The institutional-buyer question is which rail to use for which use case: speed, cost, regulatory coverage, counterparty risk, and integration complexity all vary materially by vendor.

This sector is named on the public 51 deck as a distinct research category (Slide 10 filter labels include "Payment & Settlement"; Slide 7 separates "Card Rails" but the wiki collapses these into one sector for now). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

_(populated as public vendor sources are ingested. No target in this Session 1's seed list, but cross-sector vendors — e.g. Circle, which both issues a stablecoin and operates settlement rails — may have multiple sector wiki-links from their own pages.)_

## Governing concepts

- [[mica-compliance]] — applies to crypto-asset service providers in the EU, including settlement-layer operators.
- [[crypto-asset-service-provider]] — Title V regime; transfer-of-crypto-assets, exchange, execution, and reception/transmission of orders are all named CASP services.
- [[bitlicense]] — applies to virtual-currency businesses operating in NY, including exchanges and on/off-ramps. _(Page emerges from source 6.)_
- [[citation-discipline]] — settlement-vendor licensing and partner relationships are the operational substance of institutional-buyer diligence in this sector.

## Notable regulatory frame

- **EU MiCA** ([[regulator-eu-mica-esma-hub]]) — Title V CASP authorisation covers exchange, transfer, execution, placement, and order-routing services. Transitional period under Article 143 runs until 1 July 2026.
- NYDFS BitLicense (source 6, pending ingest) — applies to virtual-currency businesses serving New York including exchanges and on/off-ramps.
- Payment and settlement is the sector with the most jurisdiction overlap: a single vendor often operates under multiple licensing regimes (state-level US virtual-currency licenses, federal money-transmitter status, EU MiCA, equivalent regimes in UK / Singapore / Switzerland / etc.). The wiki's `public_status` vendor frontmatter is most populated here.

## Cross-sector connections

- [[stablecoin-issuers]] — issuers and settlement vendors overlap heavily; some vendors are both.
- [[custody]] — settlement vendors often partner with custodians for institutional-client asset holding.
- [[regulatory-and-compliance]] — settlement vendors are heavy users of compliance tooling (travel-rule, AML, KYT).

## Open questions

- Should "Card Rails" (slide 7) be a separate sector or collapsed into payment-and-settlement? Card programs have a meaningfully different vendor archetype (Mastercard / Visa / issuer banks) than crypto-native settlement, but the institutional-buyer use case is closely related.
- How does the sector handle vendors that operate purely on-chain (decentralized exchanges, on-chain swap protocols) where there is no regulated entity in the traditional sense? Are they out-of-scope for this institutional-buyer-framed wiki, or do they get pages under a separate "DeFi-native settlement" framing?

## Sources cited

- [[51-deck-april-2026]]
- [[regulator-eu-mica-esma-hub]]
