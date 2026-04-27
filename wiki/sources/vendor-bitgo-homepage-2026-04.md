---
type: source
name: BitGo public homepage (fetched April 2026)
source_url: https://www.bitgo.com
publication: BitGo Holdings, Inc.
author: BitGo (institutional)
published: 2026 (page maintained by BitGo; latest content references the OCC national trust bank charter approval as a featured announcement)
ingested: 2026-04-27
paywalled: false
---

# BitGo public homepage (fetched April 2026)

> _Source: https://www.bitgo.com_

## Summary

BitGo's homepage positions the company as **"the digital asset infrastructure company"** offering five service categories: Prime Services (liquidity and capital), Ecosystem (launch / manage / grow), Stablecoins (hold / swap / manage / issue), Wallet Services (secure wallet solutions), and Crypto-as-a-Service. The most substantive ingest content is regulatory: BitGo recently secured **OCC approval to convert to a federally chartered national trust bank** under the entity name **BitGo Bank & Trust, National Association**. This federal charter is structurally significant — it is distinct from the [[limited-purpose-trust-charter|NYDFS Limited Purpose Trust Charter]] that BitGo New York Trust Company, LLC has held since 2021-03, and it places BitGo's federally-chartered subsidiary under direct OCC (Office of the Comptroller of the Currency) supervision.

The corporate structure surfaced on the page is: **BitGo Holdings, Inc.** (Delaware corporation, headquartered in Sioux Falls, South Dakota) is the parent, with **BitGo Bank & Trust, N.A.** as a wholly-owned subsidiary chartered and regulated by the OCC. BitGo also retains the **BitGo New York Trust Company, LLC** subsidiary (per the [[regulator-nydfs-bitlicense-page-2026-04]] Regulated Entities list). The vendor uses a multi-entity structure that maps different regulatory regimes to different subsidiaries — the same pattern as [[circle]] (Circle Internet Financial, LLC for NYDFS; Circle International Bermuda Limited for BMA).

The homepage product taxonomy distinguishes Hot Wallets, Cold Wallets, Self-Custody, and Qualified Custody. The "Qualified Custody" product is the institutional-buyer-targeted offering aligned with US federal qualified-custodian rules applicable to SEC-registered investment advisers. The page mentions an MPC (multi-party computation) blog post but does not detail BitGo's key-management cryptographic architecture in the homepage text.

The page contains an explicit insurance disclosure: **"Digital assets held in custody are not guaranteed by BitGo and are not subject to... FDIC or SIPC."** A trust-bank charter does NOT bring deposit insurance, and BitGo states this explicitly.

For the institutional-buyer audience, the substantive payload of this ingest is **(a) the new OCC federal charter as a US regulatory path distinct from BitLicense and state trust charter**, **(b) the multi-jurisdictional subsidiary structure**, and **(c) the explicit non-FDIC/SIPC disclosure**. The MPC architecture, specific bankruptcy-remote segregation language, and SOC 1/2 / ISO 27001 certifications are referenced indirectly or not at all on the homepage and are flagged as open questions for future ingest.

## Key claims

1. **OCC national trust bank charter approval.** — > "BitGo Secures OCC Approval to Convert to a Federally Chartered National Trust Bank" (featured announcement).
2. **BitGo Bank & Trust, National Association as the federally-chartered subsidiary.** — > "BitGo Bank & Trust, National Association... is a national trust bank chartered and regulated by the Office of the Comptroller of the Currency (OCC)" (footer).
3. **Corporate structure.** — > "BitGo Bank & Trust is a wholly-owned subsidiary of BitGo Holdings, Inc., a Delaware corporation headquartered in Sioux Falls, South Dakota" (footer).
4. **Non-FDIC / non-SIPC disclosure.** — > "Digital assets held in custody are not guaranteed by BitGo and are not subject to... FDIC or SIPC."
5. **Non-broker-dealer / non-FINRA disclosure.** — > "BitGo does not... qualify as broker-dealer, SIPC member, or FINRA member."
6. **Five service categories**: Prime Services, Ecosystem, Stablecoins, Wallet Services, Crypto-as-a-Service.
7. **Product taxonomy**: Hot Wallets, Cold Wallets, Self-Custody, Qualified Custody.
8. **MPC reference.** — Blog post titled "How MPC Strengthens Crypto Wallet Signing" linked on homepage but content not detailed.
9. **CEO / Co-Founder named.** — A "Letter From Mike Belshe, BitGo CEO and Co-Founder" is featured (presumably IPO-related per its placement).

## Concepts cited

