---
type: concept
name: Qualified custodian
sources: 1
last_updated: 2026-04-27
---

# Qualified custodian

> *US federal regulatory status that determines who may hold custody of client assets on behalf of SEC-registered investment advisers under the Investment Advisers Act of 1940 (Rule 206(4)-2). Recognized qualified custodians include banks, trust companies, broker-dealers, futures commission merchants, and certain foreign institutions.*

## What it means

When a US-based investment adviser registered with the Securities and Exchange Commission (SEC) holds client assets, the **Custody Rule** (Rule 206(4)-2 under the Investment Advisers Act of 1940) requires those assets to be held by a **qualified custodian** — not by the adviser itself. This is one of the most consequential federal regulatory definitions for the [[custody]] sector: any custody vendor that wants to serve SEC-registered investment-adviser clients must qualify under this rule.

For a digital-asset custodian, qualified-custodian status typically requires holding one of the following federal authorisations: a national-bank charter (including [[occ-national-trust-bank-charter|OCC national trust bank charters]]), a broker-dealer registration, a futures commission merchant registration, or in some cases a state-level trust charter that is recognized by the SEC as equivalent. The vendor's "Qualified Custody" product typically refers to this regulatory capacity.

For an institutional buyer — particularly an SEC-registered RIA, family office acting under advisory rules, or asset manager managing pooled vehicles for US clients — qualified-custodian status is **a first-order screening criterion**. A custody vendor lacking qualified-custodian status cannot serve these clients for the regulated portion of their custody needs.

## How it shows up in sources

- [[vendor-bitgo-homepage-2026-04]] — BitGo's homepage product taxonomy distinguishes "Self-Custody" from "Qualified Custody" — the latter being the institutional-buyer offering aligned with the federal qualified-custodian definition. The homepage doesn't elaborate the rule's specific requirements but uses "Qualified Custody" as a standard product category.

## Mechanism / how it works

**Statutory basis**: Rule 206(4)-2 under the Investment Advisers Act of 1940 ("the Custody Rule"). The rule defines who may hold custody of advisory client assets and what disclosures and audit requirements apply when an adviser does have custody.

**Qualified custodian categories** (per the rule, paraphrased — the wiki's source does not reproduce statutory text):

- US banks (as defined in the Investment Advisers Act).
- Broker-dealers registered under the Securities Exchange Act.
- Futures commission merchants registered under the Commodity Exchange Act.
- Certain foreign financial institutions.

National trust banks — including those holding [[occ-national-trust-bank-charter|OCC national trust bank charters]] — generally qualify as banks under the Investment Advisers Act definition.

**State trust charter equivalence**: state-chartered trust companies may qualify as banks under specific conditions; this is one of the structural reasons digital-asset custodians have pursued state trust charters (e.g. [[limited-purpose-trust-charter|NYDFS Limited Purpose Trust Charter]]) before or alongside federal charters. The specific equivalence is not detailed on the BitGo homepage and remains an open question for future regulator-side ingest.

**Surrounding rule mechanics** (paraphrased; not reproduced verbatim from this wiki's sources):

- The investment adviser must reasonably believe that the qualified custodian sends quarterly statements directly to clients.
- Annual surprise audits are required for advisers holding client assets.
- "Custody" includes any arrangement under which the adviser has access to client funds or securities.

These mechanics are noted as context; substantive ingest of SEC rule-side material would be needed to develop them into a wiki concept page in their own right.

## Related concepts

- [[occ-national-trust-bank-charter]] — federal banking authorisation that meets the qualified-custodian definition.
- [[limited-purpose-trust-charter]] — state-level trust authorisation; equivalence to qualified-custodian status varies and is one of the structural reasons custody vendors pursue this path.
- [[bitlicense]] — does NOT meet qualified-custodian status by itself; BitLicensees that need qualified-custodian status typically pursue a parallel banking / trust-charter path.
- [[citation-discipline]] — qualified-custodian status is one of the canonical citation surfaces in custody-vendor diligence (the federal authorisation is itself a citable regulatory fact).
- [[counterparty-graph-research]] — qualified-custodian status surfaces specific named regulators (SEC, OCC, state banking regulators) as counterparties in vendor graphs.

## Related vendors / sectors

- [[custody]] — sector where this status is most consequential.
- [[bitgo]] — wiki's first vendor explicitly using "Qualified Custody" as a product category.

## Open questions

- **Substantive content of Rule 206(4)-2.** This wiki's source references the qualified-custodian concept but does not reproduce the rule's specific requirements (surprise-audit cadence, statement-delivery requirements, custody-definition scope). Future ingest of SEC rule-side material would substantively develop this page.
- **Investment Advisers Act 2023 amendments.** The SEC has proposed amendments to the Custody Rule (now sometimes called the "Safeguarding Rule"). Whether these amendments are in force as of 2026-04-27 and how they apply to digital-asset custody is not addressed in the current sources. Future ingest territory.
- **Federal qualified-custodian status for state trust companies.** The structural-equivalence question between [[limited-purpose-trust-charter|NYDFS Limited Purpose Trust Charter]] holders and the federal definition needs source-side development.
- **Other custodians with qualified-custodian status.** Anchorage Digital, Coinbase Custody, Fidelity Digital Assets, BNY Mellon (for digital assets), State Street (for digital assets) — most are not currently in the wiki. Future ingest territory.

## Sources cited

- [[vendor-bitgo-homepage-2026-04]]
