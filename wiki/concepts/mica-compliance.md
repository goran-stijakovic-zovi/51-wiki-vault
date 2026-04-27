---
type: concept
name: MiCA compliance
sources: 1
last_updated: 2026-04-27
---

# MiCA compliance

> *The EU regulatory frame for crypto-assets — Regulation (EU) 2023/1114 — instituting uniform market rules for issuers and service providers across asset-referenced tokens, e-money tokens, other crypto-assets, and crypto-asset service providers.*

## What it means

The Markets in Crypto-Assets Regulation (MiCA) is the EU's uniform regulatory regime for crypto-asset markets that aren't already covered by other financial-services legislation. For an institutional buyer doing vendor diligence on any vendor that operates in or serves the EU market, MiCA registration status is a first-order screening criterion: a vendor is either MiCA-registered (under one of the relevant Titles), in transitional status under Article 143, operating outside MiCA scope, or non-compliant.

The regime decomposes into four regulatory categories:

- **[[asset-referenced-token]]** (Title III) — tokens referencing baskets, fiat currencies other than a single official currency, commodities, or other crypto-assets.
- **[[e-money-token]]** (Title IV) — tokens referencing a single official currency (the EU equivalent of stablecoins pegged to a single fiat).
- **Other crypto-assets** (Title II) — crypto-assets that are neither ART nor EMT.
- **[[crypto-asset-service-provider]]** (Title V) — entities providing services like custody, exchange, transfer, advice, portfolio management, etc. on crypto-assets.

The disclosure primitive is the [[crypto-asset-white-paper]], filed by issuers and (since 23 December 2025) required to use iXBRL machine-readable formatting.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — ESMA's institutional MiCA hub: scope statement, four categories, white-paper iXBRL requirement, ESMA's registry-keeper-not-gatekeeper stance, the interim MiCA register's weekly CSV cadence, the Article 143 transitional period, the implementation timeline.

## Mechanism / how it works

**Implementation timeline (verbatim from the source):**

- **Entry into Force**: June 2023.
- **Full Application**: December 2024.
- **Transitional Period (Article 143)**: 18 months, ending **1 July 2026**.
- **iXBRL White-Paper Formatting**: in force from **23 December 2025**.
- **MiCA Order Book / Records Keeping JSON Schema**: published 28 November 2025; NCAs expect compliance within 6 months.

**Article 143 transitional provisions:**

1. **Grandfathering (Art. 143(3))** — entities providing crypto-asset services per national law before 30 December 2024 may continue until 1 July 2026 or until authorisation decision.
2. **Simplified Authorisation (Art. 143(6))** — for entities already authorised under national law on 30 December 2024.

**ESMA's role and the interim register:**

ESMA maintains the **interim MiCA register** as **weekly-updated CSV files** (until formal IT integration in mid-2026). The register lists:

- White papers for non-ART / non-EMT crypto-assets.
- Issuers of asset-referenced tokens.
- Issuers of e-money tokens.
- Authorised crypto-asset service providers.
- **Non-compliant entities.**

Critically, ESMA states the listed white papers "have not been reviewed or approved by any competent authority." The regime puts disclosure responsibility on the issuer; ESMA's role is registry-keeper, not endorsement-issuer. This is structurally important for institutional-buyer trust: a MiCA-registered listing means the issuer filed the disclosure, **not** that ESMA validated it.

**Member State notification deadlines (Articles 93 / 99 / 108 / 111):**

- Designated competent authorities (Art. 93).
- Laws implementing Title VII (Art. 99) — deadline 30 June 2025.
- Administrative penalties rules (Art. 111) — deadline 30 June 2025.
- Complaints-handling procedures (Art. 108).

**Schema implication for the wiki**: Vendor `public_status:` frontmatter should be populated only when sourced from the ESMA register (or a snapshot of it), not from a vendor's own marketing claims. Possible values: `["MiCA-registered (ART)"]`, `["MiCA-registered (EMT)"]`, `["MiCA-registered (CASP)"]`, `["MiCA-transitional"]` (Article 143 status during the 2024-12-30 → 2026-07-01 window).

## Related concepts

- [[asset-referenced-token]] — Title III category (multi-reference stablecoins / baskets / commodities / other crypto-assets).
- [[e-money-token]] — Title IV category (single-fiat-reference stablecoins).
- [[crypto-asset-service-provider]] — Title V category (custody, exchange, transfer, etc.).
- [[crypto-asset-white-paper]] — the disclosure primitive.
- [[citation-discipline]] — MiCA's "issuer responsibility, ESMA registry-keeper" stance enforces disclosure discipline at the regulatory layer.
- [[counterparty-graph-research]] — MiCA registration status is a first-order edge label in the counterparty graph for any EU-touching vendor.

## Related vendors / sectors

- [[stablecoin-issuers]] — ART and EMT regimes apply directly to most issuer archetypes.
- [[custody]] — custody-of-crypto-assets is a CASP service under Title V.
- [[regulatory-and-compliance]] — MiCA is the central regulatory frame compliance vendors map to.
- [[payment-and-settlement]] — transfer-of-crypto-assets is a CASP service under Title V.

## Open questions

- The Article 143 transitional period creates a status distinct from "MiCA-registered" or "MiCA-non-compliant" — does the schema need an explicit `["MiCA-transitional"]` value? **Tentative yes**; will be confirmed if a later source shows a vendor in this state.
- ESMA's hub references the iXBRL machine-readable white-paper format. For an LLM Wiki, this is in principle a structured-data fetcher target — a `raw/regulators/eu-mica-register.csv` plus parsed white papers could populate vendor `public_status:` automatically. Tracked for `scripts/_README.md` future-fetcher list.
- Where does the Title II "other crypto-assets" boundary against MiFID II financial instruments lie? ESMA publishes a guideline on this; future ingest if a wiki vendor sits at this boundary.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
