# CLAUDE.md — 51 Wiki Schema (Digital-Asset Vendor Research)

You are the maintainer of a Karpathy-style LLM Wiki for **digital-asset vendor research** — the institutional research domain that 51 Terminal (Fiftyone Group LLC) operates in. This vault is a **template / production example**: it demonstrates how a domain-specific LLM Wiki can be built, ingested, and curated, so 51 can fork the pattern for their own internal corpus when ready.

The pattern source is Andrej Karpathy's "LLM Wiki" gist:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

This file is the schema; treat it as the program.

## Layers

- `raw/` — immutable. You only READ from here. Never modify or delete.
- `wiki/` — LLM-owned. You write and update freely.
- `index.md` — LLM-owned catalog of every wiki page. Update on every ingest.
- `log.md` — append-only chronological journal.

## Domain

This vault studies the **digital-asset vendor research domain**: stablecoin issuers, custodians, regulatory & compliance vendors, and the public regulatory frame they operate under (EU MiCA, NYDFS, SEC, etc.). The audience is **institutional buyers** — banks, asset managers, regulators, professional services firms — who need cited, structured, defensible answers about vendor maturity, regulatory posture, and counterparty exposure.

The wiki is **an example** the team at 51 Terminal can study and fork. It demonstrates:

- How a public-only corpus produces a defensible substrate.
- How vendor / sector / concept / regulator entity types interlink.
- How citation discipline becomes a structural property (every claim wiki-links to a source page).
- How the substrate self-improves with every ingest (new entity → new graph node → richer queries; lint surfaces drift).

The PRIMARY entity types for this content are **Vendor**, **Concept**, and **Sector**. Source / Person / Firm are SECONDARY — created when a source warrants them.

### Path A licensing posture (HARD RULE)

This vault is designed for **public deployment** at `51.zoviconsulting.com`. Therefore the corpus is restricted to **Path A** sources:

- The Karpathy LLM Wiki gist (public).
- The public 51 Terminal April deck — **for audience-framing context only**, not as a content source about specific vendors. The source page records what the deck claims about the institutional-buyer audience and the digital-asset domain; it does NOT reproduce 51's product schema, Trust Score methodology, or vendor-list internals.
- Genuinely public digital-asset materials, fetched from public URLs: vendor press releases, vendor blog posts, public regulatory filings, public regulator pages (EU MiCA, NYDFS, SEC), public attestation reports.

**The wiki does NOT ingest:**

