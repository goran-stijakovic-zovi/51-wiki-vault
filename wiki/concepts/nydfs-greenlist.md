---
type: concept
name: NYDFS Greenlist
sources: 1
last_updated: 2026-04-27
---

# NYDFS Greenlist

> *A static list of coins that may be offered by [[nydfs|NYDFS]]-licensed virtual-currency entities without separate DFS approval. The Greenlist is one of three paths NYDFS offers VC entities to add a coin to their offering; the other two are individual DFS application approval and self-certification under a DFS-approved policy.*

## What it means

The Greenlist is a regulatory expediency mechanism: rather than require every NYDFS-licensed entity to seek separate DFS approval for every coin it offers, NYDFS publishes a list of coins that all licensees may offer (with 10-day notice). The list is small and conservative — 8 coins as of 2026-04-27 — but its publication dynamics are structurally important: NYDFS retains discretionary authority to add coins, remove coins, or "discontinue the Greenlist process entirely" at any time.

For institutional buyers, the Greenlist is **one of two distinct vendor-status questions**. The other is whether a vendor itself is licensed (BitLicense or Limited Purpose Trust Charter). The two are structurally separate: a coin can be Greenlisted without its issuer holding any NYDFS license (the Greenlist applies to *licensed entities offering the coin*, not to the coin's issuer); a vendor can hold a BitLicense without that vendor's own coins being Greenlisted.

## How it shows up in sources

- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS's main page publishes the static Greenlist (8 coins as of fetch) and describes the three-paths-to-listing mechanism.

## Mechanism / how it works

**Coins on the Greenlist as of 2026-04-27:**

| Coin | Symbol | Type |
|------|--------|------|
| Bitcoin | BTC | non-stablecoin |
| Ethereum | ETH | non-stablecoin |
| Gemini Dollar | GUSD | USD-pegged stablecoin |
| GMO JPY | GYEN | JPY-pegged stablecoin |
| GMO USD | ZUSD | USD-pegged stablecoin |
| Ripple USD | RLUSD | USD-pegged stablecoin |
| WisdomTree Dollar | USDW | USD-pegged stablecoin |
| WisdomTree Gold | GOLD | gold-referenced |

Notable absences: USDT (Tether), USDC (Circle's stablecoin even though Circle holds a BitLicense), DAI, USDS, FDUSD, USDP (Paxos). The Greenlist's small scope is itself a finding for institutional buyers — the list is highly curated, and many widely-used stablecoins are not on it.

**Three paths to listing a coin** (from the NYDFS source):

1. **Specific DFS application approval** for a material business change. Vendor-by-vendor, coin-by-coin.
2. **Self-certification under a DFS-approved coin listing policy.** Filed via the DFS Portal at myportal.dfs.ny.gov. The policy itself must be approved by DFS before self-certifications under it are accepted.
3. **Use of a coin already on the Greenlist** with 10-day notice to DFS.

**Discretionary authority retained by DFS (verbatim):**

> "DFS may, at any time and in its sole discretion, prohibit or otherwise limit a coin's use before or after a VC Entity begins using a coin; require that any VC Entity delist, halt, or otherwise limit or curtail activity with respect to any coin; remove any coin from the Greenlist; refrain from placing any coin on the Greenlist; or discontinue the Greenlist process entirely."

This discretionary stance is structurally important: a coin's Greenlist presence is **not a permanent property**. Institutional-buyer diligence on Greenlist status must reflect this — the static list as published is a current-state snapshot that NYDFS may change unilaterally.

## Related concepts

- [[bitlicense]] — vendor-side licensing regime. The Greenlist is coin-side; the two are complementary, not interchangeable.
- [[limited-purpose-trust-charter]] — alternative vendor-side licensing regime. Trust-chartered vendors are subject to the same Greenlist + self-certification mechanism for adding coins to their offering.
- [[citation-discipline]] — the Greenlist is one example of NYDFS's regulator-side public surface that the wiki's source-driven discipline cites.

## Related vendors / sectors

- [[stablecoin-issuers]] — sector most affected by Greenlist status. USDC's absence from the Greenlist (despite Circle holding a BitLicense) is a structurally interesting finding.
- [[circle]] — Circle's BitLicense covers Circle's own activity, but USDC is not on the Greenlist as of this fetch. Open question on the Circle vendor page.
- [[regulatory-and-compliance]] — compliance vendors integrate the Greenlist into their listing-policy workflows for client VC entities.

## Open questions

- **Why is USDC not on the Greenlist?** Circle is BitLicensed (controlling/administering/issuing a virtual currency, Part 200(5)). The Greenlist mechanism is for coins offered by *other* licensed entities — so the question is whether other NYDFS-licensed VC entities offering USDC do so under DFS-approved listing policies (path 2) or specific approvals (path 1). Material to institutional-buyer diligence on USDC's NY-side regulatory pathway.
- **The Greenlist's curation logic.** What criteria determine inclusion? The NYDFS source page does not articulate the inclusion criteria; future ingest of NYDFS's "General Framework for Greenlisted Coins" guidance (2023-09-18) would substantively develop this.
- **The 10-day-notice mechanism.** Operationally, what does notice consist of? Filed via the DFS Portal. Future-ingest territory if the procedural details become institutionally relevant.

## Sources cited

- [[regulator-nydfs-bitlicense-page-2026-04]]
