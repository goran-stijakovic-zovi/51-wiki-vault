---
source_url: https://sky.money
publication: Skybase / Sky Protocol
author: Skybase International (interface operator); Sky Protocol governance (smart contracts)
fetched: 2026-04-27
note: Sky.money is the public landing page for the Sky Protocol stablecoin ecosystem. Interface operated by Skybase International. Path A safe — fully public; no IP concerns. Substantive limitation: the landing page is mostly product navigation + governance disclaimers; technical architecture details are in the developer portal and chainlog (which were not successfully fetched in this ingest — see open questions).
---

# Sky Protocol: Content Extraction from Sky.money

## What Sky Protocol Is

**Mission & Positioning:**
The page presents Sky.money as "a non-custodial interface operated by Skybase, an independent Sky Agent with no control over Sky Protocol smart contracts or ecosystem governance."

The core value proposition is stated as: *"Put your stablecoins to work through Sky.money"* with access to *"market-leading returns on stablecoins through a suite of savings tools from Sky Protocol."*

**Primary Products Offered:**

1. **sUSDS** — described as *"The world's largest yield-generating stablecoin"* where *"Maximize your dollars with the Sky Savings Rate. Governed by Sky Ecosystem to deliver the best risk-adjusted yield, sUSDS allows you to grow your holdings with instant liquidity and zero fees."*

2. **stUSDS** — positioned as *"High-performance risk capital"* for *"expert users"* that *"provides the essential liquidity that powers SKY-backed borrowing in exchange for accelerated returns."*

3. **Sky Vaults** — described as *"Diversified stablecoin strategies"* that *"Deploy your USDS, USDC and USDT into a range of high-performance vault strategies designed to capture the best yields across the market."*

4. **SKY Token** — the governance layer, described as: *"SKY is a decentralized governance token of Sky Protocol. It is not a security, investment contract, or financial instrument."*

---

## Technical Architecture

**Governance Structure:**
The protocol uses decentralized governance via SKY tokenholders. The critical disclaimer states: *"The Sky Savings Rate and all other protocol parameters are determined through decentralized governance by SKY tokenholders and are subject to change or elimination at any time."*

SKY staking is offered: *"you can access SKY, stake it to earn rewards for governance participation, and borrow USDS against your staked SKY for more liquidity."*

**No Named "Stars" or Sub-DAO Structure:**
The page does not describe an explicit "Stars" structure or sub-DAOs. It mentions *"Sky Agents"* and *"Sky Ecosystem partners"* but does not define their formal governance role.

**Collateral & Backing:**
The page references *"SKY-backed lending"* for stUSDS yield generation and *"SKY-backed borrowing."* However, **the page does not explicitly detail what backs USDS** in terms of on-chain reserves, off-chain collateral, or hybrid models. This information is deferred to linked documentation.

---

## History / Rebrand

**No mention of MakerDAO or prior protocol name.** The page contains no historical narrative about Sky Protocol's origins or any rebrand event.

---

## Reserve / Collateral Approach

The page provides **no explicit breakdown** of what backs USDS. References exist to:
- *"Sky Savings Rate, which is backed by the Sky Agent Network"*
- *"SKY-backed lending within Sky Protocol"*

But specific collateral composition (on-chain vs. off-chain, percentages, asset types) is not detailed here. Users are directed to linked pages: *"View more details [here](/susds)"* and *"View more details [here](/stusds)."*

---

## Regulatory Positioning

**The page contains no explicit mention of:**
- MiCA (Markets in Crypto-Assets Regulation)
- NYDFS (New York Department of Financial Services)
- SEC (Securities and Exchange Commission)
- Any other regulatory framework

**Geographic Restriction:**
Two products display: *"Currently unavailable in the US"* — sUSDS, stUSDS, and Sky Ecosystem Rewards. This suggests compliance measures but without stated legal basis.

---

## Trust & Transparency Claims (Verbatim Wording)

**Core Disclaimers on Control:**

> "Sky.money does not control, set, or guarantee the rate."

(Repeated for sUSDS, stUSDS, and vault yields.)

> "Skybase does not set, control, or guarantee any rates displayed on this interface."

**Independence:**

> "Sky.money is a non-custodial interface operated by Skybase, an independent Sky Agent with no control over Sky Protocol smart contracts or ecosystem governance."

> "Skybase International does not guarantee any level of yield, return, or protocol performance."

**Governance Autonomy:**

> "Skybase does not participate in, and has no ability to control or guarantee outcomes of, decentralized governance processes."

**Limited Liability on Forward-Looking Statements:**

> "Actual results could differ materially due to market volatility, regulatory changes, and decisions made through decentralized governance that are outside Skybase's control."

---

## Related Sky Protocol Resources

**Provided Links:**

- **App:** https://app.sky.money
- **Developer Portal:** https://developers.skyeco.com/
- **Github:** https://github.com/sky-ecosystem
- **Governance Voting:** https://vote.sky.money/
- **Community Forum:** https://forum.sky.money/ and https://forum.skyeco.com/
- **Discord:** https://discord.com/invite/skyecosystem
- **Sky Ecosystem (Main):** https://skyeco.com
- **Legal Docs:** https://docs.sky.money/legal/skybase-international/
- **Chainlog (canonical contract registry):** https://chainlog.sky.money/
- **Info Dashboard:** https://info.sky.money (redirects to https://info.skyeco.com/)

---

## Critical Gaps in This Source

This landing page **does not contain**:
- Technical architecture diagrams or smart contract details
- Collateral reserve audits or transparency dashboards
- Detailed history or rebranding narrative
- Explicit regulatory compliance statements
- Sub-DAO or "Stars" governance structure (if it exists)

**Substantive detail on these topics must be sourced from linked documentation**, particularly the developer portal and governance forum.

## Ingest-time fetching notes (added 2026-04-27)

During ingest, attempted to fetch additional substantive sources to fill the architectural gaps:
- `https://docs.sky.money` returned **HTTP 403** (Forbidden).
- `https://endgame.makerdao.com` returned **ECONNREFUSED** (host unreachable).
- `https://developers.skyeco.com` returned navigation-only content (no substantive technical detail in the homepage).
- `https://info.skyeco.com/` is JavaScript-rendered and returned empty shell to the fetcher.

The wiki therefore characterizes Sky Protocol from the landing page only, with substantive technical detail flagged as open questions for a follow-up source ingest in a future session.