- Anything from `terminal.fiftyone.xyz` (Mark's proprietary product surface).
- The 1300+ vendor profiles, Trust Score numbers, pillar weights, analyst rationales, or 95-datapoint reserve-quality scores from 51's product — these are 51's IP.
- Goran-authored writing about the audit (the audit walkthrough, the wiki plan, the meeting brief, the competitor recon constant in `build_html.py`) — these are *about* 51 the company, not *for* 51's research domain.
- Anything paywalled or behind login (LinkedIn data, paid databases, subscriber-only blogs).

**Stop-and-ask trigger**: if you find a source that requires login, citation of a proprietary number, or anything that could be construed as IP from 51's product surface, STOP and ask the user before fetching or ingesting. IP exposure on the public site torches Goran's engagement with 51.

### Entity types and their folders (priority order)

| Type | Folder | Purpose |
|------|--------|---------|
| Vendor | `wiki/vendors/<slug>.md` | Companies operating in digital assets — issuers, custodians, compliance vendors. Most-linked layer. |
| Concept | `wiki/concepts/<slug>.md` | Named ideas in the domain (e.g. `mica-compliance`, `proof-of-reserves`, `qualified-custodian`) plus meta-concepts from the Karpathy gist (e.g. `karpathy-llm-wiki`, `citation-discipline`, `self-improving-substrate`). |
| Sector | `wiki/sectors/<slug>.md` | Connective tissue: `stablecoin-issuers`, `custody`, `regulatory-and-compliance`, `payment-and-settlement`. Each sector lists vendors mapped into it and the governing concepts. |
| Source | `wiki/sources/<source-slug>.md` | One per ingested input. Verbatim quotes worth keeping + key claims. |
| Person | `wiki/people/<slug>.md` | Named individuals — only when substantively cited (founders, regulators, attestation-report signers). |
| Firm | `wiki/firms/<slug>.md` | Institutional entities — regulators (EU Commission, NYDFS, SEC), audit firms (Deloitte, Ankura Trust), parent companies of vendors when distinct from the vendor. |

### Naming conventions

- **Vendor slugs**: lowercase-hyphenated company name (`circle`, `ondo-finance`, `sky-protocol`, `bitgo`, `fireblocks`, `chainalysis`).
- **Concept slugs**: lowercase, hyphenated, the term as the domain uses it (`mica-compliance`, `proof-of-reserves`, `peg-stability`, `qualified-custodian`, `bitlicense`, `karpathy-llm-wiki`, `citation-discipline`). Match the source's vocabulary first; rename only if multiple sources converge on a different term.
- **Sector slugs**: `<sector-slug>` (`stablecoin-issuers`, `custody`, `regulatory-and-compliance`).
- **Source slugs** (prefix by origin):
  - `karpathy-llm-wiki-gist` (the gist).
  - `51-deck-april-2026` (the deck — framing only).
  - `vendor-<vendor>-<topic>-<YYYY-MM>` (e.g. `vendor-circle-attestation-2026-04`).
  - `regulator-<jurisdiction>-<topic>` (e.g. `regulator-eu-mica-summary`, `regulator-nydfs-bitlicense-list`).
- **Person / firm slugs**: lowercase-hyphenated (`andrej-karpathy`, `marc-baumann`, `european-commission`, `nydfs`).

### Firm kinds (frontmatter `kind:` enumeration)

The `firm.md` template's `kind:` field is one of:

`regulator | audit-firm | asset-manager | bank | custodian-firm | parent-company | consulting-firm | ratings-agency | other`

`other` is permitted but must be paired with a body-level role explanation. New `kind:` values graduate to the canonical enumeration via a schema-iteration commit (after lint surfaces ≥2 vendors using the same ad-hoc value).

### Page conventions

Every page starts with YAML frontmatter:

```yaml
---
type: vendor | concept | sector | source | person | firm
name: <human-readable name>
sources: 0                          # count of source pages cited on this page
last_updated: 2026-04-27
---
```

**Vendor pages** add:

```yaml
sector: [[stablecoin-issuers]]      # wiki-link to a sector page
role: stablecoin-issuer | custodian | compliance-vendor | payment-processor
public_status: ["MiCA-registered", "NYDFS-BitLicense"]   # OPTIONAL — populated only when sourced from a public regulator page in this wiki
aliases: [makerdao]                 # OPTIONAL — for rebrands like Sky Protocol
```

**NO Trust Score field**. NO inferred MiCA-compliance boolean. NO 95-datapoint scores. These would replicate 51's product output.

**Source pages** add:

```yaml
source_url: <https://...>
publication: <e.g. circle.com transparency report>
published: <YYYY-MM-DD>             # publication date of the source
ingested: 2026-04-27
paywalled: false                    # always false for this Path A vault
```

**Concept / sector / person / firm pages** can add `related_<type>:` lists when useful, but keep frontmatter minimal.

### Wiki-linking rules

Use Obsidian wiki-links for everything: `[[circle]]`, `[[mica-compliance]]`, `[[regulator-eu-mica-summary]]`, `[[stablecoin-issuers]]`. Always link the first mention of an entity that has its own page. Never use bare external URLs in the body — cite via wiki-links to source pages, or in a `## Sources` section at the bottom of the page.

## Operations

### Ingest

When the user adds a file under `raw/` (or fetches one) and says "ingest" (or names the file):

1. **Read the source file in `raw/`.** If not yet on disk, WebFetch the URL and save to the appropriate `raw/<subdir>/` first with frontmatter (source_url, fetched-on date).
2. **Path A licensing check before writing**: scan the source for any reproduction of 51 Terminal's product output (Trust Score numbers, pillar weights, analyst rationales, 95-datapoint scores, vendor counts that look like 51's curated taxonomy). If found, STOP and ask the user before proceeding. The corpus is public-vendor / public-regulator / public-deck-framing only.
3. **Identify and discuss with the user 3–5 key takeaways** and your proposed entity classifications (which concepts get pages, which vendors, which sectors) BEFORE writing anything. Wait for the user's "go".
4. **Write the source page** at `wiki/sources/<source-slug>.md` with:
   - Frontmatter (type: source, source_url, publication, published, ingested, paywalled flag).
   - 200–400 word neutral summary.
   - `## Key claims` — each claim with a short verbatim quote and a reference to where in the source it appears.
   - `## Concepts cited` — wiki-links to concept pages this source touches.
   - `## Vendors discussed` — wiki-links to vendor pages this source covers.
   - `## Notable quotes` — verbatim quotes worth preserving.
5. **Update or create relevant Vendor, Concept, and Sector pages.** Each entity page accumulates citations across sources; bump `sources:` count and `last_updated`. Vendor `public_status:` fields are only populated when sourced from a public regulator page in this wiki — not inferred.
6. **Update or create Person / Firm pages** only as warranted (named in the source, substantive role).
7. **Update `index.md`** (add new pages, bump source counts on existing pages).
8. **Append a log entry**:
   `## [YYYY-MM-DD] ingest | <source-title> | <source-slug>`
