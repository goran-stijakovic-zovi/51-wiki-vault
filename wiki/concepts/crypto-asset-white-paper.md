---
type: concept
name: Crypto-asset white paper
sources: 1
last_updated: 2026-04-27
---

# Crypto-asset white paper

> *The MiCA disclosure primitive — an issuer-prepared document analogous in role to a securities prospectus, machine-readable in iXBRL format from 23 December 2025, filed with the home Member State competent authority and listed in ESMA's interim MiCA register.*

## What it means

A crypto-asset white paper is the public disclosure document a MiCA issuer files about its crypto-asset before public offering or trading-platform admission in the EU. It is analogous in regulatory role to a securities prospectus, but with a specific structural property: ESMA does **not** review or approve the content. The disclosure burden is the issuer's, and the regulator's role is registry-keeper, not gatekeeper.

This structural property is significant for institutional buyers. A "MiCA-registered" status means the issuer filed the disclosure; it does **not** mean the contents have been validated by an EU competent authority. Independent due diligence on the white paper's claims remains a buyer obligation.

## How it shows up in sources

- [[regulator-eu-mica-esma-hub]] — ESMA's hub explicitly states: "The crypto-asset white papers listed in ESMA's register have not been reviewed or approved by any competent authority in any Member State of the European Union." The hub also notes that white-paper formatting entered into application on 23 December 2025, requiring iXBRL format for machine-readability.

## Mechanism / how it works

**Filing scope:** White papers cover crypto-assets in two of the three MiCA asset categories explicitly:

- Crypto-assets that are neither ART nor EMT (Title II "other crypto-assets") — white papers listed in the ESMA register.
- ART issuers (Title III) — white papers required as part of the authorisation package.
- EMT issuers (Title IV) — white papers required as part of the authorisation package.

**Format (in force from 23 December 2025):**

- **iXBRL** (Inline eXtensible Business Reporting Language) — a machine-readable XML-based format also widely used for EU prospectuses and corporate financial reporting.
- ESMA publishes a "MiCA White Paper Taxonomy 2025" defining the iXBRL tagging.
- Machine-readability is intended to make the white papers consumable by both regulators and downstream tooling (analytics platforms, supervisory reporting systems, institutional-buyer diligence systems).

**Disclaimer pattern:**

ESMA's stance is verbatim: white papers in the register "have not been reviewed or approved by any competent authority." This contrasts with prospectus regimes for traditional securities, which involve competent-authority approval before public offering. The MiCA model places disclosure responsibility on the issuer and surveillance responsibility on ESMA / NCAs, but **not** content-validation responsibility.

**Implication for the LLM-Wiki pattern:**

Machine-readable iXBRL white papers are a near-ideal raw-input source for a wiki-pattern substrate. A future fetcher could pull the ESMA register's weekly CSV, parse the linked iXBRL files, and auto-populate vendor frontmatter (`public_status:`, reserve composition, governance details) with structured citations back to specific iXBRL tags. This is an explicit Tier-3 candidate for a future scripts/fetcher addition (see `scripts/_README.md`).

## Related concepts

- [[mica-compliance]] — parent regulatory frame.
- [[asset-referenced-token]] — Title III issuers file white papers as part of authorisation.
- [[e-money-token]] — Title IV issuers file white papers as part of authorisation.
- [[crypto-asset-service-provider]] — CASPs filing under Title V also produce supervisory disclosures, though distinct from the issuer-side white paper.
- [[citation-discipline]] — white papers are designed to be citation-grade public sources, with iXBRL machine-readability supporting structural citation.
- [[proof-of-reserves]] — for ART/EMT issuers, the white paper plus periodic attestation reports together constitute the reserve-disclosure layer.

## Related vendors / sectors

- [[stablecoin-issuers]] — primary filers of EMT and ART white papers.
- [[regulatory-and-compliance]] — compliance vendors consume the white papers as authoritative source data.

## Open questions

- The iXBRL taxonomy is a structured-data spec; for an LLM Wiki, the "right" way to represent a white paper might be a wiki page with a `whitepaper_ixbrl_url:` frontmatter pointer plus extracted-claims body, rather than a flat raw-file ingest. Resolve when the first vendor-side white paper enters the wiki.
- ESMA's "not reviewed or approved" disclaimer puts the disclosure-quality burden on issuers. Are there empirical signals (white-paper completeness, iXBRL tag density, post-filing supervisory action) that institutional buyers track to gauge white-paper quality across issuers? Lint candidate for a later session.

## Sources cited

- [[regulator-eu-mica-esma-hub]]