- [[occ-national-trust-bank-charter]] — substantive: the federal regulatory primitive BitGo secured.
- [[qualified-custodian]] — BitGo's "Qualified Custody" product is the institutional-buyer-targeted offering aligned with this concept.
- [[limited-purpose-trust-charter]] — cross-reference; BitGo also retains the NYDFS Limited Purpose Trust Charter through BitGo New York Trust Company, LLC. The two regulatory paths (state trust + federal trust bank) are complementary in BitGo's regulatory stack.
- [[bitlicense]] — cross-reference; BitGo's NY-side activity goes through the trust-charter path rather than the BitLicense path (the trust charter authorizes both VC business activity and money transmission, where BitLicense + separate MTL would be the alternative configuration).
- [[counterparty-graph-research]] — BitGo's named regulatory counterparties (OCC, NYDFS) are graph-traversal targets.
- [[citation-discipline]] — BitGo's homepage surfaces structural regulatory facts in the footer (legal-entity disclosure, regulator names, non-FDIC/SIPC disclaimer) but defers technical-architecture detail to separate resource pages.

## Vendors discussed

- [[bitgo]] — primary subject of the page.

## Sectors touched

- [[custody]] — BitGo is the wiki's first custody-sector vendor; BitGo also has stablecoin-management infrastructure (B2B angle distinct from custody alone).
- [[stablecoin-issuers]] — minor: BitGo's "Stablecoins" service category includes "issue" as a service, suggesting B2B issuer-platform infrastructure rather than first-party stablecoin issuance.

## Notable quotes

> "The digital asset infrastructure company."

> "BitGo Secures OCC Approval to Convert to a Federally Chartered National Trust Bank."

> "BitGo Bank & Trust, National Association... is a national trust bank chartered and regulated by the Office of the Comptroller of the Currency (OCC)."

> "Digital assets held in custody are not guaranteed by BitGo and are not subject to... FDIC or SIPC."

## Open questions raised

- **MPC-CMP architecture details.** Homepage references an MPC blog post but doesn't detail key-management cryptographic architecture. Future ingest of BitGo's product or technical pages would substantively develop the [[mpc-key-management]] concept (currently deferred).
- **Bankruptcy-remote segregation language.** Homepage doesn't surface specific structural-segregation claims. NYDFS 2025-09-30 Custodial Structures Guidance (referenced from [[regulator-nydfs-bitlicense-page-2026-04]]) is the regulator-side framework; whether BitGo's specific structural-segregation arrangements are publicly disclosed is an open question.
- **Insurance coverage details.** Homepage links to an Insurance resource page but doesn't detail policy types or coverage amounts.
- **SOC 1/2, ISO 27001 certifications.** Homepage doesn't mention them. Future ingest of certification-listing pages would substantively address.
- **State trust charters beyond NY.** Homepage mentions only the OCC federal charter. The wiki currently knows about NYDFS Limited Purpose Trust Charter (2021-03). South Dakota's state trust regulator may be relevant given the headquarters-in-Sioux-Falls disclosure; not explored in this ingest.
- **The Mike Belshe IPO letter.** Featured on the homepage but content not reproduced. SEC EDGAR S-1 filings (BitGo filed an S-1 in 2024 in preparation for IPO) would be a natural next-source for a future ingest — fully public, regulator-side, structurally rich.
- **Relationship to [[circle]] specifically.** BitGo's clientele likely includes stablecoin issuers using BitGo for reserve custody. Whether Circle uses BitGo for any portion of its reserves is not surfaced on either Circle's or BitGo's homepage; both pages name BlackRock (Circle's MMF manager) and various banks generically. Open cross-reference question.

## External references

- BitGo Insurance resource page (linked, not fetched) — https://www.bitgo.com/solutions/insurance/
- BitGo "How MPC Strengthens Crypto Wallet Signing" blog (linked, not fetched).
- "A Letter From Mike Belshe, BitGo CEO and Co-Founder" (featured, content not reproduced on homepage).

## Cross-references

- [[regulator-nydfs-bitlicense-page-2026-04]] — confirms BitGo New York Trust Company, LLC holds NYDFS Limited Purpose Trust Charter since 2021-03 (regulator-side cross-confirmation of BitGo's NY presence).
- [[vendor-circle-transparency-page-2026-04]] — for parallel-vendor framing: Circle and BitGo both use multi-entity subsidiary structures mapping different regulatory regimes to different subsidiaries.
- [[51-deck-april-2026]] — names "Custody" as a sector and "Mike Belshe, CEO, BitGo" in the expert-network slide; this BitGo source is the regulator-and-public-vendor anchoring of the deck-level mention.
