---
type: concept
name: Asset-referenced token (ART)
sources: 1
last_updated: 2026-04-27
---

# Asset-referenced token (ART)

> *Crypto-assets that purport to maintain stable value by referencing another value or right, or a combination thereof — including baskets, commodities, fiat currencies (other than a single official currency), or other crypto-assets. One of the four regulatory categories under [[mica-compliance]].*

## What it means

An asset-referenced token (ART) is a MiCA Title III category: a token whose value is anchored to a basket of underlying values or rights — multiple fiat currencies, commodities (gold, silver), other crypto-assets, or any combination — rather than to a single official currency. The Title III regime applies authorisation, white-paper disclosure, and reserve / governance requirements distinct from those for [[e-money-token|e-money tokens]] (Title IV) and "other crypto-assets" (Title II).

For an institutional buyer doing vendor diligence on a stablecoin issuer that targets EU jurisdiction, the ART vs. EMT classification is the first technical decision — it determines which Title applies and therefore which authorisation regime, reserve obligations, and supervisory authority govern the issuer.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — ESMA's hub names ART as one of three primary asset categories under MiCA, governed by Title III. The interim MiCA register lists ART issuers as a separate entity class, distinct from EMT issuers and authorised CASPs.

## Mechanism / how it works

The defining property of an ART is **multi-reference stabilisation** — the token's value is intended to track a basket or composite, not a single official currency. Examples (from public market knowledge, to be cross-confirmed by future sources):

- Baskets of multiple fiat currencies (e.g. SDR-style basket tokens).
- Tokens referencing precious metals (e.g. gold-backed tokens).
- Tokens with mixed crypto-asset and fiat collateral.

Title III obligations include:

- Authorisation by an EU competent authority before public offering or trading admission in the EU.
- Filing a [[crypto-asset-white-paper]] (iXBRL machine-readable from 23 December 2025) with the home Member State's competent authority.
- Reserve, governance, and prudential requirements specific to multi-reference stability.
- Supervisory reporting and ongoing disclosure obligations.

The boundary between ART and EMT is set by the **single-vs-multi reference** dimension. A token referencing only one fiat currency falls under Title IV (EMT); a token referencing more than one, or a basket, or a commodity, falls under Title III (ART). Stablecoin issuers that operate USD-pegged tokens for EU jurisdictions therefore typically fall under EMT, not ART.

## Related concepts

- [[mica-compliance]] — parent regulatory frame.
- [[e-money-token]] — sister Title IV category (single-fiat-reference).
- [[crypto-asset-service-provider]] — entities providing services on ART tokens are subject to Title V.
- [[crypto-asset-white-paper]] — disclosure primitive ART issuers must file.

## Related vendors / sectors

- [[stablecoin-issuers]] — multi-reference issuers (basket-pegged, commodity-pegged) are ART issuers under MiCA.

## Open questions

- The wiki currently has no Session-1 ART-issuer vendors in the seed list (Circle is USD-pegged → EMT; Sky's collateralisation model needs the source-5 ingest to clarify). When a multi-reference issuer enters the wiki, this concept page graduates from "structural placeholder" to "lived case study."
- The Title III obligations on ART are reportedly more stringent than EMT in some areas (governance, reserve composition). Future ingest of an ART-issuer source could substantively develop the comparative regime.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
