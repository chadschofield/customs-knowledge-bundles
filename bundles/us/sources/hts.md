---
type: Source Document
title: Harmonized Tariff Schedule — current edition
description: The current HTS edition, kept latest-only under stable filenames and auto-refreshed weekly — the Current release and Current PDF lines below, with source-state.json, name the edition.
resource: https://hts.usitc.gov/
tags: [source, hts, tariff, usitc, auto-refreshed]
timestamp: 2026-08-03T14:23:05Z
---

**Current release:** 2026HTSRev14 — Revision 14 (2026); 35,789 records; downloaded 2026-08-03
**Current PDF:** Revision 14 (2026) — USITC Publication 5772; 18,768,585 bytes; downloaded 2026-08-03

The two lines above, the frontmatter timestamp, [source-state.json](source-state.json),
and the [bundle log](/log.md) are maintained by `scripts/update_sources.py`
(run weekly by the `update-sources` GitHub Actions workflow), which watches
`https://hts.usitc.gov/reststop/currentRelease`.

Policy: this bundle keeps **only the latest edition** under stable filenames —
prior versions live in git history and in the
[USITC archive](https://hts.usitc.gov/download/archive).

**Local files:**

- [files/hts-current.json](files/hts-current.json) — full-schedule JSON export
  (`reststop/exportList?from=0101&to=9999&format=JSON&styles=false`),
  **auto-refreshed** on release change; fields: `htsno`, `indent`,
  `description`, `units`, `general`, `special`, `other`, `footnotes`,
  `quotaQuantity`, `additionalDuties`.
- [files/hts-current.pdf](files/hts-current.pdf) — official full PDF (GRIs,
  General Notes, chapters 1–99, statistical annexes), **auto-refreshed**
  alongside the JSON on release change from the "Download Full Revision"
  endpoint (`reststop/file?release=currentRelease&filename=finalCopy`, the
  button on [hts.usitc.gov/download](https://hts.usitc.gov/download)). The
  publication number in the Current PDF line above is read off the PDF's own
  cover page; if that line lags the Current release line, the automated fetch
  failed and the swap is pending manually.

**Distilled into:** [Harmonized Tariff Schedule](/tariff/hts.md)
