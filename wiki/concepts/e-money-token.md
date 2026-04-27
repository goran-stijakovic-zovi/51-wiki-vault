---
type: concept
name: E-money token (EMT)
sources: 2
last_updated: 2026-04-27
---

# E-money token (EMT)

> *Crypto-assets that purport to maintain stable value by referencing the value of one official currency. One of the four regulatory categories under [[mica-compliance]] (Title IV).*

## What it means

An e-money token (EMT) is a MiCA Title IV category: a token whose value is anchored to a **single official currency** (typically the euro, US dollar, or another sovereign fiat). EMTs are the EU regulatory home for what are commonly called single-fiat stablecoins. The Title IV regime applies authorisation, white-paper disclosure, and reserve requirements distinct from those for [[asset-referenced-token|asset-referenced tokens]] (Title III, multi-reference) and "other crypto-assets" (Title II, neither ART nor EMT).

For institutional buyers in the EU market, the practical implication is that USD-pegged stablecoins (USDC, USDT, etc.) and EUR-pegged stablecoins fall under Title IV when they operate in or serve EU jurisdiction.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — ESMA's hub names EMT as one of three primary asset categories under MiCA, governed by Title IV. The interim MiCA register lists EMT issuers as a separate entity class.
- [[vendor-circle-transparency-page-2026-04]] — Circle's USDC and EURC are single-fiat-pegged tokens (USD and EUR respectively) — EMT-archetype issuers under MiCA framing. Notably, Circle's transparency page does NOT mention MiCA registration status; the EU-side disclosure layer is absent from the page even though the token shape qualifies as an EMT structurally.

## Mechanism / how it works

The defining property of an EMT is **single-reference stabilisation** — the token's value is intended to track exactly one official currency. The boundary against [[asset-referenced-token|ART]] (Title III) is the multi-reference dimension: any basket, commodity, or multi-fiat token falls under ART instead.

Title IV obligations include:

- Authorisation by an EU competent authority for the issuer (often building on existing e-money licensing regimes — there is overlap with the EU's E-Money Directive in legacy form, which makes Title IV a relatively familiar regulatory shape for fintech-rooted institutions).
- Filing a [[crypto-asset-white-paper]] (iXBRL machine-readable from 23 December 2025).
- Reserve obligations: 1:1 reserve coverage in the referenced currency, with restrictions on reserve composition.
- Supervisory reporting and ongoing disclosure obligations.

The Title IV regime is generally regarded as the closer of the two stablecoin tracks (Title III vs. Title IV) to existing EU e-money licensing — institutions with prior e-money authorisation often have a more direct on-ramp to EMT issuance.

## Related concepts

- [[mica-compliance]] — parent regulatory frame.
- [[asset-referenced-token]] — sister Title III category (multi-reference).
- [[crypto-asset-service-provider]] — entities providing services on EMT tokens are subject to Title V.
- [[crypto-asset-white-paper]] — disclosure primitive EMT issuers must file.
- [[proof-of-reserves]] — concept that emerges with Circle's reserve attestation source (4); single-fiat 1:1 reserve coverage is the institutional implementation of Title IV reserve obligations.

## Related vendors / sectors

- [[stablecoin-issuers]] — single-fiat-pegged issuers (USDC, USDT, EUR-pegged stablecoins) are EMT-archetype issuers under MiCA framing.
- [[circle]] — single-USD-pegged (USDC) and single-EUR-pegged (EURC) issuer; EMT-archetype structurally, though MiCA registration status is not surfaced on Circle's transparency page (open question on the [[circle]] vendor page).

## Open questions

- The Title IV regime's overlap with the existing E-Money Directive is partial — does the wiki need a `e-money-directive` concept page to disambiguate, or is "Title IV" sufficient as a regulatory anchor in the EMT page itself? Resolve when a future source substantively touches it.
- Reserve-composition restrictions under Title IV: what's permitted (Treasury bills, central-bank deposits, commercial-bank deposits), and at what concentration limits? **Partial answer from Circle**: Circle's USDC reserve composition (cash + short-dated US Treasuries + overnight Treasury repos, with majority in an SEC-registered 2a-7 government MMF) is structurally close to the asset classes typically permitted under Title IV reserve rules, but Circle's transparency page does not explicitly map its reserve to MiCA Title IV requirements.
- **Circle's MiCA registration status as of 2026-04 is an open question** — see [[circle]] page. Substantively answered if/when an EU-side regulator source or Circle EU disclosure enters the wiki.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
- [[vendor-circle-transparency-page-2026-04]]
