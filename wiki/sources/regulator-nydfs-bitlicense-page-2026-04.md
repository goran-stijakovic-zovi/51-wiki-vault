---
type: source
name: NYDFS — Virtual Currency Businesses (BitLicense + Limited Purpose Trust Charter)
source_url: https://www.dfs.ny.gov/virtual_currency_businesses
publication: New York State Department of Financial Services (NYDFS)
author: NYDFS (institutional)
published: 2026 (page maintained continuously by NYDFS; latest content references 2025-09-30 custodial-structures guidance)
ingested: 2026-04-27
paywalled: false
---

# NYDFS — Virtual Currency Businesses (BitLicense + Limited Purpose Trust Charter)

> _Source: https://www.dfs.ny.gov/virtual_currency_businesses_

## Summary

NYDFS's main public page for virtual-currency-business regulation describes two parallel regulatory paths under New York State law: the **BitLicense** (codified at 23 NYCRR Part 200) and the **Limited Purpose Trust Charter** (under New York Banking Law). Both authorize a business to engage in Virtual Currency Business Activity in or with New York Residents; they have different scopes, advantages, and operational implications.

The BitLicense regime defines five categories of triggering activity: (a) receiving virtual currency for transmission or transmitting it; (b) storing, holding, or maintaining custody of virtual currency on behalf of others; (c) buying and selling virtual currency as a customer business; (d) performing exchange services as a customer business; (e) controlling, administering, or issuing a virtual currency. Five categories of exemption are explicitly listed: consumer investment use, merchant payment acceptance, mining-in-itself, software development as a purely technical service, and advisory services on buying or selling.

The Limited Purpose Trust Charter is the alternative path. Trust-chartered companies "may exercise fiduciary powers" (which BitLicensees cannot) AND "can engage in money transmission in New York without obtaining a separate New York money transmitter license." Custody-focused vendors typically choose the trust path; transactional / payment vendors typically choose the BitLicense path; some vendors hold both (or BitLicense + MTL).

Operationally, BitLicense applications are filed via the **Nationwide Multistate Licensing System (NMLS)**. Capital requirements (under 23 NYCRR 200.8) vary by business model and risk; a surety bond or funded account "for the protection of the BitLicensee's customers" is required at a minimum of $500,000 (23 NYCRR 200.9(a)). Many BitLicensees also hold a New York Money Transmitter License under Banking Law Article 13-B because they transmit fiat currency in addition to virtual currency.

The page also publishes the **NYDFS Regulated Entities list** — the canonical source of truth for which entities hold which authorisations. Selected entries include Circle Internet Financial, LLC (BitLicense + MTL since 2015-09), Coinbase, Inc. (BitLicense + MTL since 2017-01), PayPal, Inc. (BitLicense + MTL since 2022-06), Block, Inc. f/k/a Square, Inc. (BitLicense + MTL since 2018-06), Gemini Trust Company, LLC (Limited Purpose Trust since 2015-10), Coinbase Custody Trust Company, LLC (Limited Purpose Trust since 2018-10), BitGo New York Trust Company, LLC (Limited Purpose Trust since 2021-03), bitFlyer USA, Inc. (Virtual Currency License since 2017-11), and Ripple Markets DE LLC (Virtual Currency License since 2016-06).

A separate but related public surface is the **NYDFS Greenlist** — a static list of 8 coins that may be offered by NYDFS-licensed VC entities without separate DFS approval. Coins on the list as of this fetch: Bitcoin (BTC), Ethereum (ETH), Gemini Dollar (GUSD), GMO JPY (GYEN), GMO USD (ZUSD), Ripple USD (RLUSD), WisdomTree Dollar (USDW), and WisdomTree Gold (GOLD). Three paths exist for VC entities to list a coin: specific DFS approval, self-certification under a DFS-approved listing policy, or use of a Greenlisted coin (with 10-day notice). DFS retains discretionary authority to remove coins from the Greenlist or curtail any coin's use at any time.

For the institutional-buyer audience this wiki serves, the NYDFS regime is the canonical US-state regulatory primitive — relevant to any vendor whose activities involve New York or New York Residents. The page is structurally important to the wiki: it is the regulator-side source of truth that allows vendor `public_status:` frontmatter to be populated under the schema's "sourced from a public regulator page" discipline.

## Key claims

