---
type: concept
name: On-chain analytics
sources: 1
last_updated: 2026-04-27
---

# On-chain analytics

> *The technical discipline of extracting actionable intelligence from public blockchain transaction data. The structural primitive underlying compliance-vendor products like KYT and investigation tools like Reactor; methodologically rooted in clustering heuristics + machine-learning techniques applied at scale.*

## What it means

Public blockchains produce transaction data in massive volumes — every block contains dozens or thousands of transactions, each linking sender / receiver addresses with values and timestamps. **On-chain analytics** is the engineering and methodological discipline of turning this raw transaction firehose into entity-level intelligence: which addresses are controlled by the same entity, which entities are sanctioned / illicit / known custodians / known exchanges, what fund-flows imply about activity patterns.

The institutional-grade compliance and investigation use cases (KYT, sanctions screening, Reactor-style fund-tracing, market intelligence) all sit on top of an on-chain analytics layer. The vendor's ability to produce defensible answers depends on the methodology of this layer: how addresses are clustered, how entity classifications are made, how cross-chain bridges are handled, how data is verified at scale.

## How it shows up in sources

- [[vendor-chainalysis-homepage-2026-04]] — Chainalysis articulates its on-chain analytics methodology as a structural moat: "Using sophisticated machine learning techniques coupled with proprietary architecture, we are built to handle hundreds of clustering heuristics, ingest data at scale, and verify data accuracy with the lowest tolerance for error in the industry." Plus the multi-chain capability claim: "Chainalysis simplifies the complex and makes it effortless to trace the flow of funds through bridges, mixers, DEX swaps, and more."

## Mechanism / how it works

Three structural components (synthesized from the Chainalysis source; specific methodology not publicly detailed):

1. **Address clustering** — heuristics that group multiple addresses into a single entity. Common heuristics include common-input-ownership (multi-input transactions imply common control), behavioral-pattern matching, off-chain identifiers correlated with on-chain behavior. The number of heuristics matters because each one captures a different kind of signal.

2. **Entity classification** — labeling clustered entities as exchanges, mixers, sanctioned addresses, ransomware infrastructure, retail wallets, institutional custodians, etc. Classification is partly inferred from on-chain behavior and partly from off-chain intelligence (court records, public OFAC lists, vendor research).

3. **Cross-chain tracing** — following fund-flows across bridges (Ethereum ↔ other L1s/L2s), mixers (Tornado Cash and similar), DEX swaps (Uniswap-style automated market makers), and other DeFi protocols. The fund-flow graph traverses protocol boundaries, not just blockchain boundaries.

Critical institutional-buyer quality dimensions:

- **Accuracy** — false-positive rates (legitimate transactions flagged as illicit) and false-negative rates (illicit transactions missed). Chainalysis's positioning: "the lowest tolerance for error in the industry."
- **Court admissibility** — whether the analytics output is robust enough to support enforcement actions. Chainalysis: "Chainalysis data is court admissible and has uniquely helped customers take ground-breaking actions in court."
- **Coverage** — which blockchains, which protocols, which DeFi primitives are supported.
- **Scale** — the ability to ingest and process the full transaction firehose in real-time.

## Related concepts

- [[kyt-know-your-transaction]] — the compliance product category built on top of on-chain analytics.
- [[counterparty-graph-research]] — on-chain analytics applied to fund-flow tracing IS counterparty-graph research at the protocol layer; the wiki's higher-level concept (vendor-to-vendor graph traversal in research) is the institutional-buyer-domain analogue.
- [[citation-discipline]] — court-admissibility positioning for analytics output is citation-discipline at the technical-product layer.
- [[bitlicense]] — NYDFS 2022-04-28 "Guidance on Use of Blockchain Analytics" (referenced from [[regulator-nydfs-bitlicense-page-2026-04]]) is the regulator-side anchor; on-chain analytics products are the operational implementation.

## Related vendors / sectors

- [[regulatory-and-compliance]] — sector that consumes on-chain analytics most heavily.
- [[chainalysis]] — wiki's canonical on-chain-analytics vendor.

## Open questions

- **Methodology transparency.** "Hundreds of clustering heuristics" is structural but not publicly detailed. Independent technical evaluation of clustering accuracy is difficult without methodology disclosure. Whether vendors like Chainalysis publish enough methodology to support independent peer review is an open question for institutional buyers in highly-regulated jurisdictions.
- **Privacy-protocol coverage.** Mixers, privacy coins, zero-knowledge protocols all complicate on-chain analytics. Chainalysis's homepage claims tracing through "mixers" specifically; the underlying technical limits are not publicly detailed.
- **Cross-chain coverage breadth.** Bridges, DEX swaps, and CEX deposits are named on the homepage; the actual list of supported chains and protocols is not enumerated.
- **Comparison across vendors.** Chainalysis is the wiki's canonical example; TRM Labs, Elliptic, and others claim similar capabilities but use different methodologies. Substantive comparison would require source-side ingest from multiple vendors.

## Sources cited

- [[vendor-chainalysis-homepage-2026-04]]
