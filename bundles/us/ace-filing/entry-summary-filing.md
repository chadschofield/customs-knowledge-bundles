---
type: Process
title: Entry Summary Filing (AE/AX)
description: The technical side of filing CBP Form 7501 data — AE/AX record formats (rev 111 current, with Entry Type 13 and FY27 user fees), UC status notifications, the error dictionary, and census warning overrides.
tags: [entry-summary, ae, ax, abi, catair, 7501, process]
timestamp: 2026-09-28T21:00:00Z
---

The **Entry Summary Create/Update (AE/AX)** CATAIR chapter defines the record
formats for transmitting entry summary data (CBP Form 7501) to ACE — the
technical layer beneath [Entry Summary in ACE](/entry/entry-summary-ace.md),
which covers the business process. Input structure maps, the ES line and PGA
groupings, party/transportation reporting, and per-entry-type usage notes all
live in this one 246-page chapter.

# Which Version Is in Force — rev 111

The current-capabilities chapter at the time of writing is the **September
2026 edition, [Revision 111](/sources/catair-entry-summary-ae-ax-rev-111.md)**
(posted 2026-09-24, 254 pages). It rolls up three revisions since
[rev 108](/sources/catair-entry-summary-ae-ax-rev-108.md):

- **Rev 109** — the aluminum/steel US-territory bar and the **copper IAD 12**
  record, in production since 2026-07-16 and 2026-07-30. Its Global Business
  Identifier (GBI) changes (four repeats; SE31/SE51 identifier widened from
  20 to 35 characters) still await a CSMS production date. The
  [2025-11 rev 109 edition](/sources/catair-entry-summary-ae-ax-rev-109.md)
  is kept for diffing.
- **Rev 110** — **FY27 user fees**, effective for importations from
  **2026-10-01** (91 FR 48398): formal MPF **$34.58–$670.86**, informal MPF
  (automated) **$2.77**, **Dutiable Mail Fee $7.61**, manual surcharge $4.15
  (up from $33.58–$651.50, $2.69, $7.39 and $4.03 in FY26). A summary
  pre-filed before 10-01 takes the new amounts if its entry date is 10-01 or
  later (CSMS # 69915041).
- **Rev 111** — **Entry Type 13 (Informal – Mail)**: the Final Delivered To
  Party groupings, SFP issuer code, and "M" manifest component type. See
  [Entry Type 13 Test](/entry/entry-type-13-test.md); CBP scheduled it for
  production on 2026-09-22.

# Recent Changes That Matter for Parcel/Tariff Work

- **Rev 108** added Importer's Additional Declaration Type Code 11 (**Auto
  Parts Offset License**) — conditionally required on applicable auto-parts
  HTS lines; see [Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md)
  for the Section 232 context. Deployed to production 2025-09-11 per the
  chapter's change table. From **2026-07-18** the license is actively
  validated (errors F866/F861 below).
