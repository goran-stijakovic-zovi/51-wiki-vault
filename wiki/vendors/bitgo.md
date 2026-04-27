---
type: vendor
name: BitGo
sector: [[custody]]
role: custodian
public_status: ["NYDFS-Limited-Purpose-Trust-Charter (BitGo New York Trust Company, LLC, since 2021-03)", "OCC-National-Trust-Bank-Charter (BitGo Bank & Trust, National Association)"]
sources: 2
last_updated: 2026-04-27
---

# BitGo

> *Institutional digital-asset custody and infrastructure provider; first vendor in the wiki's [[custody]] sector. Operates a multi-jurisdictional subsidiary structure mapping different regulatory regimes to different entities — recently secured an OCC federal national trust bank charter, retains its NYDFS Limited Purpose Trust Charter through BitGo New York Trust Company, LLC since 2021-03.*

## What it is

BitGo is the wiki's first [[custody]]-sector vendor. The corporate structure surfaced on its public homepage is: **BitGo Holdings, Inc.** (Delaware corporation, headquartered in Sioux Falls, South Dakota) is the parent. **BitGo Bank & Trust, National Association** is the federally-chartered subsidiary regulated by the **[[occ|Office of the Comptroller of the Currency]]**. Per the NYDFS Regulated Entities list, **BitGo New York Trust Company, LLC** holds the NYDFS Limited Purpose Trust Charter since 2021-03.

BitGo positions itself as "the digital asset infrastructure company" with five service categories: Prime Services (liquidity and capital), Ecosystem (launch / manage / grow), Stablecoins (hold / swap / manage / issue), Wallet Services, and Crypto-as-a-Service. Product taxonomy includes Hot Wallets, Cold Wallets, Self-Custody, and Qualified Custody — the last is the institutional-buyer-targeted offering aligned with US federal [[qualified-custodian]] rules.

The structural distinction from [[circle]] in this wiki: where Circle is a single-issuer model (issuing USDC and EURC under a centralized regime with named auditor and SEC-registered reserve vehicle), BitGo is a multi-service custody-and-infrastructure model targeting institutional buyers and B2B clients (including stablecoin issuers using BitGo for reserve custody, exchanges using BitGo for treasury custody, etc.). Both vendors use multi-entity subsidiary structures with regulator-mapped subsidiaries.

## Sector position

- Sector: [[custody]]
- Role: custodian
- Differentiation framing: institutional-grade qualified-custody operator with both state-level (NYDFS Limited Purpose Trust Charter) and federal-level (OCC national trust bank charter) regulatory paths in the US. Multi-product surface (hot wallets, cold wallets, self-custody, qualified custody) plus B2B services (Prime / Ecosystem / Stablecoin tools / CaaS).

## Public moves cited

- [[vendor-bitgo-homepage-2026-04]] — BitGo's public homepage articulating the OCC national trust bank charter approval, the corporate structure (BitGo Holdings, Inc. → BitGo Bank & Trust N.A.), the five service categories, the wallet-product taxonomy (Hot / Cold / Self-Custody / Qualified Custody), and the explicit non-FDIC/SIPC disclosure.
- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS regulator-side cross-confirmation: BitGo New York Trust Company, LLC holds the Limited Purpose Trust Charter since 2021-03.

## Public regulatory status

_Sourced specifically from the cited source pages._

- **NYDFS Limited Purpose Trust Charter** (BitGo New York Trust Company, LLC, since 2021-03) — sourced from [[regulator-nydfs-bitlicense-page-2026-04]] (Regulated Entities list). Per [[limited-purpose-trust-charter]]: this charter authorizes virtual-currency business activity AND money transmission AND fiduciary powers under New York Banking Law.
- **OCC National Trust Bank Charter** (BitGo Bank & Trust, National Association) — sourced from [[vendor-bitgo-homepage-2026-04]] (footer disclosure + featured-announcement banner). The OCC charter is federal-level (Office of the Comptroller of the Currency, US Treasury); structurally distinct from the NY state trust charter.
- **Non-FDIC / non-SIPC custody status** — explicit footer disclosure: "Digital assets held in custody are not guaranteed by BitGo and are not subject to... FDIC or SIPC." Trust-bank charter does NOT bring deposit insurance.
- **Non-broker-dealer / non-FINRA / non-SIPC member** — explicit footer disclosure.
- **MiCA registration status: not surfaced on the homepage.** Whether BitGo (or any of its subsidiaries) is registered as a MiCA CASP is an open question.
- **No SOC 1/2 or ISO 27001 certifications mentioned on the homepage** — these are typical institutional-custody assurances but not surfaced. Open question.

## Concepts cited

- [[occ-national-trust-bank-charter]] — federal US regulatory path; BitGo's recent charter approval is the canonical example in this wiki.
- [[limited-purpose-trust-charter]] — NY state regulatory path; BitGo's NY subsidiary uses this path.
- [[qualified-custodian]] — BitGo's "Qualified Custody" product targets the federal-rule-defined institutional custody role.
- [[bitlicense]] — cross-reference; BitGo's NY-side activity goes through trust-charter, not BitLicense.
- [[counterparty-graph-research]] — BitGo's named regulatory counterparties (OCC, NYDFS) are graph-traversal targets.
- [[citation-discipline]] — BitGo's homepage surfaces structural regulatory facts in the footer but defers technical-architecture detail to separate resource pages.

## Counterparties cited

- [[occ]] — Office of the Comptroller of the Currency; federal regulator that chartered BitGo Bank & Trust, N.A.
- [[nydfs]] — New York State Department of Financial Services; state regulator under which BitGo New York Trust Company, LLC operates.
- [[mike-belshe]] — CEO and Co-Founder.

## Open questions

- **MPC-CMP architecture details.** BitGo is widely associated in the public domain with multi-party computation custody architecture, but the homepage references "How MPC Strengthens Crypto Wallet Signing" only as a blog title without elaboration. Future ingest of product or technical pages would substantively develop the [[mpc-key-management]] concept (currently deferred).
- **Bankruptcy-remote segregation language.** Homepage doesn't surface specific structural-segregation claims; NYDFS 2025-09-30 Custodial Structures Guidance is the regulator-side framework, but BitGo's specific arrangements are not publicly disclosed on the homepage.
- **Insurance coverage details.** Linked but not detailed.
- **SOC 1/2, ISO 27001, and other audit certifications.** Not surfaced on homepage.
- **State trust charters beyond NY.** South Dakota (HQ jurisdiction) may have its own state-trust authorisation; not explored in this ingest.
- **The Mike Belshe IPO letter / S-1 filing.** Featured on homepage. SEC EDGAR S-1 (filed 2024 prior to IPO) would be a natural next-source ingest — fully public, regulator-side, structurally rich.
- **Relationship to specific stablecoin issuers.** BitGo's clientele likely includes stablecoin reserve custodians; whether [[circle]] uses BitGo for any portion of USDC reserves is not surfaced on either vendor's homepage. Both vendors generically reference "leading global banks" as counterparties.
- **MiCA / EU regulatory posture.** Not surfaced on homepage.

## Sources cited

- [[vendor-bitgo-homepage-2026-04]]
- [[regulator-nydfs-bitlicense-page-2026-04]]
