---
type: Reference
title: 19 CFR — Customs Duties
description: Title 19 of the Code of Federal Regulations — structure, the parts that matter for parcel logistics, and the bundle's full-text XML copy refreshed from the eCFR API.
resource: https://www.ecfr.gov/current/title-19
tags: [regulations, cfr, ecfr, title-19]
timestamp: 2026-07-03T19:00:00Z
---

**Title 19 CFR ("Customs Duties")** contains the implementing regulations for
US customs law. The **eCFR** (ecfr.gov) is the continuously-updated,
unofficial-but-current compilation; the annual GPO edition is the official
one. This bundle carries a **full-text point-in-time XML copy** —
[sources/files/ecfr-title-19.xml](/sources/ecfr-title-19.md) — whose current
as-of date is tracked in the source stub (2026-07-01 at the time of writing,
covering the twin de minimis IFRs; auto-refreshed weekly).

# Structure

| Chapter | Agency | Parts |
|---------|--------|-------|
| I | CBP (DHS/Treasury) | 0–199 — the operational customs regulations |
| II | US International Trade Commission | 200–299 |
| III | International Trade Administration (Commerce) | 300–399 |
| IV | US Immigration and Customs Enforcement | 400–599 |

# Chapter I Parts That Matter for Parcel Logistics

| Part | Subject | Why it matters here |
|------|---------|---------------------|
| 10 | Articles conditionally free | § 10.151–10.153: de minimis & gift implementation — see [De Minimis Suspension](/entry/de-minimis-suspension.md) |
| 24 | Financial & accounting | Duty payment, statements, fees (MPF) |
| 101 | General provisions | § 101.9 test authority behind [ET13](/entry/entry-type-13-test.md) |
| 111 | Customs brokers | Licensing behind [Right to Make Entry](/entry/right-to-make-entry.md) |
| 113 | Bonds | §§ 113.62/113.63/113.64 — see [Customs Bonds](/entry/bonds.md) |
| 128 | Express consignments | Courier hub clearance |
| 141–142 | Entry of merchandise / entry process | Entry, release, § 141.68 time-of-entry |
| 143 | Special entry procedures (incl. ABI) | Subpart C informal entry; § 143.23(j)(3) manifest release (now unavailable for low-value) |
| 145 | **Mail importations** | § 145.12 formal-entry triggers, new § 145.15 bond, § 145.31 de minimis suspension — see [Postal Informal Entry](/entry/postal-informal-entry-imdw.md) |
| 146 | Foreign trade zones | FTZ operations |
| 152 | Classification & appraisement | [Customs Valuation](/valuation/customs-valuation.md) |
| 159 | Liquidation | Final duty determination |
| 163 | Recordkeeping | (a)(1)(A) list, 5-year retention |
| 165 | EAPA investigations | Evasion allegations |

# Local Copy & How to Refresh

There is no one-click "download all of Title 19" on ecfr.gov, but the
**eCFR Versioner API** serves the complete title as one XML document:

```
# metadata — has each title's up_to_date_as_of / latest_amended_on
https://www.ecfr.gov/api/versioner/v1/titles.json

# full point-in-time XML for Title 19 (~11 MB)
https://www.ecfr.gov/api/versioner/v1/full/{YYYY-MM-DD}/title-19.xml
```

`scripts/update_sources.py --download` (repository root; run weekly by the
`update-sources` GitHub Actions workflow) compares `up_to_date_as_of` against
`sources/source-state.json` and replaces `sources/files/ecfr-title-19.xml`
when the eCFR advances; git history keeps prior snapshots. Alternatives: GPO **govinfo bulk data**
([govinfo.gov/bulkdata/ECFR/title-19](https://www.govinfo.gov/bulkdata/ECFR/title-19),
same XML), or the official annual-edition PDFs per volume from govinfo for
legal-record purposes.

The XML uses `DIV1/DIV3/DIV5/DIV8`-style elements (title/chapter/part/section)
with `N` and `TYPE` attributes — grep-able and easily chunked by part for
retrieval.

# Citations

[1] [Local eCFR Title 19 XML source stub](/sources/ecfr-title-19.md)
[2] [eCFR Title 19 (live)](https://www.ecfr.gov/current/title-19)
[3] [eCFR developer API](https://www.ecfr.gov/developers/documentation/api/v1)
