---
type: firm
name: New York State Department of Financial Services (NYDFS)
kind: regulator
jurisdiction: US-NY
sources: 1
last_updated: 2026-04-27
---

# New York State Department of Financial Services (NYDFS)

> *The New York State financial-services regulator. Operates two parallel virtual-currency authorisation regimes — the [[bitlicense|BitLicense]] (codified at 23 NYCRR Part 200) and the [[limited-purpose-trust-charter|Limited Purpose Trust Charter]] (under NY Banking Law). Maintains the public Regulated Entities list (regulator-side source of truth for vendor licensing status) and the [[nydfs-greenlist|Greenlist]] of approved coins.*

## What it is

NYDFS is the New York State Department of Financial Services — the US-state-level regulator with the densest digital-asset rule-making in the United States. NYDFS supervises BitLicensees, Limited-Purpose-Trust-chartered companies, and Money Transmitter Licensees that engage in virtual-currency business activity involving New York or New York Residents. Its rule-making and guidance directly affect issuers ([[circle]], future stablecoin-issuer ingests), custodians (BitGo, Gemini, Coinbase Custody all use the trust charter), and payment / settlement vendors (Coinbase, PayPal, Block all hold BitLicense + MTL).

For an institutional buyer doing US-side diligence on any digital-asset vendor whose activity touches New York, NYDFS is a first-order screening counterparty: the Regulated Entities list and the Greenlist are public records that materially inform the diligence outcome.

## How it shows up in sources

- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS's own canonical public page describing the BitLicense regime, the Limited Purpose Trust Charter alternative, the Regulated Entities list, the Greenlist, and the operational supervision framework.

## Vendors / people associated

- [[circle]] — BitLicense + MTL since 2015-09 (Circle Internet Financial, LLC); confirmed via the NYDFS Regulated Entities list.
- Forward references in this wiki: BitGo (Limited Purpose Trust Charter since 2021-03 for BitGo New York Trust Company, LLC), Coinbase / Coinbase Custody, PayPal, Block, Gemini, bitFlyer, Ripple Markets — all currently named in the NYDFS source page but with vendor pages that will emerge from their own direct vendor-source ingests.

## Concepts associated

- [[bitlicense]] — NYDFS's central virtual-currency-regulatory primitive.
- [[limited-purpose-trust-charter]] — NYDFS's alternative regulatory path for fiduciary-powers vendors.
- [[nydfs-greenlist]] — NYDFS's static list of 8 approved coins (BTC, ETH, GUSD, GYEN, ZUSD, RLUSD, USDW, GOLD) + the three-paths-to-listing mechanism.
- [[mica-compliance]] — NYDFS's regulatory analogue at the EU level. Different jurisdictional scope, structurally different mechanism (NYDFS supervises licensees vs. ESMA coordinates a register-based regime), but both are first-order screening regimes for international issuers.
- [[citation-discipline]] — the Regulated Entities list is the canonical regulator-side source of truth that enables vendor `public_status:` discipline in this wiki.
- [[counterparty-graph-research]] — NYDFS is one of the most-named regulator counterparties in the wiki's vendor graph.

## Open questions

- **NYDFS guidance documents** (2022-06-08 stablecoin issuance, 2025-09-30 custodial structures, 2023-11-15 listing guidance, etc.) are referenced from the source page but not ingested. Future ingest of the specific guidance documents would substantively expand this firm page's relationship to [[stablecoin-issuers]] / [[custody]] / [[payment-and-settlement]].
- **NMLS — the Nationwide Multistate Licensing System** — referenced as the application channel but not characterized as a separate entity in this wiki. If multiple state regulators surface in future ingests, NMLS may warrant its own page as a multi-state-coordinator firm.

## Sources cited

- [[regulator-nydfs-bitlicense-page-2026-04]]
