---
type: vendor
name: Chainalysis
sector: [[regulatory-and-compliance]]
role: compliance-vendor
public_status: []
sources: 1
last_updated: 2026-04-27
---

# Chainalysis

> *Institutional-grade blockchain compliance and investigation platform; the wiki's first vendor in the [[regulatory-and-compliance]] sector. Positions itself as "the blockchain data platform" providing infrastructure for transaction monitoring (KYT), investigation (Reactor), risk assessment (Address Screening / VASP Risking / Sentinel), and emerging security (Hexagate / Alterya). Customer base spans 1,500+ entities including 9 of the top 10 crypto exchanges and 45+ regulators worldwide.*

## What it is

Chainalysis is a SaaS-model blockchain compliance and investigation vendor — distinct from the wiki's [[stablecoin-issuers]] and [[custody]] sector vendors in that Chainalysis is **not itself a regulated digital-asset entity**. Instead, it serves regulated entities (exchanges, custody vendors, banks, stablecoin issuers) and government clients (regulators, tax agencies, law enforcement) by providing the on-chain analytics layer that those clients use to satisfy their own regulatory obligations.

The product surface decomposes into three primary categories:

1. **Transaction monitoring**: KYT (Know Your Transaction) — real-time crypto transaction screening for compliance purposes.
2. **Investigation**: Reactor — multi-chain fund-flow tracing across bridges, mixers, DEX swaps, web3 infrastructure.
3. **Risk assessment**: Address Screening (wallet-level risk), VASP Risking (counterparty-VASP risk), Sentinel (token-level risk).

Plus emerging security products (Hexagate, Alterya) and Data Solutions for proactive threat intelligence.

The structural mechanism is **on-chain analytics**: "hundreds of clustering heuristics" combined with machine-learning techniques to identify entity ownership across blockchain transactions. The institutional-buyer trust claims are technical accuracy ("data accuracy with the lowest tolerance for error in the industry") and legal admissibility ("Chainalysis data is court admissible"). Both are designed to make Chainalysis's outputs defensible in regulator and court contexts.

For the wiki's institutional-buyer audience, Chainalysis fills a structurally distinct role from issuers and custodians: it is the compliance-tooling layer that turns regulator transaction-monitoring requirements (e.g. [[bitlicense|NYDFS]] 23 NYCRR Part 504, [[mica-compliance|MiCA]] Title V CASP supervisory obligations, FATF Travel Rule) into operational capability for the regulated vendor.

## Sector position

- Sector: [[regulatory-and-compliance]]
- Role: compliance-vendor
- Differentiation framing: SaaS-model blockchain analytics vendor serving 1,500+ institutional and government clients. The dominant institutional-grade compliance vendor by quantified market position ("Nine of the top ten crypto exchanges use Chainalysis"). Court-admissible data positioning and "lowest tolerance for error in the industry" methodology claims target the most-conservative institutional-buyer segment.

## Public moves cited

- [[vendor-chainalysis-homepage-2026-04]] — Chainalysis's public homepage articulating the multi-product surface (KYT, Reactor, Risk Assessment, Hexagate, Alterya, Data Solutions), the on-chain analytics methodology (clustering heuristics + ML), the customer-base scale (1,500+ customers, 45+ regulators), the named example clients across exchanges / financial institutions / tax agencies / infrastructure, and the structural trust claims (data accuracy, court admissibility, cross-chain tracing).

## Public regulatory status

_Sourced specifically from the cited source pages._

- **Empty `public_status:` field.** Chainalysis is a SaaS provider (not a regulated digital-asset entity itself); its regulatory posture is positioned through customer outcomes ("45+ regulators use Chainalysis") rather than through specific regulator licenses. This contrasts structurally with [[circle]], [[sky-protocol]], and [[bitgo]] — all of which have direct regulator-issued licenses or are deliberately operating without them.
- **Implicit regulatory alignment** with NYDFS 23 NYCRR Part 504 transaction-monitoring requirements, FATF Travel Rule, FinCEN AML expectations, OFAC sanctions screening, and MiCA Title V CASP supervisory standards — but the homepage does NOT name these frameworks explicitly. Open question whether product-specific documentation pages develop this.

## Concepts cited

- [[kyt-know-your-transaction]] — KYT is Chainalysis's flagship transaction-monitoring product; the canonical compliance-vendor product category.
- [[on-chain-analytics]] — the technical primitive on which Chainalysis's product surface is built.
- [[citation-discipline]] — Chainalysis's "court admissible" data positioning is structural citation discipline at the compliance-vendor product layer.
- [[counterparty-graph-research]] — Reactor (Chainalysis's investigation product) applies graph-traversal logic to on-chain transaction flows; the wiki's counterparty-graph-research concept (vendor-to-vendor graph traversal in research) is conceptually adjacent.
- [[bitlicense]] — NYDFS BitLicensees use Chainalysis-style products to satisfy 23 NYCRR Part 504 transaction-monitoring requirements.
- [[mica-compliance]] — MiCA CASPs use Chainalysis-style products to satisfy Title V supervisory transaction-monitoring obligations.

## Counterparties cited

_(Chainalysis's homepage names example clients but does not characterize them as legal-entity counterparties in the way that custodial / issuer vendors name auditors / fund managers / regulators. Named example clients on the homepage: Coinbase, Kraken, Crypto.com, eToro, BBVA, BNY [Mellon], IRS, Fireblocks, Tether. None of these have vendor pages in the wiki yet; future ingests will create them only on direct vendor-source ingests.)_

## Open questions

- **Specific regulatory framework alignment.** Homepage doesn't name NYDFS Part 504, FATF Travel Rule, FinCEN, OFAC, or MiCA explicitly. Product-specific documentation likely details these alignments. Future ingest territory.
- **Methodology transparency.** The "hundreds of clustering heuristics" claim is structural but not publicly detailed. Whether Chainalysis methodology supports independent technical evaluation by institutional buyers is an open question.
- **VASP Risking and FATF Virtual Asset Service Provider definitions.** The product positions on FATF terminology but doesn't detail the methodology for assessing VASP risk profiles.
- **Pricing and tier structure.** Not surfaced; institutional buyers would need direct sales engagement.
- **Comparison to other compliance vendors** named in [[51-deck-april-2026]]: TRM Labs, Elliptic, CipherTrace. None currently in the wiki.
- **Government-client relationship details.** The named-client list includes IRS; specific named-relationship content for other government clients would require separate Path A consideration if ingested.

## Sources cited

- [[vendor-chainalysis-homepage-2026-04]]
