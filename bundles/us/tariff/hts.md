---
type: Reference
title: Harmonized Tariff Schedule (HTS)
description: The US tariff nomenclature maintained by the USITC — structure, Chapter 98/99 special provisions, revision cadence, and machine-readable access; current edition 2026 Revision 11.
resource: https://hts.usitc.gov/
tags: [hts, htsus, classification, tariff, usitc]
timestamp: 2026-07-03T19:00:00Z
---

The **Harmonized Tariff Schedule of the United States (HTSUS)** sets the
classification and duty rates for everything imported into the US. It is
maintained and published by the **USITC** on the WCO's international
6-digit Harmonized System base, extended to **8-digit legal tariff lines and
10-digit statistical reporting numbers**. Since the
[de minimis suspension](/entry/de-minimis-suspension.md), a 10-digit
classification is required on effectively every shipment, of any value, in
every entry pathway.

The bundle's current edition is tracked in the [source stub](/sources/hts.md)
(**2026 Revision 11**, USITC Pub. 5758, at the time of writing — the stub is
auto-refreshed weekly), with both the official PDF and the machine-readable
JSON export kept **latest-only** under stable filenames in
[sources/files/](/sources/index.md) (prior editions: git history and the
USITC archive).

# Structure

| Piece | What it holds |
|-------|---------------|
| General Rules of Interpretation (GRIs 1–6) + Additional US Rules | The legal method for classifying goods. |
| General Notes | MFN relationships, FTA rules of origin and SPI codes, quota notes. |
| Chapters 1–97 | The substantive nomenclature (sections I–XXII). |
| **Chapter 98** | Special classification provisions — US goods returned (9801), repairs/alterations (9802), personal exemptions, government imports. |
| **Chapter 99** | Temporary legislation and trade-remedy modifications — Section 301/232/201 measures, exclusions, and emergency actions land here as 9903.xx.xx secondary classifications. |
| Rate columns | Column 1 **General** (MFN/NTR), Column 1 **Special** (preference programs), Column 2 (statutory — Cuba, North Korea). |

Entries during trade actions typically pair a **primary** Ch. 1–97 line with
**secondary** Ch. 99 line(s) — exactly the "primary and secondary
classifications" the [ET13](/entry/entry-type-13-test.md) and
[IMDW](/entry/postal-informal-entry-imdw.md) processes call for.

# Editions & Revision Cadence

The USITC publishes a **Basic edition** each year and **numbered revisions**
throughout the year (2026 is already at Revision 11 as of July) — driven by
Federal Register tariff actions, FTA staging, and statistical changes. Every
edition is archived at the
[HTS archive](https://hts.usitc.gov/download/archive). Watch Federal Register
notices and CBP CSMS messages for what changed; the
[current tariff-action context](/tariff/tariff-actions-2025-2026.md) makes
revisions unusually frequent.

**How changes reach ACE — Harmonized System Updates (HSUs).** CBP loads tariff
and ABI record changes into ACE as numbered **HSUs**, announced by CSMS
(2026 ran HSU 2607–2614 across April–July, carrying Section 232 metals, the
Section 301 Large Civil Aircraft lines, USDA agricultural license flags, the
Taiwan Section 232 modifications, and the Spring 2026 §484(f) statistical
update). HSUs are the ACE-side mirror of HTS revisions; the bundle's
`hts-current.json` weekly refresh absorbs the resulting record changes, so the
individual HSU notices are operational plumbing rather than separate knowledge.

# Machine-Readable Access (verified endpoints)

| Endpoint | Returns |
|----------|---------|
| `https://hts.usitc.gov/reststop/currentRelease` | JSON identifying the current edition, e.g. `{"name": "2026HTSRev11", "title": "Revision 11 (2026)"}` — the update-check signal. |
| `https://hts.usitc.gov/reststop/exportList?from=0101&to=9999&format=JSON&styles=false` | Full schedule export (also `format=CSV`); fields include `htsno`, `indent`, `description`, `units`, `general`, `special`, `other`, `footnotes`. |
| [hts.usitc.gov/download/archive](https://hts.usitc.gov/download/archive) | Per-edition PDF/Excel/CSV/JSON downloads, current and historical. |

`scripts/update_sources.py` at the repository root uses the first two to keep
[sources/files/hts-current.json](/sources/hts.md) on the current release. The export is a flat indented-outline structure: rate-bearing rows
carry 8/10-digit `htsno` values; parent headings provide description context
via `indent`.

# Citations

[1] [HTS current edition (2026 Rev 11, USITC Pub. 5758) — local source](/sources/hts.md)
[2] [USITC HTS site](https://hts.usitc.gov/)
