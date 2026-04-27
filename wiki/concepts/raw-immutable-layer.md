---
type: concept
name: Raw immutable layer
sources: 1
last_updated: 2026-04-27
---

# Raw immutable layer

> *The first layer of the [[karpathy-llm-wiki]]: a curated collection of source documents the LLM only reads from, never modifies.*

## What it means

The `raw/` directory holds the original source material — articles, gists, papers, transcripts, vendor pages, regulator pages, attestation reports — exactly as fetched. The LLM treats this as the source of truth: it reads from raw to ingest, but never edits or deletes raw files. Provenance and reproducibility flow from this discipline. If the curated wiki layer drifts, raw is the anchor that lets a re-ingest re-derive the synthesis cleanly.

## How it shows up in sources

- [[karpathy-llm-wiki-gist]] — > "Raw sources — your curated collection of source documents… These are immutable — the LLM reads from them but never modifies them. This is your source of truth."

## Mechanism / how it works

The immutability rule is enforced by convention rather than by file-system permissions: the schema file (`CLAUDE.md`) instructs the LLM that `raw/` is read-only, and the LLM honors the rule. Operationally, raw files carry minimal frontmatter (source URL, fetched date) and the original body unmodified. When a source needs sanitization (e.g. removing IP-sensitive sections under a Path A licensing posture), the sanitization happens at *write-to-raw* time and is documented in a banner at the top of the raw file — never as an edit-in-place after the fact.

Raw files in this vault are organized by source type:

- `raw/gist/` — Karpathy's gist (and any future patten-source gists).
- `raw/deck/` — the public 51 Terminal April deck (framing-only).
- `raw/vendors/` — public vendor materials (Circle, Sky, BitGo / Fireblocks, Chainalysis).
- `raw/regulators/` — public regulator pages (EU MiCA, NYDFS BitLicense).

## Related concepts

- [[wiki-curated-layer]] — the LLM-owned layer that reads from raw and produces interlinked entity pages.
- [[schema-as-program]] — defines the immutability rule.
- [[karpathy-llm-wiki]] — the parent pattern.

## Related vendors / sectors

_(pre-domain)_

## Open questions

- How are sanitized raw files (e.g. public-safe extracts of mixed-IP source documents) handled across the chain — is the sanitization documented in a banner header, or in a parallel `raw/<original>.banner.md`? (This vault uses banner headers.)

## Sources cited

- [[karpathy-llm-wiki-gist]]
