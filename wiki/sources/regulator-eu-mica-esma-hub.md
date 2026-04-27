---
type: source
name: ESMA — Markets in Crypto-Assets Regulation (MiCA) hub
source_url: https://www.esma.europa.eu/esmas-activities/digital-finance-and-innovation/markets-crypto-assets-regulation-mica
publication: European Securities and Markets Authority (ESMA)
author: ESMA (institutional)
published: 2025 (page maintained by ESMA; iXBRL disclosure rules referenced as of December 2025)
ingested: 2026-04-27
paywalled: false
---

# ESMA — Markets in Crypto-Assets Regulation (MiCA) hub

> _Source: https://www.esma.europa.eu/esmas-activities/digital-finance-and-innovation/markets-crypto-assets-regulation-mica_

## Summary

ESMA's MiCA hub describes the EU's Markets in Crypto-Assets Regulation as a uniform market-rules framework covering crypto-assets that are not already governed by existing EU financial-services legislation. Four regulatory categories structure the regime: **Asset-Referenced Tokens (Title III)**, **E-Money Tokens (Title IV)**, **other crypto-assets (Title II — i.e. crypto-assets that are neither ART nor EMT)**, and **Crypto-Asset Service Providers / CASPs (Title V)**. The framework's stated objectives are transparency, disclosure, authorisation, and supervision of crypto-asset transactions, with consumer-information protection as a downstream goal.

The disclosure primitive is the **crypto-asset white paper**, an issuer-prepared document analogous in role to a securities prospectus. As of 23 December 2025, white papers must use **iXBRL formatting** to ensure machine-readability and consistency with technical standards. Importantly, ESMA explicitly states that the white papers in its register "have not been reviewed or approved by any competent authority" — the regime puts the disclosure burden on the issuer and treats ESMA's role as registry-keeper, not gatekeeper.

ESMA maintains an **interim MiCA register** as weekly-updated CSV files, listing white papers (for non-ART/non-EMT crypto-assets), ART issuers, EMT issuers, authorised CASPs, and non-compliant entities. The register integrates into ESMA's IT systems formally in mid-2026.

The regulation entered into force in June 2023 and reached full application in December 2024. A **transitional period under Article 143** runs until **1 July 2026**: entities that were providing crypto-asset services under national law before 30 December 2024 may continue operating during this window or until they receive a MiCA authorisation decision (Art. 143(3)). A simplified-authorisation track exists for entities authorised under national law on 30 December 2024 (Art. 143(6)). Member State notification deadlines under Articles 93, 99, 108, and 111 covered competent-authority designation, Title VII implementation laws (deadline 30 June 2025), administrative-penalties rules (30 June 2025), and complaints-handling procedures.

For the institutional-buyer audience this wiki serves, MiCA is the central regulatory primitive cross-cutting [[stablecoin-issuers]], [[custody]], [[regulatory-and-compliance]], and [[payment-and-settlement]] sectors — its registration status (or lack of it) is a first-order screening criterion for any vendor operating in or serving the EU market.

## Key claims

1. **MiCA covers crypto-assets not already regulated by other EU financial-services law.** — > "The regulation covers crypto-assets that are not currently regulated by existing financial services legislation."
2. **MiCA addresses transparency, disclosure, authorisation, and supervision for crypto-asset issuers and traders.** — > "Key provisions for those issuing and trading crypto-assets (including asset-reference tokens and e-money tokens) cover transparency, disclosure, authorisation and supervision of transactions."
3. **Four regulatory categories: ART, EMT, "other crypto-assets," CASPs.** — Titles III, IV, II (excluding ART/EMT), and V respectively.
4. **White papers are the disclosure primitive; iXBRL formatting required from 23 December 2025.** — White paper formatting "entered into application on 23 December 2025, requiring iXBRL format to ensure information is machine-readable and consistent with technical standards."
5. **ESMA does NOT review or approve white papers.** — > "The crypto-asset white papers listed in ESMA's register have not been reviewed or approved by any competent authority in any Member State of the European Union."
6. **ESMA maintains the public MiCA register as weekly-updated CSV files** until mid-2026.
7. **Transitional period under Article 143 ends 1 July 2026.** Entities providing crypto-asset services under national law before 30 December 2024 may continue until then or until authorisation decision.
8. **Implementation timeline:** entry into force June 2023; full application December 2024; transitional period 18 months ending 1 July 2026; iXBRL disclosure requirement from 23 December 2025; MiCA Order Book / Records Keeping JSON Schema published 28 November 2025.

