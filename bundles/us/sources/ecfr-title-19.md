---
type: Source Document
title: eCFR Title 19 — Customs Duties (full text XML)
description: Complete point-in-time XML of 19 CFR from the eCFR Versioner API, auto-refreshed weekly — the Point-in-time line below and source-state.json carry the current as-of date.
resource: https://www.ecfr.gov/current/title-19
tags: [source, regulations, ecfr, title-19, auto-refreshed]
timestamp: 2026-08-31T23:52:42Z
---

Complete Title 19 ("Customs Duties") as one XML document from the eCFR
Versioner API (`https://www.ecfr.gov/api/versioner/v1/full/{date}/title-19.xml`).

**Point-in-time:** 2026-08-28 (latest amendment 2026-08-26; downloaded 2026-08-31)

The line above, the frontmatter timestamp, [source-state.json](source-state.json),
and the [bundle log](/log.md) are maintained by `scripts/update_sources.py`
(run weekly by the `update-sources` GitHub Actions workflow).

- **Size:** ~11 MB; structure: nested `DIV` elements (`TYPE` =
  TITLE/CHAPTER/PART/SUBPART/SECTION, `N` = number) — grep-able, easily
  chunked by part.
- **Stable filename** — prior snapshots live in git history.
- The eCFR is the continuously-updated unofficial compilation; for the
  official legal record use the annual GPO edition
  ([govinfo bulk data](https://www.govinfo.gov/bulkdata/ECFR/title-19)
  mirrors the same XML).

**Local file:** [files/ecfr-title-19.xml](files/ecfr-title-19.xml)

**Distilled into:** [19 CFR — Customs Duties](/regulations/cfr-title-19.md)