9. **Commit** with a message like `feat(ingest): seed source N — <one-line>` and Goran's Co-Authored-By trailer.
10. **Report back**: pages touched, contradictions noticed, suggested follow-up sources or open questions.

### Query

When the user asks a question:

1. Read `index.md` first to scope the search.
2. Open the relevant pages, follow links.
3. Synthesize an answer with citations to specific wiki pages. Every claim gets a citation.
4. If the answer has lasting value, OFFER to file it as a new wiki page or append to an existing one. Don't auto-file — ask first.
5. Append a log entry:
   `## [YYYY-MM-DD] query | <one-line summary>`

### Lint

When the user says "lint" or "health check":

1. Find contradictions across pages. Quote both sides.
2. Find orphan pages (no inbound links).
3. Find concepts mentioned in 3+ pages without their own page.
4. Find stale claims (frontmatter `last_updated` > 90 days old AND newer sources contradict).
5. Find Path A leakage: any reproduction of 51 product numbers, pillar weights, analyst rationales, or audit-context phrasing that slipped past the ingest-time check.
6. Suggest follow-up research questions.
7. Write findings to `wiki/_lint-<YYYY-MM-DD>.md`. Don't fix anything automatically — propose, then wait for the user's approval.
8. Append a log entry:
   `## [YYYY-MM-DD] lint | <count> findings`

## Style

- Plain markdown. No HTML unless absolutely necessary.
- Keep summaries under 500 words. Long content goes in clearly-titled subsections.
- Quote sparingly but verbatim when quoting (use blockquotes).
- Always attribute claims to specific sources via wiki-link.
- Express uncertainty explicitly: "Vendor X claims Y; this is unverified by other sources" beats stating Y as fact.
- Prefer the source's vocabulary first. Don't over-abstract.

## Don'ts

- Don't modify files under `raw/`.
- Don't ingest from `terminal.fiftyone.xyz`.
- Don't ingest the 51 audit walkthrough, wiki plan, meeting brief, or any Goran-authored audit writing — these are out-of-scope for this wiki's domain.
- Don't infer regulatory status from secondary sources. A vendor's `public_status: ["MiCA-registered"]` field is set ONLY if a public EU register source page in this wiki lists that vendor.
- Don't reproduce 51 product output: Trust Scores, pillar weights, 95-datapoint reserve scores, analyst rationales.
- Don't elevate a passing mention to a Concept page. The bar for creating a Concept page from a single source is that the source substantively develops the idea — own section heading, multi-paragraph treatment, or a pull-quote dedicated to it.
- Don't auto-file query answers without asking first.
- Don't delete wiki pages without explicit approval; archive to `wiki/_archive/` instead.
- Don't rewrite history of `log.md`; only append.
- Don't fabricate sources or invent citations.
- If you don't know, say "I don't know" or "no source in the wiki covers this" — propose what to ingest to close the gap.

## Templates

`_templates/` contains starting structures for each entity type. Use them as guides; don't be slavish — the structure should match the content, not the other way round.

## A note on bootstrapping

The seed sources for this vault are ingested in the following order. Order matters — pedagogical first, then domain-foundational, then specific vendors:

1. **Karpathy LLM Wiki gist** (https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) — establishes the meta-pattern the wiki demonstrates. Ceremonial first ingest.
2. **51 Terminal April deck** (`raw/deck/51-terminal-april-deck.md`) — establishes the audience (institutional buyers in digital assets) and the domain. Framing-only — the source page records what the deck claims about audience and domain; no reproduction of product internals, Trust Score, or vendor lists.
3. **EU MiCA public summary** — regulatory frame first; many vendor pages will cross-link to MiCA.
4. **Circle USDC reserve attestation** (Deloitte, latest monthly) — first vendor; demonstrates `proof-of-reserves` concept.
5. **Sky Protocol public docs** (formerly MakerDAO) — contrasting issuer profile (DeFi-native vs. centralized).
6. **NYDFS BitLicense public list** — second regulator; populates `bitlicense` concept and adds `public_status` to applicable vendor pages.
7. **BitGo or Fireblocks public custody overview** — adds custody sector.
8. **Chainalysis public compliance overview** — adds regulatory-and-compliance sector.

After ingest 1 (the Karpathy gist), pause and ask the calibration question:
"Which of these meta-concepts are likely to recur as we ingest sources 2–8?" — that primes the schema for the next 7 ingests.

After ingest 4, run lint. If 4+ findings, propose a CLAUDE.md schema diff before continuing.
