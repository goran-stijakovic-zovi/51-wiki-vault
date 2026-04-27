# 51 Wiki — a digital-asset vendor research wiki

A Karpathy-style LLM Wiki demonstrating how a domain-specific research substrate can be built, ingested, and curated for the **digital-asset vendor research** domain. This vault is a **production template / example** that 51 Terminal (Fiftyone Group LLC) can study and fork for their own internal corpus.

**Pattern source**: Andrej Karpathy's LLM Wiki gist —
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

**Schema**: see [`CLAUDE.md`](CLAUDE.md) — the schema *is* the program.

**Scope** (Path A — public sources only):

- The Karpathy gist (meta-pattern).
- The public 51 Terminal April deck (audience framing only — no reproduction of product internals).
- Public vendor materials (Circle, Sky Protocol, BitGo / Fireblocks, Chainalysis — fetched from their public sites).
- Public regulator pages (EU MiCA, NYDFS BitLicense).

**Out of scope**: anything from `terminal.fiftyone.xyz`, anything Goran-authored about the audit (walkthrough, wiki plan, meeting brief), anything paywalled. See `CLAUDE.md` for the full Path A licensing posture.

## Layout

- `raw/` — immutable inputs (gist, deck, vendor / regulator pages).
- `wiki/` — LLM-curated entity pages (vendors, concepts, sectors, sources, people, firms).
- `index.md` — LLM-maintained catalog of every wiki page.
- `log.md` — append-only chronological journal of ingests, queries, lints.
- `_templates/` — entity-type page starters.
- `scripts/` — operational toolbox; currently just a `_README.md` (manual ingest, no fetcher yet).

## Operations

Three operations run against the vault, defined in `CLAUDE.md`:

- **Ingest** — raw input → entity pages. Always interactive: read → takeaways → "go" → write.
- **Query** — graph walk + cited answer.
- **Lint** — find drift, contradictions, orphans, stale claims, Path A leakage.

## Companion site

A public deploy of this vault lives (or will live) at
**https://51.zoviconsulting.com/** — see the deployment handover at
`/Users/gstijakovic/Dev/Projects/51/51-wiki-handover.md`.
