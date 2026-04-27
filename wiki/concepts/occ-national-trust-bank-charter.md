---
type: concept
name: OCC national trust bank charter
sources: 1
last_updated: 2026-04-27
---

# OCC national trust bank charter

> *US federal regulatory path for trust banks: a national trust bank charter issued and supervised by the Office of the Comptroller of the Currency (OCC), part of the US Treasury. Distinct from state trust charters (e.g. [[limited-purpose-trust-charter|NYDFS Limited Purpose Trust Charter]]) — federal scope, federal supervision, broader bank-like regulatory perimeter.*

## What it means

The OCC national trust bank charter is the **federal-level** US regulatory authorisation for trust-banking activities. Holders of this charter are nationally-chartered banks that may exercise trust powers across all US states without separately seeking state-level authorisation in each. Their primary regulator is the **[[occ|Office of the Comptroller of the Currency]]**, which is part of the US Treasury and has supervisory authority over national banks.

For digital-asset custodians, the OCC trust bank charter has emerged as a distinct regulatory path alongside state-level trust charters. It is structurally significant for institutional-buyer diligence in three ways: **federal-level supervision** (a single primary regulator vs. patchwork state regulators), **multi-state operating scope** (a national charter authorizes activity across all 50 states by default), and **bank-like regulatory perimeter** (capital, liquidity, governance standards aligned with national banking norms rather than crypto-specific state regimes).

The wiki's first concrete example is [[bitgo]]'s **BitGo Bank & Trust, National Association** — federally chartered and regulated by the OCC per BitGo's homepage announcement.

## How it shows up in sources

- [[vendor-bitgo-homepage-2026-04]] — BitGo's homepage features the OCC charter approval as the announcement: "BitGo Secures OCC Approval to Convert to a Federally Chartered National Trust Bank." Footer disclosure: "BitGo Bank & Trust, National Association... is a national trust bank chartered and regulated by the Office of the Comptroller of the Currency (OCC)."

## Mechanism / how it works

**Issuing authority**: the **Office of the Comptroller of the Currency (OCC)** — a bureau of the US Treasury Department that charters, regulates, and supervises all national banks and federal savings associations. The OCC's authority derives from the National Bank Act of 1864 and subsequent amendments.

**Trust bank scope**: a national trust bank may exercise **trust powers** (fiduciary capacity for clients) at the federal level. This is structurally analogous to the [[limited-purpose-trust-charter|NYDFS Limited Purpose Trust Charter]] but federal in scope rather than state.

**Multi-state operations**: an OCC-chartered national trust bank may operate across all US states without separately obtaining each state's trust authorisation. This is one of the structural advantages over state-charter-only paths.

**Insurance posture**: an OCC trust bank charter does NOT automatically include FDIC deposit insurance. BitGo's homepage explicitly discloses: "Digital assets held in custody are not guaranteed by BitGo and are not subject to... FDIC or SIPC." Trust banks generally do not take traditional bank deposits and therefore do not carry deposit insurance — the regulatory perimeter is bank-like for trust / fiduciary purposes but distinct from full commercial banking.

**Distinction from full national banking**: an OCC national trust bank charter is narrower than a full national bank charter. Trust banks are limited to fiduciary and custody-related activities and typically do not offer commercial banking services (lending, deposit-taking, etc.).

**Implication for institutional-buyer diligence**: a vendor with an OCC national trust bank charter has cleared a federal regulatory bar that combines (a) capital and governance requirements, (b) supervisory examination cadence, (c) multi-state operating authority, and (d) the prestige of a federal banking regulator's seal. For SEC-registered investment advisers required to use a [[qualified-custodian]] under the Investment Advisers Act, OCC-chartered national trust banks are recognized as qualified custodians.

## Related concepts

- [[limited-purpose-trust-charter]] — state-level (NY) analogue. The two paths are not redundant — vendors may hold both (BitGo holds both for different subsidiaries) — but the federal charter is broader in scope and supervised by a single federal regulator rather than a single state regulator.
- [[bitlicense]] — different state-level US regulatory path; transactional-vendor-focused rather than fiduciary. BitGo's NY subsidiary uses the trust-charter rather than BitLicense path.
- [[qualified-custodian]] — OCC trust banks meet the federal qualified-custodian definition for SEC-registered investment-adviser clients.
- [[mica-compliance]] — EU regulatory analogue is the [[crypto-asset-service-provider|CASP]] custody-and-administration service category; structurally different mechanism (registration vs. chartering) but similar institutional-buyer screening role.
- [[counterparty-graph-research]] — OCC charter introduces the OCC as a federal regulator counterparty in vendor graphs.

## Related vendors / sectors

- [[custody]] — sector where this regulatory path is most relevant.
- [[bitgo]] — first wiki vendor with this charter; the wiki's canonical example.
- [[occ]] — the regulator firm.

## Open questions

- **Other digital-asset custodians with OCC national trust bank charters.** Anchorage Digital and Paxos National Trust have historically held OCC charters in this space; the wiki's current sources don't directly cover them. Future ingest territory.
- **Substantive comparison of capital and operational requirements** between an OCC national trust bank charter and state-level trust charters. Practical diligence comparison would benefit from a future ingest of regulator-side documentation specifying the requirements.
- **The relationship between OCC national trust bank charter status and SEC qualified-custodian rules.** The Investment Advisers Act has specific qualified-custodian requirements (Rule 206(4)-2); confirming that OCC trust bank charter satisfies them substantively requires ingest of SEC rule-side material. Open question on the [[qualified-custodian]] page.

## Sources cited

- [[vendor-bitgo-homepage-2026-04]]
