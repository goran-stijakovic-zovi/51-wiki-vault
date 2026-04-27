---
type: source
name: Circle USDC Transparency & Reserves (public page, fetched April 2026)
source_url: https://www.circle.com/transparency
publication: Circle Internet Financial / Circle.com
author: Circle (institutional)
published: 2026 (page maintained by Circle; latest content reflects January 2026 attestations and 23 April 2026 issuance/redemption summaries)
ingested: 2026-04-27
paywalled: false
---

# Circle USDC Transparency & Reserves (public page, fetched April 2026)

> _Source: https://www.circle.com/transparency_

## Summary

Circle's public transparency page articulates the structural commitments and disclosure regime backing USDC and EURC. The defining policy claim is a **1:1 redemption guarantee** — USDC is "always redeemable 1:1 for US dollars, and EURC is always redeemable 1:1 for euros, always." Reserves are "100% backed by highly liquid cash and cash-equivalent assets," concretely structured as cash deposits at large banks, short-dated US Treasury securities, and overnight US Treasury repurchase agreements.

The structural mechanism that makes this transparency claim regulator-grounded is the **Circle Reserve Fund (USDXX)**, an **SEC-registered 2a-7 government money market fund** that holds the majority of USDC reserves. The fund is **managed by BlackRock**, with daily independent third-party portfolio reporting publicly available via BlackRock's product page. The remainder of the reserve sits in cash deposits at unnamed but characterized "leading global banks." The 2a-7 government MMF is a long-established US securities-law primitive used by money market funds for liquidity and stability — USDC inherits the regulatory transparency of that vehicle for its majority-reserve component.

