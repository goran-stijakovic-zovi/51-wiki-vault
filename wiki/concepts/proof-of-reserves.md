---
type: concept
name: Proof of reserves
sources: 2
last_updated: 2026-04-27
---

# Proof of reserves

> *The structural transparency primitive for centrally-issued stablecoins: a disclosure regime in which the issuer publicly demonstrates that reserve assets meet or exceed circulating supply, typically through a combination of self-published holdings reports and independent third-party attestations.*

## What it means

For a centralized fiat-pegged stablecoin issuer (USDC, USDT, EURC, USDP, etc.), the institutional-buyer trust question is binary: **are the reserves real, are they sufficient, and is the disclosure verifiable by an independent party?** Proof of reserves is the structural mechanism by which an issuer answers this question continuously, not just at a single point in time.

A robust proof-of-reserves regime typically combines:

- **Self-published holdings reports** at high cadence (weekly or daily) — telling buyers what the issuer says it holds.
- **Independent third-party attestations** at lower cadence (typically monthly) — telling buyers an independent accounting firm has verified that the reserves exceed circulating supply.
- **A regulator-grounded reserve vehicle** where possible — e.g. an SEC-registered money market fund, a bank trust account, an OCC-supervised national trust company — which adds a third layer of regulatory transparency on top of the self-published and attested layers.
- **A long disclosure history** — multi-year continuity that demonstrates the regime is operational, not aspirational.

The institutional-buyer screen is *not* whether a single attestation exists; it is whether the regime has been continuously operated, by named auditors, with public access to the underlying reports.

## How it shows up in sources

- [[vendor-circle-transparency-page-2026-04]] — Circle's transparency page is a canonical implementation. The page articulates a two-tier cadence (weekly self-published holdings + mint/burn flows, plus monthly Big Four attestation under AICPA standards), names the current independent auditor ([[deloitte]] since fiscal 2022; previously Grant Thornton LLP from 2015), references the [[2a-7-government-money-market-fund|SEC-registered Circle Reserve Fund]] as the reserve vehicle, and points to a continuous reporting history since 2018.
- [[vendor-sky-money-landing-2026-04]] — **negative finding**. Sky Protocol's public landing page does NOT surface a proof-of-reserves equivalent. No weekly holdings disclosure, no monthly attestation, no audit firm named, no regulator-grounded reserve vehicle described. The architectural contrast with Circle is structural: where centralized issuers use proof-of-reserves regimes as the institutional-buyer trust mechanism, DeFi-native protocols rely on on-chain visibility ("the contracts are public, verify yourself") plus structural disclaimers from the interface operator ([[non-custodial-interface-vs-issuer]]). Whether this constitutes a different *kind* of citation discipline or a different *standard* for transparency is an open question — see below.

## Mechanism / how it works

A working proof-of-reserves regime has four structural components:

1. **Reserve composition policy** — a public commitment about what kinds of assets back the token. Cash deposits, short-dated Treasury bills, overnight repos, money market fund holdings are typical low-risk components. Riskier components (corporate paper, longer-duration assets, non-cash collateral) introduce reserve-quality risk that's distinct from reserve-sufficiency risk.

2. **Self-published holdings reports at high cadence** — telling buyers what the issuer says it holds, between attestations. Circle's weekly disclosure is a canonical example.

3. **Independent third-party attestation at lower cadence** — typically monthly. The attestation does not validate the issuer's business; it validates the **arithmetic claim** that reserve value at a snapshot date exceeded circulating supply. Attestation standards (AICPA in the US) define how this arithmetic is checked. The attestation firm's identity (Big Four vs. mid-tier vs. specialty) is itself a signal of the regime's seriousness.

4. **Regulator-grounded reserve vehicle (optional but strong)** — when reserves sit inside a regulated structure (SEC-registered MMF, bank trust account, OCC-supervised institution), the issuer inherits the regulatory transparency of that vehicle. Circle's USDXX-via-BlackRock is a strong example.

The regime's robustness compounds with time. A monthly attestation from 2018 onward is structurally stronger than three monthly attestations starting last quarter, even if the latest snapshot looks identical — because the long history demonstrates regime operation under stress (March 2023 USDC SVB depeg event, etc.) rather than in narrow steady-state conditions.

## Distinction from "Merkle-proof-of-reserves"

This concept covers *fiat-pegged stablecoin* proof of reserves. A separate but related concept — Merkle-tree proof-of-reserves used by some crypto exchanges to demonstrate solvency over user-held crypto deposits — has different mechanics (cryptographic Merkle inclusion proofs of liability ledger entries) and is out of scope for the stablecoin-issuer use case here. May warrant a separate concept page when a relevant source enters the wiki.

## Related concepts

- [[citation-discipline]] — proof-of-reserves regimes are one of the canonical institutional implementations of structural citation discipline.
- [[2a-7-government-money-market-fund]] — a structural component of Circle's regime; the regulator-grounded reserve vehicle.
- [[e-money-token]] — under MiCA, EMT issuers face Title IV reserve requirements; proof-of-reserves regimes inherited from US disclosure practice are conceptually adjacent but not equivalent.
- [[asset-referenced-token]] — under MiCA, ART issuers face Title III reserve obligations; multi-reference issuers face structurally different reserve composition questions than single-fiat issuers.
- [[counterparty-graph-research]] — proof-of-reserves regimes surface the named auditor, named fund manager, named depository banks, named regulators — a graph-traversal target.

## Related vendors / sectors

- [[stablecoin-issuers]] — proof-of-reserves is a sector-defining transparency primitive for centralized issuers; not universal in DeFi-native protocols.
- [[circle]] — canonical large-issuer implementation.
- [[sky-protocol]] — counter-example: a DeFi-native issuer whose public landing page does not surface a proof-of-reserves regime.

## Open questions

- **What's the equivalent transparency primitive for [[asset-referenced-token|ART]] issuers?** Multi-reference tokens (basket-pegged, commodity-pegged) face different reserve-composition questions. Future ingest of an ART-issuer source would substantively develop this.
- **What's the equivalent for DeFi-native issuers** like [[sky-protocol|Sky Protocol]]? **Partial answer from source 5**: Sky's public landing page does not surface any analogous regime. The DeFi-native model relies on on-chain visibility plus interface-operator disclaimers, which is *not* a proof-of-reserves regime in the centralized-issuer sense. **Whether on-chain visibility constitutes a different *kind* of transparency primitive** (and whether it's adequate for institutional-buyer diligence) is itself an institutional-procurement question. Future ingest of Sky's developer portal, chainlog, or governance forum would establish whether transparency mechanisms exist at a layer the landing page doesn't surface.
- **The "reserve quality" dimension** — beyond sufficiency (reserves > circulating), there's a second axis of how risky/illiquid the reserve composition is. Different stablecoin issuers make different choices (cash + Treasuries vs. corporate paper vs. long-duration bonds). The wiki's seed-source list does not include direct ingest on this axis; future sources may.

## Sources cited

- [[vendor-circle-transparency-page-2026-04]]
- [[vendor-sky-money-landing-2026-04]]
