---
type: concept
name: Self-improving substrate
sources: 1
last_updated: 2026-04-27
---

# Self-improving substrate

> *The compounding property of a [[karpathy-llm-wiki]]: maintenance cost approaches zero, so the wiki gets structurally richer with every ingest instead of decaying.*

## What it means

Human-maintained wikis decay because the bookkeeping cost (cross-reference updates, summary refresh, consistency across pages) grows faster than the value. LLMs do not get bored, do not forget to update a cross-reference, and can touch 15 files in one pass. So the maintenance cost approaches zero, and the wiki keeps getting richer instead of degrading.

This is "self-improvement" at the substrate level — the data layer becomes more capable monotonically as the corpus grows. Every new source adds a node and edges to the graph. Every lint pass surfaces drift. Every schema iteration tightens the contract. None of this requires retraining a model or running RL.

The framing matters because **substrate self-improvement composes cleanly with whatever model is in use** — today's, next year's, three years from now. It is not a fine-tuning play, and it does not depend on proprietary RL infrastructure. It is a structural property of the data layer.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass. The wiki stays maintained because the cost of maintenance is near zero."

## Mechanism / how it works

Five mechanisms compose to produce the compounding behavior:

1. **Each ingest adds graph nodes and edges.** New entities → new wiki-links → new traversal paths for queries.
2. **Each ingest can deepen existing pages.** A new source citing an existing concept bumps `sources:` count, refreshes `last_updated`, and may add a Notable Quote — without anyone being told to refresh.
3. **Lint surfaces drift automatically.** Contradictions, orphans, stale claims all become visible; the user reviews and approves fixes. This is a primitive form of an eval suite.
4. **The schema itself improves.** After ~4 seed ingests the LLM proposes a schema diff based on what worked (see [[schema-as-program]]). The schema *learns* from corpus contact.
5. **Citation discipline is forced by the substrate.** Query answers carry citations because the data layer makes it the path of least resistance (see [[citation-discipline]]).

In aggregate, these five mechanisms produce a substrate where the next query is structurally easier to answer than the previous one, and where the synthesis quality improves without explicit retraining.

## Related concepts

- [[karpathy-llm-wiki]] — parent pattern.
- [[ingest-query-lint-operations]] — the mechanism through which the substrate accumulates.
- [[schema-as-program]] — the schema-iteration component.
- [[citation-discipline]] — the structural-property component.
- [[wiki-curated-layer]] — where the compounding happens visibly.

## Related vendors / sectors

_(pre-domain — but worth flagging that this property is what makes the pattern applicable to digital-asset vendor research as a long-term substrate.)_

## Open questions

- How does the compounding behavior interact with proprietary corpora that have access tiers (public, contracted, private)? Does the substrate need three parallel wikis, or one wiki with frontmatter-level visibility flags?
- What's the empirical curve of substrate value vs. corpus size? Karpathy's "moderate scale ~100 sources" may be a phase-transition threshold for index-only navigation; is there an analogous threshold for compounding effect strength?

## Sources cited

- [[karpathy-llm-wiki-gist]]
