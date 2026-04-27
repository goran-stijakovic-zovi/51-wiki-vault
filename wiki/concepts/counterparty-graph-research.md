---
type: concept
name: Counterparty-graph research
sources: 1
last_updated: 2026-04-27
---

# Counterparty-graph research

> *A research pattern in which a vendor is understood not in isolation but through its named regulators, settlement partners, integration partners, audit firms, and downstream protocol relationships — traversed as a graph rather than read as a profile.*

## What it means

A vendor's strategic posture is rarely visible from its product page alone. What matters for an institutional buyer is **who the vendor depends on, transacts with, and is regulated by** — the counterparties that, taken together, define the vendor's risk profile and growth surface. Counterparty-graph research maps these relationships explicitly: which regulators the vendor reports to, which settlement and custody partners it uses, which protocols integrate with its product, which audit firms verify its disclosures.

The pattern transforms vendor diligence from a profile-read into a **graph traversal**: start at a vendor node, walk outward to its named partners, register each partner as a node with its own incoming edges, and synthesize the picture from the connectivity. Done well, the work that traditionally takes weeks of primary research (calls, emails, document chasing) collapses to an afternoon of structured navigation.

## How it shows up in sources

- [[51-deck-april-2026]] — Slide 9 frames the pattern: "See a company's moves while they're still forming. Trace the full counterparty graph around any vendor." The deck shows a Circle counterparty mapping organized by partner type (blockchain infrastructure, cross-border payments, DeFi yield integration, exchange & trading distribution, government & regulatory partnerships, institutional custody & compliance, payment networks & card rails). **The wiki uses the *pattern* — graph traversal of counterparties — as a domain primitive; specific named-partner lists from the deck are excluded under Path A.**

## Mechanism / how it works

A wiki-pattern substrate maps onto this research pattern naturally:

- **Vendor pages** carry their own first-mention wiki-links to firm and vendor pages, which capture the counterparties.
- **Firm pages** (regulators, audit firms, parent companies) accumulate inbound links from every vendor that names them, surfacing partner-density in the graph view.
- **Source pages** ground each named relationship — a "Circle uses BNY Mellon as a custodian" claim is wiki-linked to the public attestation source that named the relationship, not to a free-text reference.
- **The lint operation** can surface counterparty-graph anomalies: a vendor named in 4+ source pages but with no incoming wiki-links from the firms it ostensibly works with; a regulator named on a vendor page but missing its own firm page.

In practice, counterparty-graph research is the workflow that justifies the wiki's investment in entity discipline. A flat document store does not produce graph traversal; a wiki-pattern substrate does.

## Related concepts

- [[institutional-digital-asset-buyer]] — the audience that needs counterparty-graph research most.
- [[citation-discipline]] — what makes the named-partner claims defensible.
- [[ingest-query-lint-operations]] — the operations that maintain the graph.
- [[karpathy-llm-wiki]] — the substrate that supports graph traversal natively.

## Related vendors / sectors

- [[custody]] — sector where counterparty-graph relationships are densest (custodian → audit firm → regulator → asset issuer chains).
- [[stablecoin-issuers]] — sector where counterparty-graph is especially load-bearing (issuer → reserve custodian → audit firm → primary-jurisdiction regulator).

## Open questions

- What's the right granularity for capturing relationships — a wiki-link is binary (page A links to page B), but real counterparty relationships have types (custodian-of, audit-firm-of, regulator-of). Does the schema need a relationship-type frontmatter field, or are the body-level prose phrasings sufficient?
- For protocol vendors (Sky, Aave, etc.), counterparties include other smart contracts and on-chain holders. How does the wiki-pattern substrate model on-chain relationships that aren't named legal entities?

## Sources cited

- [[51-deck-april-2026]]
