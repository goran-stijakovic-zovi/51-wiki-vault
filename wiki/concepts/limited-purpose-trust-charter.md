---
type: concept
name: Limited Purpose Trust Charter
sources: 1
last_updated: 2026-04-27
---

# Limited Purpose Trust Charter

> *Alternative New York regulatory path for digital-asset vendors. Issued by [[nydfs|NYDFS]] under New York Banking Law. Permits virtual-currency business activity AND money transmission AND fiduciary powers — the [[bitlicense|BitLicense]] permits only the first.*

## What it means

The Limited Purpose Trust Charter is a New York regulatory authorisation that allows the holder to engage in Virtual Currency Business Activity without a separate BitLicense, while also exercising fiduciary powers and conducting money transmission without a separate Money Transmitter License. It is the canonical regulatory path for **custody-focused vendors** in New York: BitGo New York Trust Company, Coinbase Custody Trust Company, and Gemini Trust Company all hold this charter.

For an institutional buyer screening custodians, the trust charter is structurally preferable to the BitLicense in two specific ways: **fiduciary-powers authorisation** matters because qualified-custodian status under federal advisor rules typically requires fiduciary capacity, and **bundled MTL** simplifies the regulatory stack relative to a BitLicense + separate Article 13-B MTL configuration.

## How it shows up in sources

- [[regulator-nydfs-bitlicense-page-2026-04]] — NYDFS's main page describes the charter as an alternative regulatory path with explicit advantages over the BitLicense regime.

## Mechanism / how it works

**Statutory authority** — issued under New York Banking Law (which authorises the chartering of limited-purpose trust companies generally; NYDFS approval is required for the specific virtual-currency activity scope).

**Two structural advantages over BitLicense (verbatim from NYDFS source):**

> "While these forms of authorization are similar in many respects, a New York state limited purpose trust company charter may provide some additional benefits. For example, a limited purpose trust company can exercise fiduciary powers, while a BitLicensee cannot."

> "A limited purpose trust company can engage in money transmission in New York without obtaining a separate New York money transmitter license."

**Approval path:**

> "A business that is chartered under the New York Banking Law (for example, a New York State limited purpose trust company or a New York State bank) can engage in Virtual Currency Business Activity without a BitLicense if it has received the Superintendent's approval to do so."

**Selected entities holding this charter** (per the NYDFS Regulated Entities list):

- Gemini Trust Company, LLC (since 2015-10) — exchange + custody.
- Coinbase Custody Trust Company, LLC (since 2018-10) — institutional custody arm of Coinbase.
- BitGo New York Trust Company, LLC (since 2021-03) — institutional custody.

The pattern: vendors whose primary product is custody choose the trust charter; vendors whose primary product is transactional / exchange / payment-rails (Coinbase parent, PayPal, Block, Circle) choose BitLicense + MTL.

## Related concepts

- [[bitlicense]] — alternative regulatory path. The two are similar in many respects but the trust charter's fiduciary-powers and MTL-bundled features make it structurally preferable for custody-focused vendors.
- [[occ-national-trust-bank-charter]] — federal-level US analogue. State trust charter (NY) and federal trust bank charter (OCC) are not redundant — vendors may hold both for different subsidiaries (e.g. [[bitgo]] holds NY trust + OCC trust bank). Federal charter has multi-state operating scope; state charter is NY-specific.
- [[qualified-custodian]] — federal regulatory status under SEC Custody Rule. State trust charter equivalence to qualified-custodian status is a structural question (NY trust charter is generally recognized but specific equivalence depends on Investment Advisers Act bank-definition application).
- [[counterparty-graph-research]] — vendors holding the trust charter typically have NYDFS as a named regulatory counterparty, often alongside other state and federal regulators (OCC for federally-chartered subsidiaries).
- [[mica-compliance]] — the EU functional analogue for custody is the [[crypto-asset-service-provider|CASP]] custody-and-administration service category under Title V; the regulatory mechanism is structurally different (registration under MiCA vs. chartering under NY Banking Law) but the buyer-screening implications are similar.

## Related vendors / sectors

- [[custody]] — sector where this regulatory path is most common.
- [[bitgo]] — BitGo New York Trust Company, LLC holds this charter since 2021-03, alongside the OCC federal charter for BitGo Bank & Trust, N.A.
- [[stablecoin-issuers]] — some issuers operate via subsidiary structures with trust charters (Gemini Dollar via Gemini Trust Company); the wiki's seed sources don't directly cover this path yet.

## Open questions

- **Scope of "fiduciary powers" under the charter.** Differentiating fiduciary-powers authorisation from non-fiduciary BitLicense activity is the structural distinction; the practical scope (what specific activities a fiduciary may undertake that a BitLicensee may not) is not detailed in the NYDFS overview source. Future ingest of NY Banking Law fiduciary-powers material would substantively develop this.
- **The qualified-custodian relationship.** SEC-registered investment advisers handling client assets must use a "qualified custodian" under federal advisor rules. The relationship between the New York trust charter and federal qualified-custodian status is structurally important for institutional-allocator clients diligencing the custody stack. Resolved by future qualified-custodian concept page from the upcoming custody-vendor ingest.

## Sources cited

- [[regulator-nydfs-bitlicense-page-2026-04]]
