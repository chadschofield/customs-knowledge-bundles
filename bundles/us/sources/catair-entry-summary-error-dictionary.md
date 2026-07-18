---
type: Source Document
title: ACE Error Dictionary — Entry Summary (current: v51)
description: The entry summary condition-code dictionary (~1,000 codes with narrative text and explanations) — v51 (2026-07-17) current; v49 and the v50 draft retained for change-tracking.
resource: https://www.cbp.gov/document/guidance/ace-catair-error-dictionary
tags: [source, cbp, catair, abi, entry-summary, error-codes]
timestamp: 2026-07-18T20:10:00Z
---

**ACE Error Dictionary** (CBP lists it as "Error Dictionary: Entry Summary").
Roughly a thousand condition codes returned on entry summary (AE/AX) filings,
each with narrative text, an explanation, and its last-updated date. CBP
revises it frequently; the 2026 run of changes tracked through CSMS:

| Rev | Date | Added |
|-----|------|-------|
| v49 | 2026-06-25 | **876 – DUTY HTS REQUIRES NON-DUTY HTS** (Section 232 auto-parts line pairing) |
| v50 | deployed **2026-07-16** (CERT 06-30) | **F875 – IMPORTER INACTIVE FOR ENTRY PURPOSES** (CSMS # 69268077) |
| v51 | 2026-07-17; validations deploy **2026-07-18** | **F866 – AUTO LICENSE PRESENT – DUTY NOT ALLOWED** and **F861 – AUTO LICENSE INSUFFICIENT BALANCE** — the auto-parts offset-license enforcement (CSMS # 69271650) |

**Local files:**

- [files/catair-entry-summary-error-dictionary-v51-2026-07.xlsx](files/catair-entry-summary-error-dictionary-v51-2026-07.xlsx) — **current** (v51, 2026-07-17, fetched from cbp.gov 2026-07-18).
- [files/catair-entry-summary-error-dictionary-v49-2026-06.xlsx](files/catair-entry-summary-error-dictionary-v49-2026-06.xlsx) — prior edition, retained for diffing.
- The [v50 draft](catair-entry-summary-error-dictionary-v50-draft.md) is kept as its own stub.

**Distilled into:** [Entry Summary Filing (AE/AX)](/ace-filing/entry-summary-filing.md)
