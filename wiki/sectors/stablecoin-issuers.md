---
type: sector
name: Stablecoin issuers
sources: 5
last_updated: 2026-04-27
---

# Stablecoin issuers

> *Vendors that issue digital tokens designed to maintain a stable value relative to a reference asset (typically a fiat currency, sometimes a basket or commodity). The institutional-buyer question is which issuer to trust as a counterparty.*

## Definition

A stablecoin issuer is a vendor — corporate, foundation, or protocol — that produces a digital token whose value is intended to track a reference unit (most commonly the US dollar). Issuance models vary: some issuers maintain centrally-held cash-and-equivalent reserves and attest to them periodically; others rely on over-collateralized on-chain crypto positions governed by smart contracts; others combine the two. The institutional-buyer question is rarely "which token has the best UX" and almost always **"which issuer's reserve and regulatory posture meets my risk threshold."**

This sector is named on the public 51 deck as a distinct research category (Slide 10's filter labels include "Stablecoin Issuer"). The wiki uses it as a sector entity; specific 51-product taxonomy detail is excluded under Path A.

## Vendors in this sector

- [[circle]] — centralized US- and EUR-pegged issuer (USDC, EURC). 1:1 redemption guarantee; majority of reserves held in the SEC-registered 2a-7 Circle Reserve Fund (USDXX) managed by BlackRock; weekly self-published holdings + monthly Big Four (Deloitte) attestation under AICPA standards; reporting history since 2018. Sourced from [[vendor-circle-transparency-page-2026-04]].
- [[sky-protocol]] — DeFi-native USD-pegged issuer (USDS). Smart-contract-governed by SKY tokenholders; public interface operated by separate non-custodial entity ([[skybase-international]]) that explicitly disclaims control. Architecturally distinct from Circle — no surfaced regulatory licenses, no surfaced audit firm, geographic restriction "currently unavailable in the US" without stated legal basis. Sourced from [[vendor-sky-money-landing-2026-04]].

## Centralized-vs-DeFi-native architectural contrast

The two vendors currently in this sector ([[circle]] and [[sky-protocol]]) demonstrate the load-bearing architectural choice institutional buyers face: **centralized issuer with regulator-grounded reserve transparency**, vs. **DeFi-native protocol with on-chain governance and structural disclaimers**.

| Dimension | [[circle]] (USDC, EURC) | [[sky-protocol]] (USDS) |
|---|---|---|
| Legal entity model | Single regulated entity | Smart contracts + separate non-custodial interface operator |
| Reserve disclosure | Weekly self-published + monthly Big Four attestation | Not surfaced on landing page |
| Reserve grounding | SEC-registered 2a-7 MMF (USDXX) managed by BlackRock | Not surfaced; presumed on-chain over-collateralization (open question) |
| Regulatory licenses | NYDFS Money Transmitter, NYDFS VCBA, BMA | None surfaced |
| Audit firm | [[deloitte]] since fiscal 2022 | None named |
| Governance | Corporate | Decentralized via SKY tokenholders ([[dao-governance]]) |
| Geographic posture | Available globally per regulatory licensing | "Currently unavailable in the US" without stated legal basis |

Neither model is universally better; they require **different diligence frameworks** ([[non-custodial-interface-vs-issuer]]).

## Governing concepts

- [[mica-compliance]] — the EU regulatory frame; issuers fall under either Title III ([[asset-referenced-token]]) or Title IV ([[e-money-token]]) depending on whether the token references a basket / commodity / multiple fiat (ART) or a single official currency (EMT). USD-pegged and EUR-pegged single-fiat stablecoins are EMTs.
- [[asset-referenced-token]] — Title III; multi-reference stabilisation.
- [[e-money-token]] — Title IV; single-fiat-reference stabilisation.
- [[crypto-asset-white-paper]] — issuer-side disclosure primitive under MiCA; iXBRL machine-readable from 23 December 2025.
- [[proof-of-reserves]] — the central transparency requirement for centrally-issued stablecoins. _(Page emerges from source 4 — Circle's reserve attestation.)_
- [[counterparty-graph-research]] — the research pattern that maps issuer → reserve custodian → audit firm → regulator chains.
- [[citation-discipline]] — license-clean attestation reporting is the base case for institutional-grade issuer research.

## Notable regulatory frame

- **EU MiCA** ([[regulator-eu-mica-esma-hub]]) — Titles III and IV both apply to stablecoin issuers operating in or serving the EU market. The transitional period under Article 143 runs until 1 July 2026, so authorisation status is currently a moving target. ESMA maintains the interim register; vendor `public_status:` frontmatter populates only when sourced from this register.
- **NYDFS** ([[regulator-nydfs-bitlicense-page-2026-04]]) — applies to issuers controlling/administering/issuing a virtual currency under [[bitlicense|BitLicense]] Part 200(5). NYDFS published "Guidance on the Issuance of U.S. Dollar-Backed Stablecoins" on 2022-06-08 (referenced from the source; not separately ingested). The [[nydfs-greenlist]] is a parallel coin-side surface — Greenlisted stablecoins as of 2026-04-27 include GUSD (Gemini Dollar), GYEN (GMO JPY), ZUSD (GMO USD), RLUSD (Ripple USD), USDW (WisdomTree Dollar). **Notably absent**: USDT, USDC, DAI, USDS, FDUSD, USDP. Circle holds a BitLicense (issuer-side) but USDC is not Greenlisted (coin-side) — these are structurally distinct regulatory questions.

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
- [[regulator-eu-mica-esma-hub]]
- [[vendor-circle-transparency-page-2026-04]]
- [[vendor-sky-money-landing-2026-04]]
- [[regulator-nydfs-bitlicense-page-2026-04]]
