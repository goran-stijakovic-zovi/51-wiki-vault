---
type: concept
name: Retail-grade intelligence gap
sources: 1
last_updated: 2026-04-27
---

# Retail-grade intelligence gap

> *The structural mismatch in which institutional digital-asset decisions get made on tools built for retail traders, VC dealflow, generic enterprise market research, or on-chain analytics — none of which were designed for institutional vendor selection.*

## What it means

Existing intelligence tools serve adjacent domains: retail trading apps optimize for individual investor speed and price discovery; VC dealflow databases optimize for funding-round and cap-table data; generic enterprise market-research platforms (Gartner, Forrester) optimize for IT vendor selection in mature categories; on-chain analytics tools (Artemis, Dune, Kaiko) optimize for protocol-level transaction signal. None of them produce the kind of artifact an institutional digital-asset buyer needs: a citation-clean, license-clean, structured comparison of digital-asset vendors at the level of an institutional consulting deliverable.

The gap shows up as **time and confidence costs**: institutional teams stitch together five-to-ten tools per workflow, spend most of analyst time on gathering and verifying rather than analyzing, and end up rebuilding deliverables from scratch each engagement.

## How it shows up in sources

- [[51-deck-april-2026]] — Slide 2 frames the problem: "Institutions are making eight-figure digital asset decisions on retail-grade intelligence." Slide 4 enumerates the specific status-quo limitations across CB Insights, Gartner, Messari, Bloomberg, Artemis / Dune, PitchBook, RWA.xyz.

## Mechanism / how it works

The mismatch has three observable forms:

1. **Coverage gap** — generic platforms (CB Insights, Gartner) have shallow digital-asset coverage relative to broad market data; crypto-native platforms (Messari, Artemis, RWA.xyz) have depth but narrow scope (token-investor framing, on-chain only, tokenized-RWA only).
2. **Taxonomy mismatch** — generic taxonomies don't carve up "stablecoin issuers" vs. "custody" vs. "compliance vendors" the way an institutional buyer needs to compare them; crypto-native taxonomies optimize for protocol or token concepts, not for vendor archetypes that map to institutional procurement decisions.
3. **Licensing limitations** — many platforms restrict external use of their data, which means a consulting firm cannot redistribute the analysis in client deliverables without paying again or paying differently.

The wiki-pattern substrate addresses all three: **coverage** by curating sources at the institutional-buyer scope; **taxonomy** by defining sector / vendor / concept entity types in the schema; **licensing** by being a public-source-only artifact (Path A) that the institutional buyer can fork and re-ingest with their own contracted sources for proprietary use.

## Related concepts

- [[institutional-digital-asset-buyer]] — the audience this gap affects.
- [[citation-discipline]] — what license-clean deliverables structurally require.
- [[counterparty-graph-research]] — one workflow this gap makes especially expensive (named regulators, settlement partners, integration partners).

## Related vendors / sectors

_(this concept is gap-level, not vendor-specific. It applies across all four sectors named on the deck.)_

## Open questions

- The 51 deck contrasts itself with seven existing platforms — does the gap differ qualitatively across them (CB Insights' coverage gap vs. Messari's audience-fit gap vs. Bloomberg's no-vendor-layer gap), or are they all variations of the same root mismatch?
- For institutional buyers who already license one of these platforms, what's the integration story — is the wiki-pattern substrate a replacement, or a layer on top?

## Sources cited

- [[51-deck-april-2026]]