## Concepts cited

- [[mica-compliance]] — the central regulatory frame. ESMA's hub is the canonical source.
- [[asset-referenced-token]] — Title III category.
- [[e-money-token]] — Title IV category.
- [[crypto-asset-service-provider]] — Title V category.
- [[crypto-asset-white-paper]] — the disclosure primitive (iXBRL machine-readable).
- [[citation-discipline]] — ESMA's stance that white-paper accuracy is the issuer's responsibility, with ESMA serving as registry-keeper rather than gatekeeper, is a structural enforcement of citation discipline at the regulatory layer.

## Vendors discussed

_(none in this source — the ESMA hub is regulator-side. Vendor-level MiCA-registration status will be cross-referenced from later sources, e.g. Circle and Sky's own MiCA disclosures.)_

## Sectors touched

- [[stablecoin-issuers]] — ART and EMT issuance regimes.
- [[custody]] — custody-of-crypto-assets is a CASP service under Title V.
- [[regulatory-and-compliance]] — MiCA's supervisory regime is the regulatory frame compliance vendors map to.
- [[payment-and-settlement]] — transfer-of-crypto-assets is a CASP service under Title V.

## Notable quotes

> "The regulation covers crypto-assets that are not currently regulated by existing financial services legislation."

> "The crypto-asset white papers listed in ESMA's register have not been reviewed or approved by any competent authority in any Member State of the European Union."

> "Proper disclosures are essential for safeguarding investors by allowing them to make informed decisions about a given crypto-asset."

## Open questions raised

- Where does the boundary lie between Title II "other crypto-assets" and existing financial-instrument regulation (MiFID II)? ESMA publishes a separate guideline on qualification of crypto-assets as financial instruments — a follow-up source for substantive ingest if any vendor in the wiki sits at this boundary.
- The iXBRL machine-readability requirement could be a first-class structural input for an LLM Wiki — a `raw/regulators/eu-mica-register.csv` could in principle be auto-fetched and turned into vendor `public_status:` frontmatter updates. Out of scope for this Session 1 (no fetcher), but flagged for the `scripts/_README.md` future-fetcher list.
- The Article 143 transitional period creates a "MiCA in transition" status that's distinct from "MiCA-registered" — does the schema's `public_status:` frontmatter need a sub-state like `["MiCA-transitional"]` vs `["MiCA-registered"]`?

## External references

- ESMA Joint Q&As — https://www.esma.europa.eu/joint-committee/joint-qas
- MiCA White Paper Taxonomy 2025 — https://www.esma.europa.eu/document/mica-taxonomy-2025
- MiCA Order Book and Records Keeping Message Specifications — https://www.esma.europa.eu/document/mica-order-book-and-records-keeping-message-specifications
- ESMA Final Report on Technical Standards (1st, 2nd, 3rd packages) — https://www.esma.europa.eu
- ESMA Guidelines on Crypto-Asset Qualification as Financial Instruments — https://www.esma.europa.eu/sites/default/files/2024-12/ESMA75453128700-1323_Final_Report_Guidelines_on_the_conditions_and_criteria_for_the_qualification_of_CAs_as_FIs.pdf

## Cross-references

- [[51-deck-april-2026]] — names "Regulatory & Compliance" as a sector and treats regulatory posture as a first-order vendor-screening axis; ESMA's MiCA hub is the EU regulatory frame this audience cares about.
