---
type: concept
name: 2a-7 government money market fund
sources: 1
last_updated: 2026-04-27
---

# 2a-7 government money market fund

> *A US-securities-law primitive: a money market fund registered with the SEC under Rule 2a-7 of the Investment Company Act of 1940, restricted to government securities (US Treasury bills, agency debt, government repos, cash). Used by stablecoin issuers as a regulator-grounded reserve vehicle.*

## What it means

Rule 2a-7 (under the Investment Company Act of 1940) is the SEC's regulatory framework for **money market funds** — pooled investment vehicles that buyers use as cash equivalents because they aim to maintain a stable net asset value of $1 per share. A "government" 2a-7 fund is a sub-class restricted to government securities (US Treasury bills, agency obligations, government-secured repos, cash) with no exposure to corporate paper or longer-duration credit.

For a centralized stablecoin issuer, holding the majority of reserves in a 2a-7 government MMF is a structurally significant choice. The fund itself is SEC-registered with continuous portfolio disclosure obligations; an independent fund administrator manages it; daily portfolio reporting is publicly available. The issuer inherits the regulatory transparency of this vehicle for that portion of reserves — which is structurally stronger than holding the same assets in a self-managed, opaque "we hold Treasuries" arrangement.

## How it shows up in sources

- [[vendor-circle-transparency-page-2026-04]] — Circle's transparency page names the **Circle Reserve Fund (USDXX)** as "an SEC-registered 2a-7 government money market fund" holding the majority of USDC reserves. The fund is managed by [[blackrock]]; daily independent third-party portfolio reporting is publicly available via BlackRock's product page.

## Mechanism / how it works

**Regulatory anchoring (Rule 2a-7 highlights):**

- Continuous disclosure obligations (portfolio holdings, weighted average maturity, weighted average life).
- Liquidity requirements (daily liquid assets, weekly liquid assets).
- Credit quality requirements (government MMFs restricted to government securities).
- Independent administrator and fund accountant.
- Independent auditor.

**Why a stablecoin issuer would use this structure:**

1. **Institutional credibility** — institutional buyers already know how to evaluate a 2a-7 MMF; the structure is familiar from corporate treasury and money market investing.
2. **Regulatory transparency inheritance** — the fund's SEC obligations create a public reporting layer that exists independently of the issuer's own disclosures.
3. **Liquidity discipline** — Rule 2a-7's liquid-asset requirements are aligned with the redemption-on-demand commitment of a 1:1 stablecoin.
4. **Custody-and-administration separation** — the asset manager (BlackRock for USDXX) is structurally separate from the issuer (Circle), reducing single-counterparty risk.

**Limitations:**

- Only the *majority* of Circle's reserves sit in USDXX. The remainder is in cash deposits at unnamed "leading global banks." The 2a-7 grounding does not extend to that portion.
- A 2a-7 government MMF is not a guarantee of pegging — it provides reserve-asset disclosure and quality, not arbitrage liquidity. The peg mechanism (1:1 mint/redeem with Circle) operates on top of the reserve vehicle, not within it.
- Rule 2a-7 is US-specific. EU institutional buyers may evaluate this structure as additional comfort but the EU regulatory frame ([[mica-compliance]]) is independent.

## Related concepts

- [[proof-of-reserves]] — 2a-7 MMF grounding is a strong structural component of a robust proof-of-reserves regime.
- [[citation-discipline]] — SEC-registered MMFs produce continuous public disclosure; the structure is a citation-discipline-by-design vehicle.
- [[mica-compliance]] — under EU MiCA, single-fiat-pegged stablecoins (EMTs) face Title IV reserve requirements that are structurally analogous to but legally independent from US 2a-7 grounding. A vendor with a US 2a-7 reserve vehicle still needs separate MiCA authorisation for EU operations.
- [[counterparty-graph-research]] — the fund manager (BlackRock for USDXX) and the fund administrator are named counterparties in the issuer's graph.

## Related vendors / sectors

- [[stablecoin-issuers]] — primary vendor archetype using this structure.
- [[circle]] — canonical example via the Circle Reserve Fund (USDXX).
- [[blackrock]] — manager of USDXX; an asset-management firm whose reputation and SEC oversight are part of the inherited transparency.

## Open questions

- **Reserve-vehicle structures used by other large stablecoin issuers** — does USDT (Tether) use an analogous structure? What about PayPal USD, USDP (Paxos), FDUSD? The wiki's seed sources do not cover them in Session 1; comparative ingest in a future session would substantively develop this concept page.
- **The non-government 2a-7 sub-class** (prime money market funds) holds corporate paper and is structurally different. Stablecoin issuers using prime MMFs (if any) would face a higher reserve-quality risk profile than government-only MMFs. None in the current wiki.

## Sources cited

- [[vendor-circle-transparency-page-2026-04]]