- **Copper smelt & cast reporting** (Proclamation 11021, CSMS # 69252300):
  effective **2026-07-30** (CERT 2026-07-16), entry summary lines for copper
  articles under HTS **8544.42.10 / .20 / .90 and 8544.49.10** (insulated
  wire and cable) from all non-US origins must report the **primary country
  of smelt and country of cast** (secondary smelt optional; **"OTH"**
  permitted when unknown). From **2026-09-14** the requirement is enforced:
  ACE rejects summaries missing the copper 54 record type 12 with a fatal
  **F794 – ADDTNL DEC TYPE RQRD FOR ARTICLE** (CSMS # 69711865).
- **Order of reporting multiple HTS on one line** (CSMS # 69668138,
  2026-08-27, updating # 69606660): when Chapter 98/99 classifications apply,
  report in sequence — Ch. 98 → Ch. 99 additional-duty headings (trade
  remedies in the order **Section 301 → Section 338 → Section 232 →
  Section 201 duties → Section 201 quota**) → Ch. 99 replacement-duty/MTB
  headings → other quota → the Ch. 1–97 classification. Entered value is
  reported on the Ch. 1–97 line unless Chapter 98 provisions direct
  otherwise. The Section 338 slot is new with the
  [Canada action](/tariff/tariff-actions-2025-2026.md).
- **Canada import exclusion** (from **2026-09-29**, CSMS # 70050970):
  summaries carrying [excluded Canadian products](/sources/csms-canada-import-exclusions.md)
  reject with **886 – HTS PROHIBITED FOR CO**. The same codes also reject at
  cargo release (335) and FTZ admission (239) — see
  [Cargo Release Filing](/ace-filing/cargo-release.md).
- **Section 301 China exclusions re-mapped** (91 FR 56538, CSMS # 69990649):
  four 9903.88.69 exclusions (U.S. notes 20(vvv)(i)(4)–(6) and (iv)(4)) now
  name the post-2026-07-01 statistical lines 8413.91.9039/9046/9059/9099
  and 3926.90.9915/9920. ACE accepts them from **2026-09-23 noon**. For
  entries 07-01 → 09-22 that paid Section 301 China duties, file a **PSC on
  or after 09-23** to get the refund (protest if the PSC window has closed).
- **Rev 106–107** (2025) carried the FY26 customs user-fee adjustments and
  Global Business Identifier "Test" renaming.

# Responses and Warnings

- **[Entry Summary Status Notification (UC), v30](/sources/catair-entry-summary-status-notification-uc.md)**
  (2025-06) — the unsolicited output messages ACE sends as processing
  conditions change (additional information required, rejections, CBP review
  statuses). Filers need to consume these, not just the synchronous AX
  response.
- **[ACE Error Dictionary — Entry Summary, v54 current](/sources/catair-entry-summary-error-dictionary.md)**
  (posted 2026-09-22) — ~1,000 condition codes with explanations;
  what a reject actually means. Recent additions tracked through CSMS: **864 – PSC NOT
  ALLOWED – REFUND REQUESTED** (V44, blocks a PSC while an
  [IEEPA/CAPE refund](/tariff/ieepa-refunds-cape.md) is in process);
  **F865 – HTS NOT ALLOWED FOR IMPORTER** (V46); **F60D – LIC/CERT/PERM FOR
  HTS MISSING** (V48, USDA agricultural license type 14 on sugar/dairy quota
  HTS); **876** (V49, Section 232 auto-parts duty HTS filed without its
  paired non-duty HTS — the reject behind the rev 108 declaration code above);
  **F875 – IMPORTER INACTIVE FOR ENTRY PURPOSES** (v50, **live in production
  since 2026-07-16**), the entry-summary counterpart of
  [cargo release reject 333](/ace-filing/cargo-release.md) (both enforce the
  [EO 14411 IOR deactivation](/entry/right-to-make-entry.md)); **F866 /
  F861** (v51, enforced from **2026-07-18**) — the auto-parts offset-license
  validations (license present → the paired Ch. 99 duty must be zero; the
  license balance must cover the claimed offset); and **F883 – PSC NOT
  ALLOWED TO MODIFY IEEPA HTS** (v52, deployed to CERT and PROD
  **2026-08-21**; CSMS # 69635410) — blocks a PSC on an FTZ Entry Type 06
  that modifies an IEEPA HTS in any way, companion plumbing to error 864 in
  the [IEEPA/CAPE refund](/tariff/ieepa-refunds-cape.md) machinery;
  **F884 – EXEMPT HTS NOT ALLOWED FOR SECTION 338** (v53, CERT and PROD
  **2026-08-26**; CSMS # 69915227 as corrected by # 69941677) — rejects the
  9903.03.15 carve-out on a line without a dutiable
  [Section 338](/tariff/tariff-actions-2025-2026.md) Ch. 99 HTS; and the
  **v54** Entry Type 13 set (878–882, 867/868, 877, 885, B49 renamed —
  CSMS # 69915001), detailed in [Entry Type 13 Test](/entry/entry-type-13-test.md).
- **Entry Summary Query (v26)** returns **Liquidation Reason Code 36 ("CAPE")**
  on entries refunded through the [CAPE tool](/tariff/ieepa-refunds-cape.md).
- **[Appendix H — Census Warning Messages and Override Codes](/sources/catair-appendix-h-census-overrides.md)**
  (2008 edition, still posted) — trade-statistics validations fire warnings
  that must be resolved or overridden with the codes listed there.

# Related Filing Machinery

Duty payment for accepted summaries runs through
[statements](/ace-filing/statements-duty-payment.md); Entry Type 09
reconciliation through the [RE filing](/ace-filing/reconciliation.md); entry
number construction and duty computation formulas are in the
[reference appendices](/ace-filing/catair-reference-appendices.md).

# Citations

[1] [Entry Summary Create/Update (AE/AX), rev 108 (superseded)](/sources/catair-entry-summary-ae-ax-rev-108.md)
[2] [Entry Summary Create/Update (AE/AX), rev 109 — 2025-11 edition (superseded)](/sources/catair-entry-summary-ae-ax-rev-109.md)
[3] [Entry Summary Status Notification (UC), v30](/sources/catair-entry-summary-status-notification-uc.md)
[4] [Appendix H — Census Warning Override Codes](/sources/catair-appendix-h-census-overrides.md)
[5] [ACE Error Dictionary — Entry Summary, v54 current](/sources/catair-entry-summary-error-dictionary.md)
[6] [ACE Error Dictionary — Entry Summary, v50 draft (superseded)](/sources/catair-entry-summary-error-dictionary-v50-draft.md)
[7] [CSMS # 69268077 — F875 deployed to production 2026-07-16](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/420f26d)
[8] [CSMS # 69271650 — F866/F861 offset-license validations, 2026-07-18](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41e30a7)
[9] [CSMS # 69252300 — copper smelt & cast reporting, effective 2026-07-30](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/420b4cc)
[10] [CSMS # 69711865 — copper F794 turns fatal 2026-09-14](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/427b7f9)
[11] [CSMS # 69668138 — order of reporting for multiple HTS with Ch. 98/99](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4270d2a)
[12] [CSMS # 69635410 — error dictionary v52 adds F883](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4268d52)
[13] [Entry Summary Create/Update (AE/AX), rev 111 — current](/sources/catair-entry-summary-ae-ax-rev-111.md)
[14] [CSMS # 69915041 — CATAIR ES v110 (FY27 user fees) and v111 (ET13)](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/42ad1a1)
[15] [CSMS # 69941677 — error dictionary v53 adds F884 (corrects # 69915227)](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/42b39ad)
[16] [CSMS # 69915001 — error dictionary v54, Entry Type 13 errors](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/42ad179)
[17] [Canada Import Exclusions (CSMS # 70050970) — error 886](/sources/csms-canada-import-exclusions.md)
[18] [CSMS # 69990649 — Section 301 China conforming amendment](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/42bf8f9)
