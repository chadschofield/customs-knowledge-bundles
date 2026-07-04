# Customs Knowledge Bundles

Open, agent-readable customs knowledge for cross-border logistics, packaged as
[Open Knowledge Format (OKF)](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md)
bundles — one per customs territory. Each bundle is plain markdown: distilled
topical **concepts** cross-linked over the **primary source documents**
(Federal Register documents, CBP publications and CATAIR specifications, the
Harmonized Tariff Schedule, the full text of 19 CFR) included in the bundle.

This repository is a **read-only mirror**, synced automatically from a
curated upstream. Edits made here will be overwritten by the next sync —
report corrections or gaps via GitHub issues instead.

## Bundles

| Bundle | Territory | Status | Freshness |
|--------|-----------|--------|-----------|
| [bundles/us](bundles/us/index.md) | United States (CBP) | Active | See [log.md](bundles/us/log.md) and [source-state.json](bundles/us/sources/source-state.json) |
| bundles/eu | European Union | Planned | — |

## Start here

- **People:** open [bundles/us/index.md](bundles/us/index.md) and follow the
  links — no tooling required.
- **AI agents (any model or framework):** read [AGENTS.md](AGENTS.md) for
  navigation, citation, and freshness rules. (`CLAUDE.md` just points there.)

## What's inside

```
bundles/us/
├── index.md        # Table of contents — the entry point
├── log.md          # Dated change history, newest first
├── overview.md     # Orientation to the US import system
├── entry/          # Entry pathways, de minimis suspension, postal (IMDW/ET13), bonds
├── ace-filing/     # ABI/CATAIR technical filing layer, PGA message set, CPSC eFiling
├── tariff/         # HTS classification, 2025–2026 tariff actions
├── valuation/      # Customs valuation (19 U.S.C. 1401a)
├── enforcement/    # EO 14411: IOR restrictions, penalties
├── regulations/    # 19 CFR full text, CROSS rulings
└── sources/        # One provenance stub per source; binaries in sources/files/
```

Notable machine-readable assets in `bundles/us/sources/files/`:
`ecfr-title-19.xml` (complete 19 CFR, point-in-time) and `hts-current.json`
(the full Harmonized Tariff Schedule, current edition).

## Freshness

The upstream refreshes the eCFR Title 19 XML and the HTS JSON export weekly
against their official APIs and syncs here on every change; the HTS official
PDF is swapped manually per revision and may briefly lag the JSON (the
[HTS source stub](bundles/us/sources/hts.md) flags when a swap is pending).
Every concept carries a `timestamp` and states "as of" dates for volatile
facts; much of the 2025–2026 low-value entry material is interim rulemaking
that changes quickly.

## Provenance and licensing

- **US government documents** (Federal Register, CBP publications, USITC HTS,
  eCFR) are works of the US federal government — public domain.
- **Everything else** (concept files, source stubs, BoxC-authored documents)
  is © BoxC, provided for reference.
- Nothing in this repository is legal advice. Verify time-sensitive facts
  against the Federal Register, CBP CSMS, ecfr.gov, and hts.usitc.gov before
  relying on them.
