---
type: source
name: Sky.money landing page (Sky Protocol public interface, fetched April 2026)
source_url: https://sky.money
publication: Skybase International (interface operator); Sky Protocol governance (smart contracts)
author: Skybase International (institutional)
published: 2026 (page maintained by Skybase as the public Sky Protocol interface)
ingested: 2026-04-27
paywalled: false
---

# Sky.money landing page (Sky Protocol public interface, fetched April 2026)

> _Source: https://sky.money_

## Summary

Sky.money is the public landing page and interface for the **Sky Protocol** stablecoin ecosystem, operated by **Skybase International** as a "non-custodial interface" with explicit structural separation from Sky Protocol itself. The protocol issues four primary tokens: **USDS** (the stablecoin), **sUSDS** (yield-generating savings token earning the Sky Savings Rate), **stUSDS** (high-performance risk-capital token), and **SKY** (the governance token). Governance is "decentralized governance by SKY tokenholders," and protocol parameters including the Sky Savings Rate are "subject to change or elimination at any time."

The structural contrast with [[circle|Circle]] is the substantive payload of this ingest. Circle is a single regulated legal entity with weekly self-published holdings, monthly Big Four attestations under AICPA standards, and named US + Bermuda regulatory licenses. Sky's landing page describes a **deliberate three-way separation** between (a) Sky Protocol smart contracts governed by SKY tokenholders, (b) Skybase International as the non-custodial interface operator that "does not control, set, or guarantee" rates, and (c) the geographic restriction "currently unavailable in the US" for sUSDS and stUSDS without stated legal basis.

The landing page **does NOT surface**:

- Any rebrand history from MakerDAO (widely understood in the public domain but not stated on this source).
- Detailed collateralization mechanics for USDS (on-chain, off-chain, or hybrid).
- Reserve composition, audit firms, or attestation regimes.
- Explicit MiCA, NYDFS, or SEC regulatory positioning.
- The "Stars" / sub-DAO structure if it formally exists.
- Real-world asset (RWA) collateral exposure.

These gaps are themselves a finding: Sky Protocol's most institutional-relevant architectural details are gated behind the developer portal, chainlog, and governance forum. The substantive technical content was sought during this ingest but unavailable from the immediate fetcher (`docs.sky.money` returned HTTP 403; `info.skyeco.com` is JS-rendered and returned an empty shell; `developers.skyeco.com` was navigation-only). The wiki therefore characterizes Sky Protocol from the landing page only, with substantive technical detail flagged as open questions for a follow-up source ingest.

For an institutional buyer doing diligence, the takeaway is structural: a DeFi-native stablecoin protocol's public-facing surface communicates **decentralization claims and governance disclaimers**, not reserve transparency or regulatory positioning. The architectural choice itself is the message.

## Key claims

1. **Skybase / Sky Protocol structural separation.** — > "Sky.money is a non-custodial interface operated by Skybase, an independent Sky Agent with no control over Sky Protocol smart contracts or ecosystem governance."
2. **Decentralized governance via SKY tokenholders.** — > "The Sky Savings Rate and all other protocol parameters are determined through decentralized governance by SKY tokenholders and are subject to change or elimination at any time."
3. **Four primary tokens: USDS, sUSDS, stUSDS, SKY.**
4. **sUSDS as yield-generating savings token.** — > "Maximize your dollars with the Sky Savings Rate. Governed by Sky Ecosystem to deliver the best risk-adjusted yield, sUSDS allows you to grow your holdings with instant liquidity and zero fees."
5. **stUSDS as risk-capital token.** — > "High-performance risk capital… provides the essential liquidity that powers SKY-backed borrowing in exchange for accelerated returns."
6. **SKY explicitly disclaimed as a non-security.** — > "SKY is a decentralized governance token of Sky Protocol. It is not a security, investment contract, or financial instrument."
7. **Repeated structural disclaimers.** — > "Sky.money does not control, set, or guarantee the rate." (Repeated for sUSDS, stUSDS, and vault yields.)
8. **Skybase autonomy from governance.** — > "Skybase does not participate in, and has no ability to control or guarantee outcomes of, decentralized governance processes."
9. **Forward-looking-statements limited liability.** — > "Actual results could differ materially due to market volatility, regulatory changes, and decisions made through decentralized governance that are outside Skybase's control."
10. **Geographic restriction without stated legal basis.** — sUSDS, stUSDS, and Sky Ecosystem Rewards display "Currently unavailable in the US."

