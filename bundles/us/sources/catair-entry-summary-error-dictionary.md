---
type: Source Document
title: ACE Error Dictionary — Entry Summary (current: v54)
description: The entry summary condition-code dictionary (~1,000 codes with narrative text and explanations) — v54 (2026-09-22, Entry Type 13 errors) current; v49, the v50 draft, v51 and v52 retained for change-tracking.
resource: https://www.cbp.gov/document/guidance/ace-catair-error-dictionary
tags: [source, cbp, catair, abi, entry-summary, error-codes]
timestamp: 2026-09-28T21:00:00Z
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
| v52 | deployed CERT + PROD **2026-08-21** | **F883 – PSC NOT ALLOWED TO MODIFY IEEPA HTS** — blocks a PSC on an FTZ Entry Type 06 that modifies an IEEPA HTS (CSMS # 69635410) |
| v53 | deployed CERT + PROD **2026-08-26** | **F884 – EXEMPT HTS NOT ALLOWED FOR SECTION 338** — the 9903.03.15 carve-out without a dutiable Section 338 Ch. 99 HTS on the line (CSMS # 69915227, corrected by # 69941677 — the first notice misprinted the HTS as 9903.03.05) |
| v54 | posted **2026-09-22** (drafted 07-24 → 09-01) | **Entry Type 13** errors: 878–882 manifest component type/issuer/ID, 867/868 Final Delivered To Party, 877 zip code unknown, **885 dutiable mail fee only for MOT 50**; B49 renamed "PSC NOT ALLOWED – CANNOT BE INFORMAL/MAIL" (ET 11/12/13); eleven existing errors revised for ET13 (CSMS # 69915001) |

**Local files:**

- [files/catair-entry-summary-error-dictionary-v54-2026-09.xlsx](files/catair-entry-summary-error-dictionary-v54-2026-09.xlsx) — **current** (v54, 1,077 codes, posted 2026-09-22, fetched from cbp.gov 2026-09-28). No separate v53 file was archived; v54 includes F884.
- [files/catair-entry-summary-error-dictionary-v52-2026-08.xlsx](files/catair-entry-summary-error-dictionary-v52-2026-08.xlsx) — prior edition (v52, deployed 2026-08-21), retained for diffing.
- [files/catair-entry-summary-error-dictionary-v51-2026-07.xlsx](files/catair-entry-summary-error-dictionary-v51-2026-07.xlsx) — prior edition (v51, 2026-07-17), retained for diffing.
- [files/catair-entry-summary-error-dictionary-v49-2026-06.xlsx](files/catair-entry-summary-error-dictionary-v49-2026-06.xlsx) — prior edition, retained for diffing.
- The [v50 draft](catair-entry-summary-error-dictionary-v50-draft.md) is kept as its own stub.

Pending at the time of writing: **886 – HTS PROHIBITED FOR CO**, announced for the 2026-09-29 Canada import exclusion (CSMS # 70050970) and not yet in v54.

**Distilled into:** [Entry Summary Filing (AE/AX)](/ace-filing/entry-summary-filing.md), [Entry Type 13 Test](/entry/entry-type-13-test.md)
