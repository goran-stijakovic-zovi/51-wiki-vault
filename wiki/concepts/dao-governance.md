---
type: concept
name: DAO governance
sources: 1
last_updated: 2026-04-27
---

# DAO governance

> *Decentralized governance of a smart-contract protocol via tokenholder voting. Protocol parameters — rates, fees, collateral types, treasury allocation — are determined by votes weighted by token holdings rather than by corporate decision.*

## What it means

A "DAO" (decentralized autonomous organization) governance model is the structural alternative to corporate governance in DeFi-native protocols. Instead of a board of directors, executive team, and shareholders setting policy, the protocol's parameters are set by **tokenholder votes** — typically with one token equaling one vote, sometimes with delegation, time-weighting, or quadratic-voting modifications.

For [[sky-protocol|Sky Protocol]], the governance token is **SKY**, and the canonical structural framing on the public landing page is: "The Sky Savings Rate and all other protocol parameters are determined through decentralized governance by SKY tokenholders and are subject to change or elimination at any time."

The institutional-buyer diligence question is **not** whether DAO governance is better or worse than corporate governance; it is **what risks the DAO model introduces that corporate models don't have**, and how those risks are mitigated. The risks include governance capture (a single tokenholder or coalition acquiring majority voting power), governance attacks (flash-loan-based vote manipulation), parameter changes that materially affect token value (rate changes, collateral additions/removals, treasury reallocation), and quorum failure (insufficient participation to pass needed changes).

## How it shows up in sources

- [[vendor-sky-money-landing-2026-04]] — Sky.money's landing page articulates the model explicitly: "The Sky Savings Rate and all other protocol parameters are determined through decentralized governance by SKY tokenholders." Plus structural disclaimers: "Skybase does not participate in, and has no ability to control or guarantee outcomes of, decentralized governance processes."

## Mechanism / how it works

A working DAO governance regime typically has:

1. **A governance token** with voting rights — Sky uses SKY.
2. **Voting mechanics** — proposal submission, voting period, quorum threshold, execution mechanism. (Not detailed on the Sky landing page; would require ingest of vote.sky.money or governance forum posts.)
3. **Treasury control** — the DAO governs a treasury that funds protocol development, security, RWA holdings, etc. (Sky's treasury structure not detailed on the landing page.)
4. **Smart-contract execution** — passed proposals execute via on-chain "spell" contracts that implement parameter changes deterministically.

The structural property that distinguishes DAO governance from corporate governance is that **changes are public, on-chain, and deterministic**. A corporate parameter change is announced after the fact; a DAO parameter change is a public proposal, voted on visibly, executed visibly. This is the DeFi-native analogue of [[citation-discipline]] — every protocol change has an on-chain provenance trail.

Sky's landing page emphasizes the "subject to change or elimination at any time" framing, which is the institutional-buyer warning: parameter stability cannot be assumed even when current parameters are favorable.

## Related concepts

- [[non-custodial-interface-vs-issuer]] — the architectural pattern that DAO governance enables.
- [[citation-discipline]] — DAO governance produces on-chain provenance for every parameter change; the analogous discipline at the protocol layer.
- [[counterparty-graph-research]] — DAO-governed protocols have a different counterparty surface (tokenholders, governance delegators, oracle providers) than corporate-governed issuers.

## Related vendors / sectors

- [[sky-protocol]] — canonical example in this wiki; SKY is the governance token.
- [[stablecoin-issuers]] — sector where DAO governance is structurally consequential for institutional buyers.

## Open questions

- **Sky's specific governance mechanics.** The landing page does not detail proposal-submission rules, quorum thresholds, time-locks, or execution mechanisms. A follow-up source (vote.sky.money documentation, governance forum) would substantively develop these.
- **Governance capture risks.** What's the SKY tokenholder concentration profile? Are there major holders who could pass proposals unilaterally? Open public-source ingest territory.
- **The "Stars" / sub-DAO structure.** Pre-rebrand MakerDAO introduced a sub-DAO governance hierarchy in the Endgame plan. Sky's continuity with or departure from this structure is not addressed on the landing page.
- **Comparison to non-DAO-but-tokenized models.** Some protocols have token-based governance that's structurally non-DAO (e.g. signal-only voting with the corporate entity retaining authority). The wiki may benefit from a `governance-token-vs-decision-rights` concept page if a relevant source enters.

## Sources cited

- [[vendor-sky-money-landing-2026-04]]
