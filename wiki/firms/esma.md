---
type: firm
name: European Securities and Markets Authority (ESMA)
kind: regulator
jurisdiction: EU
sources: 1
last_updated: 2026-04-27
---

# European Securities and Markets Authority (ESMA)

> *EU-level supervisory authority for securities markets; for MiCA, the central coordinator of the regulation across Member State competent authorities and the keeper of the interim MiCA register of issuers and CASPs.*

## What it is

ESMA is one of the EU's three European Supervisory Authorities (with the European Banking Authority — EBA — and the European Insurance and Occupational Pensions Authority — EIOPA). It supervises securities markets at the EU level and coordinates national competent authorities (NCAs) across Member States.

For [[mica-compliance|MiCA]], ESMA's role is regulatory coordinator and registry-keeper:

- Maintains the **interim MiCA register** as weekly-updated CSV files until mid-2026.
- Publishes technical standards, joint Q&As, and guidelines (including the iXBRL white-paper taxonomy).
- Coordinates Member State notification of competent authorities, penalty regimes, and complaints-handling procedures (Articles 93 / 99 / 108 / 111).
- Operates jointly with EBA on cross-cutting MiCA matters.

ESMA explicitly does **not** review or approve crypto-asset white papers in its register — disclosure responsibility lies with issuers. ESMA's role is registry-keeper, not endorsement-issuer.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — primary publisher of the source page; central authority described.

## Vendors / people associated

_(none in this source — vendors with MiCA-registered status will cross-reference ESMA via their own source pages once ingested.)_

## Concepts associated

- [[mica-compliance]] — ESMA is the EU-level coordinator.
- [[asset-referenced-token]] — register tracks ART issuers.
- [[e-money-token]] — register tracks EMT issuers.
- [[crypto-asset-service-provider]] — register tracks authorised CASPs.
- [[crypto-asset-white-paper]] — ESMA's interim register lists and links the iXBRL-formatted white papers.

## Open questions

- The interim register's mid-2026 IT-systems integration: does this change how downstream tooling (institutional-buyer diligence platforms, LLM Wikis like this one) consume MiCA registration data? Likely yes — but the consumption interface is not yet specified in the source.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
