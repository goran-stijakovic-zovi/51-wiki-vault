---
type: concept
name: BitLicense
sources: 1
last_updated: 2026-04-27
---

# BitLicense

> *New York State's virtual-currency-business licensing regime, codified at 23 NYCRR Part 200, administered by [[nydfs|NYDFS]]. Required for any of five categories of virtual-currency activity involving New York or New York Residents.*

## What it means

The BitLicense is a US-state regulatory authorisation issued by NYDFS to entities engaging in **Virtual Currency Business Activity** in or with New York Residents. It was the first comprehensive US-state digital-asset regulatory regime (introduced 2015) and remains one of the most-cited US-side regulatory anchors for institutional-buyer diligence on digital-asset vendors.

For an international vendor like [[circle]] operating in or serving New York, holding a BitLicense is a direct regulatory authorisation; lacking one (while engaging in the activities Part 200 covers) is a clear compliance gap. For a DeFi-native protocol like [[sky-protocol]] whose interface displays "currently unavailable in the US" without stated legal basis, the BitLicense regime is one plausible source of the geographic restriction (controlling/administering/issuing a virtual currency would trigger Part 200, and Sky Protocol does both).

## How it shows up in sources

- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS's canonical public page providing the statutory definition (23 NYCRR Part 200), the five activity categories that trigger the licensing requirement, the five exemption categories, the application process via NMLS, capital and surety-bond requirements (23 NYCRR 200.8 and 200.9(a)), and the public Regulated Entities list.
- [[vendor-circle-transparency-page-2026-04]] — Circle's transparency page footer asserts NYDFS Money Transmitter + Virtual Currency Business Activity licenses for Circle Internet Financial, LLC. Cross-confirmed by the NYDFS source above (Circle holds BitLicense + MTL since 2015-09).

## Mechanism / how it works

**Five activity categories that trigger the licensing requirement** (23 NYCRR Part 200, verbatim):

> "the conduct of any one of the following types of activities involving New York or a New York Resident:
> (1) receiving Virtual Currency for Transmission or Transmitting Virtual Currency...
> (2) storing, holding, or maintaining custody or control of Virtual Currency on behalf of others;
> (3) buying and selling Virtual Currency as a customer business;
> (4) performing Exchange Services as a customer business; or
> (5) controlling, administering or issuing a Virtual Currency."

**Five categories of exemption:**

- **Consumer investment**: a consumer using virtual currency solely for investment purposes.
- **Merchant payment acceptance**: merchants and consumers using virtual currency solely for purchase/sale of goods or services.
- **Mining-in-itself**: virtual-currency mining alone does not trigger the requirement.
- **Software development as a purely technical service**: neither does developing or disseminating software.
- **Advisory services**: providing advice on buying or selling, by itself, does not trigger.

**Application process:**

1. Filed via the **Nationwide Multistate Licensing System (NMLS)**.
2. Applicant completes a Company Account Request Form, receives NMLS login credentials, and submits a substantially complete application using the NY Virtual Currency Business Activity License New Application Checklist.
3. Application enters substantive review only after all required information, documents, and fees are received.

**Capital + surety bond:**

- Capital requirements (23 NYCRR 200.8) vary by business model and risk.
- Surety bond or funded account "for the protection of the BitLicensee's customers" is required at a minimum of $500,000 (23 NYCRR 200.9(a)).

**Dual licensing for fiat handling:**

> "The BitLicense allows a company to conduct Virtual Currency Business Activity involving New York or a New York Resident, but it does not replace any other licenses required under New York law. For example, many BitLicensees engage in the transmission of fiat currency (e.g., U.S. dollars), which requires them to hold a money transmission license under New York Banking Law Article 13-B."

This is why [[circle]]'s `public_status:` lists both NYDFS Money Transmitter and NYDFS VCBA — the two regimes are complementary, not redundant.

**Alternative path: [[limited-purpose-trust-charter|Limited Purpose Trust Charter]].** Under NY Banking Law, a New York limited-purpose trust company may engage in Virtual Currency Business Activity without a BitLicense if approved by the Superintendent. The trust charter has two structural advantages: it permits exercise of fiduciary powers (BitLicensees cannot exercise fiduciary powers) and it includes money-transmission authority (BitLicensees do not — they need a separate MTL).

**Regulator-side source of truth: the Regulated Entities list.** NYDFS publishes a static table of authorised entities with license type and date. The wiki's vendor `public_status:` frontmatter populates from this list (per the schema's "sourced from a public regulator page" discipline).

## Related concepts

- [[limited-purpose-trust-charter]] — alternative state-level regulatory path; structurally distinct (custody-focused vendors typically choose this over BitLicense).
- [[occ-national-trust-bank-charter]] — federal-level alternative path; multi-state operating scope; bank-like regulatory perimeter. Custody vendors may hold federal OCC charter alongside or instead of state regulatory paths ([[bitgo]] holds both for different subsidiaries).
- [[nydfs-greenlist]] — separate but related public surface; coins approved for offering by NYDFS-licensed VC entities. Note: BitLicense holders are not automatically Greenlist-included for their own coins (e.g. USDC is NOT on the Greenlist even though Circle holds a BitLicense).
- [[mica-compliance]] — EU-level analogue. Both regimes are first-order screening for international issuers and CASPs.
- [[crypto-asset-service-provider]] — MiCA's CASP regime is the EU functional analogue of the BitLicense's transactional / custody / exchange categories.
- [[citation-discipline]] — the Regulated Entities list is the canonical regulator-side citation source for vendor `public_status:` claims.

## Related vendors / sectors

- [[circle]] — BitLicense + MTL since 2015-09. Wiki's first vendor with regulator-side cross-confirmation.
- [[stablecoin-issuers]] — Issuers controlling/administering/issuing a virtual currency (Part 200(5)) are subject to the regime.
- [[custody]] — Custodians storing/holding virtual currency on behalf of others (Part 200(2)) are subject to the regime; trust-charter is the typical custodian path rather than BitLicense.
- [[payment-and-settlement]] — Transmission, exchange services, customer-business buying/selling are all Part 200 categories.
- [[regulatory-and-compliance]] — sector that maps compliance tooling to BitLicense reporting requirements.

## Open questions

- **2022-06-08 NYDFS Stablecoin Guidance** ("Guidance on the Issuance of U.S. Dollar-Backed Stablecoins") is referenced from the source page but its content is not ingested. Future ingest of the actual guidance document would substantively develop the relationship between BitLicense and stablecoin issuance, including reserve and disclosure expectations specific to USD-backed stablecoins.
- **2025-09-30 NYDFS Custodial Structures Guidance.** Highly relevant to the upcoming custody-vendor ingest; supersedes 2023-01-23 prior guidance.
- **The "issuer" prong of Part 200(5).** Whether [[sky-protocol]]'s decentralized issuance model triggers BitLicense applicability, and how the regime would attribute the controlling-administering-issuing activity in a non-custodial-interface architecture, is an open question.

## Sources cited

- [[regulator-nydfs-bitlicense-page-2026-04]]
- [[vendor-circle-transparency-page-2026-04]]