## Concepts cited

- [[non-custodial-interface-vs-issuer]] — the architectural separation between Skybase (interface) and Sky Protocol (smart contracts) as a domain primitive distinct from Circle's single-entity model.
- [[dao-governance]] — decentralized governance via SKY tokenholders; the contrast with Circle's corporate governance.
- [[citation-discipline]] — Sky's structure-of-disclaimers stance contrasts sharply with Circle's transparency claims; illustrates that citation discipline at the issuer layer is not universal.
- [[proof-of-reserves]] — open question whether Sky Protocol has a proof-of-reserves equivalent surfaced anywhere; the landing page does not.
- [[counterparty-graph-research]] — Sky's named counterparties (Skybase, "Sky Agents," "Sky Ecosystem partners") are not characterized as named legal entities or regulated firms in the way Circle's are.

## Vendors discussed

- [[sky-protocol]] — primary subject of the source.

## Sectors touched

- [[stablecoin-issuers]] — Sky is the wiki's first DeFi-native issuer, contrasting with Circle's centralized-issuer archetype.

## Notable quotes

> "Sky.money is a non-custodial interface operated by Skybase, an independent Sky Agent with no control over Sky Protocol smart contracts or ecosystem governance."

> "The Sky Savings Rate and all other protocol parameters are determined through decentralized governance by SKY tokenholders and are subject to change or elimination at any time."

> "Sky.money does not control, set, or guarantee the rate."

> "Skybase does not participate in, and has no ability to control or guarantee outcomes of, decentralized governance processes."

> "SKY is a decentralized governance token of Sky Protocol. It is not a security, investment contract, or financial instrument."

## Open questions raised

- **What backs USDS?** Specific collateral composition (on-chain crypto, RWAs, USDC peg-stability module, percentages) is not surfaced on the landing page. **High priority** for any institutional buyer.
- **Is there a proof-of-reserves equivalent?** Circle has weekly + monthly attestations; the Sky landing page does not describe an analogous transparency mechanism. Is one published elsewhere (chainlog, info dashboard) or is "the contracts are on-chain, look for yourself" the structural answer?
- **Does Sky Protocol have any regulatory licenses or registrations?** The page does not surface any. The "currently unavailable in the US" restriction implies geofencing without explaining the legal basis.
- **Rebrand history from MakerDAO.** Widely known in the public domain. The Sky landing page does not state it. A historical-source ingest (e.g. an Endgame plan document if it becomes accessible) would substantively develop the rebrand timeline.
- **The "Stars" / sub-DAO structure.** Referenced in pre-rebrand MakerDAO Endgame literature. The Sky landing page references "Sky Agents" and "Sky Ecosystem partners" without defining a formal governance role. Future ingest needed.
- **MiCA EMT classification.** USDS is single-USD-pegged → structurally an [[e-money-token|EMT-archetype]] under MiCA framing. The landing page does not address EU registration or the geographic-restriction reasoning.

## External references

- Sky Protocol governance voting — https://vote.sky.money/
- Community forum — https://forum.sky.money/ and https://forum.skyeco.com/
- Github — https://github.com/sky-ecosystem
- Developer portal — https://developers.skyeco.com/ (navigation-only at the homepage; substantive sub-pages exist)
- Chainlog (canonical contract registry) — https://chainlog.sky.money/
- Info dashboard — https://info.skyeco.com/ (JS-rendered, fetcher could not extract content during this ingest)
- Legal docs — https://docs.sky.money/legal/skybase-international/

## Cross-references

- [[vendor-circle-transparency-page-2026-04]] — direct architectural contrast: Circle is centralized, named-licensed, attested; Sky is DeFi-native, structurally-disclaimed, geographically-restricted.
- [[regulator-eu-mica-esma-hub]] — the EU regulatory frame USDS would fall under as an EMT-archetype if registered; Sky's landing page does not address it.
- [[51-deck-april-2026]] — the deck names "Stablecoin Issuer" as a research category; the Sky vs. Circle contrast is exactly the kind of comparison institutional buyers do within that category.
