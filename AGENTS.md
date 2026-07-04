# AGENTS.md

Instructions for AI agents — any model, any framework — consuming this
repository. Everything here is plain markdown and JSON/XML; no tooling is
required beyond reading files (web access improves freshness checks but is
optional).

## What this repository is

Customs knowledge bundles in [OKF v0.1](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md):
one directory per customs territory under `bundles/` (currently `bundles/us`).
Each bundle has two layers:

- **Concepts** — distilled topical markdown files. This is the knowledge
  layer; answer from here.
- **Sources** — one provenance stub per primary document under
  `bundles/<code>/sources/`, with the actual files (PDF/DOCX/XML/JSON) in
  `sources/files/`. This is the evidence layer; quote exact text from here.

This is a **read-only mirror** synced from a curated upstream. Do not propose
edits to bundle content here — they will be overwritten. Flag problems via
GitHub issues.

## Format rules you need

- Every concept file starts with YAML frontmatter: `type` (always present),
  `title`, `description`, `tags`, `timestamp`. Filter and route by these.
- `index.md` in each directory is its table of contents; `log.md` is the
  bundle's dated change history, newest first.
- **Link resolution:** markdown links beginning with `/` are
  **bundle-relative**, not repository-relative. Resolve them against the
  bundle root: `/entry/bonds.md` inside the US bundle means
  `bundles/us/entry/bonds.md`. (GitHub's web UI renders these links broken —
  that is expected; resolve them yourself.)
- Concepts end with a `# Citations` section pointing at source stubs; stubs
  link both the local file and the canonical public URL.

## Answering questions

1. **Navigate before searching.** Start at `bundles/us/index.md`, follow the
   section listings to the relevant concepts. Concepts are already
   synthesized and cross-linked; most questions are answered there.
2. **Cite what you used** — the concept plus the primary source behind it
   (from the concept's Citations section). Prefer citing official documents
   over the distillation when the stakes are high.
3. **Quote exact text from the evidence layer, not from memory.**
   - Regulations: `bundles/us/sources/files/ecfr-title-19.xml` — the complete
     19 CFR as nested `DIV` elements (`TYPE="PART"`, `TYPE="SECTION"`, with
     `N` attributes for numbers). Search for the section number rather than
     loading the whole ~11 MB file.
   - Tariff lines: `bundles/us/sources/files/hts-current.json` — every HTS
     line as objects with `htsno`, `description`, `general`, `special`,
     `other` (rate columns), `units`, `footnotes`. ~14 MB; filter by `htsno`
     prefix.
4. **For binding-ruling questions** (classification, valuation, origin),
   read `bundles/us/regulations/cross-rulings.md` first — it documents CBP's
   CROSS rulings JSON API, how to confirm a ruling is still good law (the
   revocation metadata is only populated on the *revoking* ruling — the
   concept explains the reverse lookup), and known search pitfalls.
5. **Time-check everything volatile.** Compare concept `timestamp`s and
   in-text "as of" dates to today; check `bundles/us/log.md` for the last
   refreshes and `bundles/us/sources/source-state.json` for exact source
   versions (eCFR point-in-time date, HTS release name). Much of the
   2025–2026 low-value entry regime is interim rulemaking with future
   effective dates. If you have web access, verify tariff rates, effective
   dates, and penalty amounts against the Federal Register, CBP CSMS,
   ecfr.gov, and hts.usitc.gov — and say which facts you live-verified. If
   you don't, state the as-of date of what you relied on.
6. **Don't oversell.** This corpus is curated but not exhaustive, and none of
   it is legal advice. When the bundle doesn't cover something, say so
   rather than extrapolating.

## Freshness signals (machine-readable)

| Signal | Where | Meaning |
|--------|-------|---------|
| `source-state.json` | `bundles/us/sources/` | Exact eCFR point-in-time date and HTS release currently on disk, with download timestamps |
| `**Point-in-time:**` / `**Current release:**` lines | eCFR and HTS source stubs | Human-readable version of the same |
| `log.md` | bundle root | Dated history of every content and source change |
| Sync commits | git history | This mirror syncs on every upstream change, including weekly automated source refreshes |
