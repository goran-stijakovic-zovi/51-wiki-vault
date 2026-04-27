---
type: sector
name: Custody
sources: 2
last_updated: 2026-04-27
---

# Custody

> *Vendors that hold digital assets on behalf of institutional clients — typically with cryptographic key management, regulatory licensing, and bankruptcy-remote segregation as core service primitives.*

## Definition

A custodian is a vendor whose service is the safekeeping of client digital assets. The institutional-buyer questions are: under what regulatory regime does the custodian operate, what cryptographic key-management architecture does it use (cold storage, MPC, multisig), what's the bankruptcy-remoteness of client assets, and what's the audit posture. Custody is often the most regulation-heavy sector in digital assets — qualified-custodian status under specific jurisdictions (US-NY BitLicense, US-Federal trust charter, EU equivalent regimes) is frequently a first-order screening criterion for institutional buyers.

This sector is named on the public 51 deck as a distinct research category (Slide 10 filter labels include "Custody"). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

_(populated as public vendor sources are ingested. Target in this Session 1: [[bitgo]] OR [[fireblocks]] (source 7 — Goran picks).)_

## Governing concepts

- [[mica-compliance]] — under MiCA, custody-and-administration of crypto-assets is a Title V CASP service ([[crypto-asset-service-provider]]).
- [[crypto-asset-service-provider]] — Title V regime that covers custody as one of the named services.
- [[qualified-custodian]] — regulatory status that defines custody for institutional purposes. _(Page emerges from sources 6 — NYDFS — and 7 — custody vendor.)_
- [[mpc-key-management]] — multi-party computation as the modern key-management architecture. _(Page emerges from source 7 — depending on whether BitGo or Fireblocks; both are MPC-relevant.)_
- [[bankruptcy-remote-segregation]] — the structural property that makes client assets recoverable in a custodian failure scenario. _(Page emerges if a source substantively develops it.)_
- [[counterparty-graph-research]] — custodians are dense graph nodes (every issuer they custody for, every audit firm they work with, every regulator they report to).

## Notable regulatory frame

- **EU MiCA** ([[regulator-eu-mica-esma-hub]]) — custody-and-administration is a Title V CASP service. Custodians serving EU clients need CASP authorisation; transitional period under Article 143 runs until 1 July 2026.
- NYDFS BitLicense (source 6, pending ingest) — applies to custodians operating from or serving New York.
- SEC qualified-custodian rules — apply for custodians serving US registered investment advisers.

## Cross-sector connections

- [[stablecoin-issuers]] — issuers depend on custodians for reserve safekeeping.
- [[regulatory-and-compliance]] — custody is the most regulation-heavy sector; substantial overlap.
- [[payment-and-settlement]] — many custodians also offer settlement infrastructure for institutional clients.

## Open questions

- Where does "custody" boundary against "wallet provider" — does any vendor whose product holds keys belong here, or only those operating under a regulatory custody charter?
- How does the sector model on-chain protocol custody (Sky's collateral vaults, smart-contract-held positions) where the "custodian" is a smart contract rather than a regulated entity?

## Sources cited

- [[51-deck-april-2026]]
- [[regulator-eu-mica-esma-hub]]
