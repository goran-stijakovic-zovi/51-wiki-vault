---
type: firm
name: Skybase International
kind: other
jurisdiction:
sources: 1
last_updated: 2026-04-27
---

# Skybase International

> *Operator of the public sky.money interface for Sky Protocol. An "independent Sky Agent" that explicitly disclaims control over Sky Protocol smart contracts or ecosystem governance. Distinct from Sky Protocol itself; the structural separation between this interface operator and the underlying protocol is the canonical example of the [[non-custodial-interface-vs-issuer]] pattern in this wiki.*

## What it is

Skybase International is the legal entity operating the public-facing interface at sky.money for the [[sky-protocol]] stablecoin ecosystem. The relationship is structurally important: Skybase is **not** Sky Protocol — it operates the website that lets users interact with Sky Protocol smart contracts, but it explicitly disclaims control over the protocol, governance outcomes, and rates displayed on the interface.

The `kind: other` frontmatter value reflects that "interface operator" is a role not currently captured by the canonical firm-kind enumeration (`regulator | audit-firm | asset-manager | bank | custodian-firm | parent-company | consulting-firm | ratings-agency`). If a second DeFi-native protocol's interface operator enters the wiki with the same role pattern, this would graduate to a canonical kind value (per the schema's `other`-escape-hatch rule). For now, the role is captured in this body.

## How it shows up in sources

- [[vendor-sky-money-landing-2026-04]] — Skybase is named throughout the landing page as the interface operator, with structural disclaimers: "Sky.money is a non-custodial interface operated by Skybase, an independent Sky Agent with no control over Sky Protocol smart contracts or ecosystem governance"; "Skybase does not set, control, or guarantee any rates displayed on this interface"; "Skybase does not participate in, and has no ability to control or guarantee outcomes of, decentralized governance processes"; "Skybase International does not guarantee any level of yield, return, or protocol performance"; "Actual results could differ materially due to market volatility, regulatory changes, and decisions made through decentralized governance that are outside Skybase's control."

## Vendors / people associated

- [[sky-protocol]] — Skybase operates the public interface for Sky Protocol but does not control the protocol or its governance.

## Concepts associated

- [[non-custodial-interface-vs-issuer]] — Skybase is the canonical example of the interface-operator role in this architectural pattern.
- [[dao-governance]] — Skybase explicitly disclaims participation in Sky Protocol's DAO governance.

## Open questions

- **Skybase's legal jurisdiction and incorporation.** The landing page references "Skybase International" without specifying the country of incorporation. The legal-docs link points to https://docs.sky.money/legal/skybase-international/ which was not fetched during this ingest.
- **Skybase's revenue model.** As an interface operator that disclaims control over rates and protocol revenue, what's Skybase's commercial relationship to Sky Protocol? Future ingest territory.
- **The "Sky Agents" framing.** Skybase is described as "an independent Sky Agent." Whether this is a defined governance role or a generic descriptor is not addressed on the landing page.

## Sources cited

- [[vendor-sky-money-landing-2026-04]]
