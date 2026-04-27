---
type: vendor
name: Sky Protocol
sector: [[stablecoin-issuers]]
role: stablecoin-issuer
public_status: []
aliases: [makerdao]
sources: 1
last_updated: 2026-04-27
---

# Sky Protocol

> *DeFi-native stablecoin protocol issuing USDS (single-USD-pegged), sUSDS (yield-generating), stUSDS (risk-capital), and SKY (governance). Architecturally distinct from Circle: smart-contract-governed by SKY tokenholders, with the public interface operated by a separate non-custodial entity (Skybase International) that explicitly disclaims control over the protocol.*

## What it is

Sky Protocol is a DeFi-native stablecoin ecosystem governed by SKY tokenholders. Its primary stablecoin is **USDS**, single-USD-pegged. Around USDS sit three additional tokens: **sUSDS** (yield-generating savings token earning the Sky Savings Rate), **stUSDS** (high-performance risk-capital token providing liquidity for SKY-backed borrowing), and **SKY** (the governance token). The public interface at `sky.money` is operated by **[[skybase-international]]**, an "independent Sky Agent" that explicitly disclaims control over Sky Protocol smart contracts or governance.

The architecture is **the contrast** with [[circle|Circle]] in this wiki: Circle is a single regulated legal entity with named US + Bermuda licenses, named auditor (Deloitte), and a regulator-grounded reserve vehicle (SEC-registered 2a-7 MMF managed by BlackRock); Sky is a smart-contract protocol with decentralized governance, no surfaced regulatory licenses, no surfaced audit firm, and structural disclaimers from the interface operator.

**Aliases note**: this vendor's prior identity as **MakerDAO** is widely documented in the public domain (the rebrand was part of MakerDAO's "Endgame" plan). The Sky.money landing page itself does NOT mention the MakerDAO history; the `aliases: [makerdao]` frontmatter field is set as a structural identity tag with this body note that the rebrand attribution is from outside the immediate source. A future source ingest (Endgame plan document, governance forum post) would establish the rebrand history within the wiki's source layer.

## Sector position

- Sector: [[stablecoin-issuers]]
- Role: stablecoin-issuer
- Differentiation framing: DeFi-native, smart-contract-governed, single-USD-pegged. Architecturally distinct from centralized issuers like [[circle]] in three load-bearing ways: (1) governance is decentralized via SKY tokenholders rather than corporate; (2) the public interface is operated by a separate non-custodial entity that disclaims control; (3) regulatory licenses and audit relationships are not surfaced on the public-facing page.

## Public moves cited

- [[vendor-sky-money-landing-2026-04]] — public landing page articulating the four-token product family (USDS, sUSDS, stUSDS, SKY), the Skybase / Sky Protocol structural separation, the decentralized-governance disclaimers, and the geographic restriction "currently unavailable in the US" for sUSDS and stUSDS without stated legal basis.

## Public regulatory status

_Sourced specifically from the cited source pages._

- **No regulatory licenses surfaced** on the Sky.money landing page. Empty `public_status:` is itself a finding when contrasted with [[circle]]'s populated list (NYDFS Money Transmitter, NYDFS VCBA, BMA Digital Asset Business).
- **Geographic restriction**: sUSDS, stUSDS, and Sky Ecosystem Rewards display "currently unavailable in the US" without stated legal basis. The wiki characterizes this as an implicit regulatory signal but does not infer specific regulator jurisdiction.
- **MiCA registration status: not surfaced.** USDS is single-USD-pegged → [[e-money-token|EMT-archetype]] under MiCA framing structurally. Whether Sky Protocol or any associated legal entity is MiCA-registered is an open question.
- **No audit firm named** on the public-facing source. Contrasts with Circle's [[deloitte]] disclosure.

## Concepts cited

- [[non-custodial-interface-vs-issuer]] — the architectural separation between Skybase (interface) and Sky Protocol (smart contracts) as a domain primitive.
- [[dao-governance]] — decentralized governance via SKY tokenholders; the governance model that contrasts with Circle's corporate model.
- [[e-money-token]] — USDS is single-USD-pegged → EMT-archetype under MiCA framing.
- [[proof-of-reserves]] — Sky's landing page does not surface a proof-of-reserves equivalent; whether one exists in the developer portal / chainlog / info dashboard is an open question.
- [[citation-discipline]] — the Sky landing page's structure-of-disclaimers stance illustrates that citation discipline at the issuer layer is not universal in DeFi-native protocols.

## Counterparties cited

- [[skybase-international]] — operator of the sky.money public interface; an "independent Sky Agent" that disclaims control over Sky Protocol smart contracts and governance.

## Open questions

- **What backs USDS?** Collateral composition (on-chain crypto, RWAs, USDC peg-stability module, percentages) is not surfaced on the landing page. **Highest-priority open question.** A follow-up source from the developer portal or chainlog would resolve.
- **Proof-of-reserves equivalent.** Circle has weekly + monthly attestations under AICPA standards; Sky's analogous transparency mechanism is not described on the landing page.
- **Audit firm relationship.** None named.
- **MiCA registration status as of 2026-04.** Not surfaced. Open question parallel to the Circle MiCA question.
- **The "Stars" / sub-DAO governance structure.** The pre-rebrand MakerDAO Endgame plan introduced "Stars" as governance sub-units; whether Sky retains this structure is not addressed on the landing page.
- **Real-world asset (RWA) exposure.** Pre-rebrand MakerDAO had substantial tokenized-Treasury and credit-facility exposure (Monetalis/Clydesdale, BlockTower); Sky's continued or evolved RWA exposure is not surfaced on the landing page.
- **The legal basis for the "currently unavailable in the US" geographic restriction.** Implicit compliance measure without stated reasoning.

## Sources cited

- [[vendor-sky-money-landing-2026-04]]
