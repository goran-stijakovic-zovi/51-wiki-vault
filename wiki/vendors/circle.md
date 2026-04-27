---
type: vendor
name: Circle
sector: [[stablecoin-issuers]]
role: stablecoin-issuer
public_status: ["NYDFS-Money-Transmitter (Circle Internet Financial, LLC)", "NYDFS-VCBA (Circle Internet Financial, LLC)", "BMA-Digital-Asset-Business (Circle International Bermuda Limited)"]
sources: 1
last_updated: 2026-04-27
---

# Circle

> *Centralized USD- and EUR-pegged stablecoin issuer (USDC, EURC). Defining structural commitment: 1:1 redemption guarantee backed by 100% cash-and-cash-equivalent reserves, with the majority held in an SEC-registered 2a-7 government money market fund managed by BlackRock and a Big Four monthly attestation cadence going back to 2018.*

## What it is

Circle is a US-rooted digital-dollar issuer operating two principal stablecoins: **USDC** (US-dollar-pegged) and **EURC** (euro-pegged). Both are single-fiat-pegged tokens with a 1:1 redemption guarantee. Circle's institutional positioning rests on three structural pillars: a regulator-grounded reserve vehicle ([[2a-7-government-money-market-fund|the SEC-registered 2a-7 Circle Reserve Fund / USDXX]] managed by [[blackrock]]), a two-tier disclosure cadence (weekly Circle self-published holdings + monthly Big Four attestation under AICPA standards), and a long disclosure history (reports on all reserve assets since 2018, longer than most centralized stablecoin issuers).

For institutional buyers, Circle is the canonical large-issuer counterparty in the [[stablecoin-issuers]] sector — high disclosure cadence, regulator-grounded reserve vehicle, named audit firm, multiple US and Bermuda regulatory licenses.

## Sector position

- Sector: [[stablecoin-issuers]]
- Role: stablecoin-issuer
- Differentiation framing: a single-fiat-pegged ([[e-money-token|EMT-archetype]] under MiCA framing) issuer with a regulator-grounded reserve vehicle (SEC-registered 2a-7 MMF managed by BlackRock) and one of the longest reserve-disclosure histories in the sector (reports since 2018).

## Public moves cited

- [[vendor-circle-transparency-page-2026-04]] — Circle's public transparency page articulating the 1:1 redemption guarantee, 100% cash/cash-equivalent backing, the Circle Reserve Fund (USDXX), the weekly + monthly disclosure cadence, the Deloitte audit relationship since fiscal 2022 (Grant Thornton previously from 2015), and explicit US (NYDFS) + Bermuda (BMA) regulatory licenses.

## Public regulatory status

_Sourced specifically from the cited source pages._

- **NYDFS Money Transmitter license** (Circle Internet Financial, LLC) — sourced from [[vendor-circle-transparency-page-2026-04]] (footer text). Cross-confirmation pending from [[regulator-nydfs-bitlicense-list]] (source 6).
- **NYDFS Virtual Currency Business Activity (VCBA) license** (Circle Internet Financial, LLC) — sourced from [[vendor-circle-transparency-page-2026-04]] (footer text). Cross-confirmation pending from [[regulator-nydfs-bitlicense-list]] (source 6).
- **BMA Digital Asset Business license** (Circle International Bermuda Limited) — sourced from [[vendor-circle-transparency-page-2026-04]] (footer text).
- **SEC-registered 2a-7 government money market fund** (Circle Reserve Fund / USDXX) — sourced from [[vendor-circle-transparency-page-2026-04]]. Note: this is the *fund* vehicle's regulatory status; the relationship to Circle is "Circle manages USDXX via BlackRock as fund manager." Captured in `public_status:` frontmatter as a Circle-relevant structural fact, with the body documenting the nuance.
- **MiCA registration status: not surfaced on Circle's transparency page.** This is an open question (see below). Vendor `public_status:` is NOT populated with any MiCA value here under the schema's source-driven discipline.

## Concepts cited

- [[proof-of-reserves]] — Circle's defining structural commitment; the two-tier disclosure cadence is a canonical implementation.
- [[2a-7-government-money-market-fund]] — the US-securities-law structure underpinning the majority of Circle's reserves.
- [[e-money-token]] — Circle is single-USD-pegged → EMT-archetype issuer under MiCA framing, even though MiCA registration is not surfaced on Circle's transparency page.
- [[citation-discipline]] — Circle's weekly + monthly + AICPA-attested disclosure regime is one of the canonical institutional implementations of structural citation discipline at the issuer layer.
- [[counterparty-graph-research]] — Circle's named partners (BlackRock as fund manager, Deloitte as auditor, NYDFS and BMA as regulators) are graph-traversal targets.
- [[crypto-asset-white-paper]] — open question: Circle does not surface a MiCA white paper on its transparency page; EU-side disclosure status is unclear.

## Counterparties cited

- [[blackrock]] — manager of the Circle Reserve Fund (USDXX). Sourced from [[vendor-circle-transparency-page-2026-04]].
- [[deloitte]] — independent auditor since fiscal 2022. Sourced from [[vendor-circle-transparency-page-2026-04]].
- [[nydfs]] — Money Transmitter and VCBA license issuer. _(Page emerges from source 6.)_
- [[bma]] — Bermuda Monetary Authority; Digital Asset Business license issuer (Circle International Bermuda Limited). Currently mentioned only in the body of this page; firm page deferred until a second source touches it.

## Open questions

- **MiCA registration status as of 2026-04.** The transparency page does not surface it. Does Circle have an EU subsidiary registered as an EMT issuer under MiCA Title IV? A follow-up source (Circle's EU regulatory disclosure or the ESMA register snapshot) would resolve this. **High priority** for an institutional buyer doing EU-jurisdiction diligence.
- **Named cash-component depository banks.** Circle's transparency page describes them generically as "leading global banks" without naming them. Other Circle disclosures (SEC filings, monthly attestations themselves) may name them.
- **Post-March-2023 (SVB depeg) bank-counterparty disclosure regime.** USDC briefly depegged in March 2023 when ~$3.3B of cash reserves at Silicon Valley Bank were temporarily inaccessible. The current transparency page does not discuss the SVB episode explicitly — has bank-counterparty disclosure changed since then? Follow-up source to consider.

## Sources cited

- [[vendor-circle-transparency-page-2026-04]]
