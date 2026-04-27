# scripts/

Helper scripts for the vault. Not part of the Karpathy LLM Wiki pattern itself — this folder is your operational toolbox.

## Current state — manual ingest

The seed sources for this vault arrive via:

- **WebFetch during Phase 7 ingests** (from Claude Code) — Karpathy gist, EU MiCA public summary, NYDFS BitLicense list, Circle / Sky / BitGo or Fireblocks / Chainalysis public pages.
- **One local copy** — the public 51 Terminal April deck, copied from `/Users/gstijakovic/Dev/Projects/51/51-Terminal-April.md` into `raw/deck/`.

No fetcher script is needed for the demo. The wiki ingests are interactive: read raw → discuss takeaways → "go" → write entity pages.

## When to add a fetcher

Add a fetcher here if/when the corpus expands to a Tier-3 source set with regular cadence:

- Vendor RSS feeds (announcements, blog posts).
- Regulator update streams (EU register changes, NYDFS publication feed).
- Public attestation-report PDFs in bulk (e.g. monthly Circle / Tether attestations).
- Conference talk transcripts, podcast episodes.

**Reference template**: the canonical fetcher in the Trading-research vault is at
`/Users/gstijakovic/Dev/Projects/Trading-research/Obsidian-vault/Trading-research-vault/scripts/fetch_starters.py`.
It's Substack-tuned (parses JSON-LD + og: meta + `.markup` div), but the structure is reusable:

- Idempotent (skip already-fetched URLs).
- Emits YAML frontmatter (source_url, title, author, published, ingested, sha256, paywalled flag).
- Outputs one markdown file per URL into `raw/<subdir>/<slug>.md`.

For non-Substack sources, you'll need a rewritten parser per source type (vendor HTML, regulator HTML, PDF extraction).

## One-time setup (when a fetcher is added later)

```bash
cd /Users/gstijakovic/Dev/Projects/51-wiki/Obsidian-vault/51-wiki-vault
python3 -m venv .venv
source .venv/bin/activate
pip install requests beautifulsoup4 markdownify
# pip install pdfminer.six       # add if PDF parsing is needed
```

## After fetching

Open Claude Code in the vault root. Use the ingest protocol from `CLAUDE.md` (read raw → takeaways → "go" → write entity pages → update index + log → commit). Recommended ingest order is in `CLAUDE.md`'s "A note on bootstrapping" section.