1. **BitLicense statutory definition (5 activity categories).** — > "the conduct of any one of the following types of activities involving New York or a New York Resident: (1) receiving Virtual Currency for Transmission or Transmitting Virtual Currency... (2) storing, holding, or maintaining custody or control of Virtual Currency on behalf of others; (3) buying and selling Virtual Currency as a customer business; (4) performing Exchange Services as a customer business; or (5) controlling, administering or issuing a Virtual Currency."
2. **Licensing requirement.** — > "No Person shall, without a license obtained from the superintendent…engage in any Virtual Currency Business Activity." (23 NYCRR 200.3(a))
3. **Five categories of exemption** — consumer investment, merchant payment acceptance, mining-in-itself, software development as a purely technical service, advisory services.
4. **Surety bond / funded account at minimum $500,000.** — > "There is a requirement to either obtain a surety bond, or to fund an account, for the protection of the BitLicensee's customers. Generally, the minimum amount of this bond or account is $500,000…" (23 NYCRR 200.9(a))
5. **Limited Purpose Trust Charter as alternative path.** — > "While these forms of authorization are similar in many respects, a New York state limited purpose trust company charter may provide some additional benefits. For example, a limited purpose trust company can exercise fiduciary powers, while a BitLicensee cannot."
6. **Trust charter MTL exemption.** — > "A limited purpose trust company can engage in money transmission in New York without obtaining a separate New York money transmitter license."
7. **Dual licensing requirement for BitLicensees handling fiat.** — > "The BitLicense allows a company to conduct Virtual Currency Business Activity involving New York or a New York Resident, but it does not replace any other licenses required under New York law. For example, many BitLicensees engage in the transmission of fiat currency (e.g., U.S. dollars), which requires them to hold a money transmission license under New York Banking Law Article 13-B."
8. **NYDFS Greenlist.** — 8 coins approved for offering without separate DFS approval as of fetch (BTC, ETH, GUSD, GYEN, ZUSD, RLUSD, USDW, GOLD).
9. **Three paths for listing a coin.** — DFS application approval, self-certification under DFS-approved policy, or use of Greenlisted coin (with 10-day notice).
10. **DFS retains discretionary authority over the Greenlist.** — > "DFS may, at any time and in its sole discretion, prohibit or otherwise limit a coin's use before or after a VC Entity begins using a coin; require that any VC Entity delist… remove any coin from the Greenlist… or discontinue the Greenlist process entirely."
11. **Regulated Entities list — selected (canonical regulator-side source of truth)**:
    - Circle Internet Financial, LLC — BitLicense + MTL, 2015-09.
    - Coinbase, Inc. — BitLicense + MTL, 2017-01.
    - PayPal, Inc. — BitLicense + MTL, 2022-06.
    - Block, Inc. (f/k/a Square, Inc.) — BitLicense + MTL, 2018-06.
    - Gemini Trust Company, LLC — Limited Purpose Trust Charter, 2015-10.
    - Coinbase Custody Trust Company, LLC — Limited Purpose Trust Charter, 2018-10.
    - BitGo New York Trust Company, LLC — Limited Purpose Trust Charter, 2021-03.
    - bitFlyer USA, Inc. — Virtual Currency License only, 2017-11.
    - Ripple Markets DE LLC — Virtual Currency License only, 2016-06.

## Concepts cited

- [[bitlicense]] — substantive: the central NY-state regulatory primitive defined by this source.
- [[limited-purpose-trust-charter]] — substantive: the alternative regulatory path for fiduciary-powers vendors.
- [[nydfs-greenlist]] — substantive: the explicit list of approved coins + the three-paths-to-listing mechanism.
- [[mica-compliance]] — cross-reference; NYDFS is the US-state analogue of EU MiCA, with structurally different scope and mechanism.
- [[crypto-asset-service-provider]] — cross-reference; CASPs and BitLicensees occupy structurally similar roles in their respective jurisdictions.
- [[citation-discipline]] — NYDFS publishes the Regulated Entities list as the regulator-side source of truth; vendor `public_status:` discipline is enforced at the regulator-publication layer.

## Vendors discussed

