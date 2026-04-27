---
type: concept
name: KYT (Know Your Transaction)
sources: 1
last_updated: 2026-04-27
---

# KYT (Know Your Transaction)

> *Real-time blockchain transaction screening for compliance purposes. The canonical compliance-vendor product category that turns regulator transaction-monitoring requirements (NYDFS 23 NYCRR Part 504, FATF Travel Rule, AML) into operational capability for digital-asset operators.*

## What it means

KYT — by analogy to the older KYC (Know Your Customer) standard — is the digital-asset compliance discipline of **screening every transaction in real time** rather than every customer at onboarding. For a digital-asset operator (exchange, custody vendor, stablecoin issuer, payment processor), KYT is the operational layer that satisfies regulator obligations to:

- Detect transactions to/from sanctioned addresses.
- Flag transactions associated with illicit activity (mixers, ransomware, scam infrastructure).
- Generate alerts for suspicious patterns (rapid layering, structured deposits, etc.).
- Produce audit trails defensible to regulators and (where applicable) courts.

KYT is structurally distinct from KYC: KYC happens once at customer onboarding; KYT happens continuously across every transaction the customer originates or receives. For institutional digital-asset operators, the two together constitute the standard AML compliance stack.

## How it shows up in sources

- [[vendor-chainalysis-homepage-2026-04]] — Chainalysis names its KYT product explicitly: "Ensure compliance and prevent illicit activity with continuous and real-time screening of crypto transactions." KYT is one of three primary product categories on Chainalysis's homepage (alongside Reactor for investigation and Risk Assessment products for wallet/VASP/token-level risk).

## Mechanism / how it works

A working KYT regime has four operational components (synthesized from the Chainalysis source; not directly enumerated on the homepage):

1. **Real-time integration with the operator's transaction flow** — the compliance vendor's API ingests every transaction at the moment it's submitted (or shortly after), not in batch hours later.

2. **Address-level risk assessment** — the vendor's [[on-chain-analytics]] engine maps the counterparty addresses to entity clusters (sanctioned entity, exchange, mixer, ransomware, scam, etc.) using clustering heuristics + ML. Output: a risk score / category for each transaction's counterparty.

3. **Threshold-based alerting** — the operator's compliance team is alerted when transactions exceed pre-configured risk thresholds, triggering manual review or automated holds.

4. **Audit trail generation** — every screening decision and alert is logged in a regulator-defensible format. Where the underlying data comes from a vendor like Chainalysis with court-admissibility positioning, the trail is designed to support enforcement actions.

The output of a KYT system is regulator-facing: the operator must be able to demonstrate to its regulator (NYDFS, ESMA, etc.) that it has continuous transaction-monitoring in place that meets the regulator's expectations.

## Related concepts

- [[on-chain-analytics]] — the technical primitive on which KYT is built.
- [[bitlicense]] — NYDFS 23 NYCRR Part 504 (Transaction Monitoring and Filtering Program Requirements) is the canonical US-state regulatory anchor that drives BitLicensees and Trust Charter holders to deploy KYT systems.
- [[mica-compliance]] — MiCA Title V CASP supervisory obligations include transaction monitoring; KYT is one operational implementation.
- [[citation-discipline]] — KYT outputs are designed to be regulator-defensible and (in some vendor's positioning) court-admissible, which is structural citation discipline at the compliance-vendor product layer.
- [[counterparty-graph-research]] — KYT is itself a counterparty-graph operation: every transaction reveals two graph endpoints (the operator's customer and the external counterparty); KYT classifies both sides at scale.

## Related vendors / sectors

- [[regulatory-and-compliance]] — sector where KYT is the canonical product category.
- [[chainalysis]] — wiki's canonical KYT vendor.
- [[stablecoin-issuers]] — issuers use KYT for sanctions-screening on stablecoin transfers (Tether named as a Chainalysis customer).
- [[custody]] — custodians use KYT for AML monitoring on inbound deposits.
- [[payment-and-settlement]] — exchanges and on/off-ramps use KYT for travel-rule compliance and AML monitoring.

## Open questions

- **The boundary between KYT and KYC.** As digital-asset compliance evolves, the integration between KYT (per-transaction) and KYC (per-customer) is increasingly continuous; institutional-grade compliance stacks may not treat the two as separable. Future ingest territory.
- **Travel Rule implementation via KYT.** FATF Recommendation 16 (Travel Rule) imposes specific data-sharing requirements between VASPs for transactions above thresholds. How KYT systems coordinate Travel Rule data exchange is an operational detail not covered by the current sources.
- **Comparison across compliance vendors.** Chainalysis is the wiki's canonical example; TRM Labs, Elliptic, CipherTrace (named on [[51-deck-april-2026]]) are not yet in the wiki. Substantive comparison would benefit from future ingests.

## Sources cited

- [[vendor-chainalysis-homepage-2026-04]]