The disclosure regime is a **two-tier cadence**: weekly self-published Circle reports of holdings + mint/burn flows, plus monthly third-party attestation by a Big Four accounting firm (currently Deloitte & Touche LLP, Circle's independent auditor since fiscal 2022; previously Grant Thornton LLP from 2015). The monthly attestations follow attestation standards set by the AICPA and provide third-party assurance that reserves exceed circulating USDC. Circle states it has "issued reports on all reserve assets since 2018" — making it one of the longest reserve-disclosure histories among centralized stablecoin issuers.

Regulatory licenses explicitly named on the page footer:

- **Circle Internet Financial, LLC** — licensed as a Money Transmitter by the New York State Department of Financial Institutions, and licensed for Virtual Currency Business Activity by the New York State Department of Financial Services (NYDFS).
- **Circle International Bermuda Limited** — licensed to conduct digital asset business by the Bermuda Monetary Authority (BMA).

Notably, **MiCA (Markets in Crypto-Assets Regulation) is not mentioned on this transparency page.** Circle's EU-side regulatory posture is not surfaced here. For an institutional buyer doing EU-jurisdiction diligence on USDC, this is a structurally significant absence.

## Key claims

1. **1:1 redemption guarantee for USDC and EURC.** — > "USDC is always redeemable 1:1 for US dollars, and EURC is always redeemable 1:1 for euros. Always."
2. **100% cash and cash-equivalent backing.** — > "USDC is a digital dollar backed 100% by highly liquid cash and cash-equivalent assets and is always redeemable 1:1 for US dollars."
3. **Reserve composition: three asset classes** — cash deposits at leading financial institutions, short-dated US Treasury securities, overnight US Treasury repurchase agreements.
4. **Majority of reserves held in the SEC-registered 2a-7 government MMF (USDXX).** — > "The majority of the USDC reserve is held in the Circle Reserve Fund (USDXX), an SEC-registered 2a-7 government money market fund." Managed by BlackRock; daily independent portfolio reporting publicly available.
5. **Two-tier disclosure cadence: weekly Circle + monthly Big Four.** — > "USDC reserve holdings are fully disclosed on a weekly basis, along with associated mint/burn flows. Additionally, a Big Four accounting firm provides monthly third-party assurance that the value of USDC reserves are greater than the amount of USDC in circulation."
6. **Attestation standards: AICPA.** — > "The reports are prepared according to attestation standards set out by the American Institute of Certified Public Accountants (AICPA)."
7. **Reporting history since 2018.** — > "we've issued reports on all reserve assets since 2018, along with SEC filings in 2021 and 2022."
8. **Current independent auditor: Deloitte & Touche LLP (since fiscal 2022); previously Grant Thornton LLP (from 2015).**
9. **Circle Internet Financial, LLC: NYDFS Money Transmitter + Virtual Currency Business Activity licenses.**
10. **Circle International Bermuda Limited: BMA digital asset business license.**
11. **No MiCA mention.** Circle's EU regulatory posture is not surfaced on this page.

## Concepts cited

- [[proof-of-reserves]] — the central transparency primitive; Circle's two-tier weekly + monthly disclosure regime is a canonical implementation.
- [[2a-7-government-money-market-fund]] — the US-securities-law structure underpinning Circle's majority-reserve vehicle.
- [[e-money-token]] — single-USD-pegged → EMT-archetype issuer under MiCA framing, even though Circle's transparency page does not mention MiCA.
- [[citation-discipline]] — Circle's weekly + monthly + AICPA-attested disclosure regime is a real-world institutional implementation of structural citation discipline at the issuer layer.
- [[counterparty-graph-research]] — Circle's transparency page itself surfaces named counterparties (BlackRock as fund manager, Deloitte as auditor, NYDFS as regulator, BMA as regulator), making the page a graph traversal target.
- [[crypto-asset-white-paper]] — Circle does not file a MiCA white paper as of this page; the EU-side disclosure layer is absent.

## Vendors discussed

- [[circle]] — primary subject of the page.

## Sectors touched

- [[stablecoin-issuers]] — Circle is the canonical large centralized stablecoin issuer.

## Notable quotes

> "USDC is always redeemable 1:1 for US dollars, and EURC is always redeemable 1:1 for euros. Always."

> "USDC is a digital dollar backed 100% by highly liquid cash and cash-equivalent assets and is always redeemable 1:1 for US dollars."

> "The majority of the USDC reserve is held in the Circle Reserve Fund (USDXX), an SEC-registered 2a-7 government money market fund."

> "Daily, independent, third-party reporting on the portfolio is publicly available via BlackRock."

> "The reserve is designed to provide holders with ready liquidity, even under extremely stressed conditions."

> "As part of our strong commitment to transparency, we've issued reports on all reserve assets since 2018, along with SEC filings in 2021 and 2022."

## Open questions raised

- **Circle's MiCA registration status as of 2026-04.** The transparency page does not surface it. Does Circle have an EU subsidiary registered as an EMT issuer under MiCA Title IV? A follow-up source (Circle's EU regulatory disclosure or the ESMA register snapshot) would resolve this.
- **Identity of the named "leading global banks" holding the cash component.** The transparency page describes them generically but does not name them on this page. Other Circle disclosures (SEC filings, monthly attestations) may name them.
- **Did the transparency page change after the March 2023 SVB depeg event?** USDC depegged briefly in March 2023 when ~$3.3B of cash reserves at Silicon Valley Bank were briefly inaccessible. The current page does not discuss the SVB episode explicitly — has the bank-counterparty disclosure regime changed since then? Out-of-scope for this ingest, but a follow-up source to consider.

## External references

- BlackRock USDXX (Circle Reserve Fund) product page — https://www.blackrock.com/cash/en-us/products/329365/
- USDC monthly attestation reports archive — `https://6778953.fs1.hubspotusercontent-na1.net/hubfs/6778953/USDCAttestationReports/` (reports from October 2018 onward; pattern: `[YEAR]/[YEAR] USDC_Examination Report [MONTH] [YY].pdf`).
- EURC monthly attestation reports archive — `https://6778953.fs1.hubspotusercontent-na1.net/hubfs/6778953/EURC%20Attestations/` (reports from June 2022 onward; renamed from EUROC to EURC in 2023).
- Specific attestation PDFs are linked but not fetched into this wiki — they are point-in-time financial snapshots; the structural / policy content above captures the durable substance.

## Cross-references

- [[regulator-eu-mica-esma-hub]] — the EU regulatory frame that Circle does NOT mention on its transparency page; this absence is itself a finding.
- [[51-deck-april-2026]] — names "Stablecoin Issuer" as a category; Circle is referenced (as one named example among many) but no proprietary 51 product detail is reproduced in the deck source page either.