- [[circle]] — BitLicense + MTL since 2015-09 (Circle Internet Financial, LLC). This source is the regulator-side cross-confirmation of the licenses that Circle's transparency-page footer asserts on the vendor side.
- Forward references to BitGo, Coinbase, PayPal, Gemini, Block, bitFlyer, and Ripple Markets — these vendors hold NYDFS authorizations per the regulated-entities list, but vendor pages will only be created when their own direct vendor-source ingests occur (per the schema's "create pages from sources" rule).

## Sectors touched

- [[regulatory-and-compliance]] — NYDFS is the US-state regulator anchor for this sector.
- [[stablecoin-issuers]] — NYDFS published "Guidance on the Issuance of U.S. Dollar-Backed Stablecoins" (2022-06-08); Greenlist includes named stablecoins (GUSD, GYEN, ZUSD, RLUSD, USDW); USDC notably is NOT on the Greenlist but Circle holds a BitLicense.
- [[custody]] — Limited Purpose Trust Charter is the canonical custodian-vendor path (BitGo, Gemini, Coinbase Custody all use it); 2025-09-30 NYDFS "Updated Guidance on Custodial Structures for Customer Protection in the Event of Insolvency" supersedes 2023-01-23 prior guidance.
- [[payment-and-settlement]] — BitLicense + MTL dual licensing is the canonical configuration for fiat-handling payment / settlement vendors (Coinbase, PayPal, Block, Circle).

## Notable quotes

> "the conduct of any one of the following types of activities involving New York or a New York Resident: (1) receiving Virtual Currency for Transmission or Transmitting Virtual Currency..."

> "No Person shall, without a license obtained from the superintendent…engage in any Virtual Currency Business Activity."

> "While these forms of authorization are similar in many respects, a New York state limited purpose trust company charter may provide some additional benefits. For example, a limited purpose trust company can exercise fiduciary powers, while a BitLicensee cannot."

> "A limited purpose trust company can engage in money transmission in New York without obtaining a separate New York money transmitter license."

> "The BitLicense allows a company to conduct Virtual Currency Business Activity involving New York or a New York Resident, but it does not replace any other licenses required under New York law."

> "DFS may, at any time and in its sole discretion, prohibit or otherwise limit a coin's use before or after a VC Entity begins using a coin… or discontinue the Greenlist process entirely."

## Open questions raised

- **USDC is not on the Greenlist as of this fetch, but Circle holds a BitLicense.** What's the specific regulatory pathway through which Circle's USDC operates in NY-licensed vendor portfolios — via Circle's own BitLicense (controlling/administering/issuing a virtual currency) or via DFS-approved listing on each individual vendor's coin policy? Material to institutional-buyer diligence on USDC.
- **NYDFS Stablecoin Guidance (2022-06-08).** The page references but does not reproduce this guidance. A future ingest of the actual guidance document would substantively develop the [[bitlicense]] / [[circle]] / [[sky-protocol]] concept clusters.
- **NYDFS Custodial Structures Guidance (2025-09-30).** Same: page references but doesn't reproduce. Highly relevant to the upcoming custody-vendor ingest.
- **Sky Protocol's NY status.** Sky.money's "currently unavailable in the US" geographic restriction may relate to NYDFS BitLicense scope (the protocol controls/administers/issues a virtual currency, which would trigger the BitLicense requirement). Open question on the [[sky-protocol]] page.

## External references

- 23 NYCRR Part 200 (Virtual Currency regulation).
- 23 NYCRR Part 504 (Transaction Monitoring and Filtering Program Requirements).
- New York Banking Law Article 13-B (Money Transmitters).
- NMLS application portal — https://mortgage.nationwidelicensingsystem.org/slr/SitePages/DynamicLicenses.aspx?StateID=NY
- DFS Portal for self-certification — https://myportal.dfs.ny.gov/
- NYDFS Industry Letters referenced (not separately ingested):
  - "Updated Guidance on Custodial Structures for Customer Protection in the Event of Insolvency" (2025-09-30)
  - "Guidance Regarding Listing of Virtual Currencies" (2023-11-15)
  - "General Framework for Greenlisted Coins" (2023-09-18)
  - "Guidance on the Issuance of U.S. Dollar-Backed Stablecoins" (2022-06-08)
  - "Guidance on Use of Blockchain Analytics" (2022-04-28)
  - "Guidance on Assessment of the Character and Fitness of Directors, Senior Officers, and Managers" (2024-01-22)
  - "Guidance Regarding Customer Service Requests and Complaints" (2024-05-30)

## Cross-references

- [[regulator-eu-mica-esma-hub]] — the EU regulatory analogue. NYDFS is the US-state primitive; MiCA is the EU-level. International issuers like [[circle]] navigate both regimes, with distinct authorisation tracks per jurisdiction.
- [[vendor-circle-transparency-page-2026-04]] — Circle's own footer asserts NYDFS Money Transmitter + VCBA licenses; this NYDFS source is the regulator-side cross-confirmation.
- [[51-deck-april-2026]] — names "Regulatory & Compliance" as a research category; NYDFS is one of the canonical jurisdictional anchors institutional buyers diligence.
