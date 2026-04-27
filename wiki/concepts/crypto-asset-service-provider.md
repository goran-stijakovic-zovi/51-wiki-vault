---
type: concept
name: Crypto-asset service provider (CASP)
sources: 1
last_updated: 2026-04-27
aliases: [casp]
---

# Crypto-asset service provider (CASP)

> *Entities providing services on crypto-assets — custody, exchange, transfer, execution, advice, portfolio management, placement — to clients in the EU. One of the four regulatory categories under [[mica-compliance]] (Title V).*

## What it means

CASPs (the regulatory acronym is widely used) are MiCA Title V's service-provider category: any entity offering one or more of the named crypto-asset services in or to the EU market needs CASP authorisation under Title V. Unlike the issuer-centric Titles III ([[asset-referenced-token|ART]]) and IV ([[e-money-token|EMT]]), Title V regulates the *service layer* — the vendors that move, hold, exchange, execute on, or advise about crypto-assets without necessarily issuing them.

For institutional buyers, the CASP authorisation is the relevant license check for [[custody|custodians]], exchanges, on/off-ramps, transfer-rail operators, and execution venues that target EU clients.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — ESMA's hub names CASPs as Title V coverage; the interim MiCA register lists "authorised crypto-asset service providers" as a separate entity class. Article 143's transitional provisions explicitly cover CASPs that were operating under national law before 30 December 2024.

## Mechanism / how it works

Title V CASP services typically cover (commonly cited categories from MiCA implementation literature; full enumeration in the regulation text):

- **Custody and administration** of crypto-assets on behalf of clients.
- **Operation of trading platforms** for crypto-assets.
- **Exchange** of crypto-assets for funds or for other crypto-assets.
- **Execution of orders** for crypto-assets on behalf of clients.
- **Placement** of crypto-assets.
- **Reception and transmission of orders** for crypto-assets.
- **Providing advice** on crypto-assets.
- **Portfolio management** on crypto-assets.
- **Transfer services** for crypto-assets.

CASP authorisation requirements include:

- Capital requirements (varying by service category).
- Governance and prudential standards.
- Conduct-of-business rules (suitability, best execution, conflicts of interest).
- Operational resilience and IT security.
- Filing white papers when applicable (e.g. when also acting as issuer).

**Article 143(3)** transitional provision: entities operating under national crypto-asset-services licenses before 30 December 2024 may continue until **1 July 2026** or until they receive a MiCA authorisation decision. **Article 143(6)** simplified-authorisation track: for entities authorised under national law on 30 December 2024.

For the wiki's `public_status:` frontmatter discipline, a CASP-relevant value would be `["MiCA-registered (CASP)"]` for an authorised provider, or `["MiCA-transitional (CASP)"]` for one operating under Article 143 during the transitional window.

## Related concepts

- [[mica-compliance]] — parent regulatory frame.
- [[asset-referenced-token]] — sister Title III category (issuers, not service providers).
- [[e-money-token]] — sister Title IV category (issuers, not service providers).
- [[qualified-custodian]] — overlaps with Title V's custody-and-administration service category, though qualified-custodian is a US-rooted concept (NYDFS / SEC / OCC) rather than an EU one. Worth tracking how the regimes converge or diverge for global custodians.
- [[citation-discipline]] — CASPs operating in the EU produce supervisory reports that are themselves citation-grade public sources for vendor diligence.

## Related vendors / sectors

- [[custody]] — custody is a Title V service.
- [[regulatory-and-compliance]] — compliance vendors map their tooling to CASP supervisory requirements (transaction monitoring, conduct-of-business reporting).
- [[payment-and-settlement]] — transfer-of-crypto-assets and exchange-for-funds are Title V services.
- [[stablecoin-issuers]] — issuers that *also* operate exchange or transfer services need both Title-III/IV authorisation and Title V CASP authorisation.

## Open questions

- The Article 143 transitional period creates a moving-target authorisation status for many CASPs through July 2026. The wiki's `public_status:` frontmatter discipline needs a way to mark this temporally — sub-state value or a `mica_transitional_until: 2026-07-01` field. Tentative direction: sub-state value.
- The boundary between "providing crypto-asset services" (CASP, Title V) and "operating a financial-instruments trading venue" (MiFID II) hinges on whether the underlying crypto-asset qualifies as a financial instrument. ESMA publishes a separate guideline on this — future ingest if a wiki vendor sits at the boundary.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
