---
type: Process
title: Entry Summary Filing (AE/AX)
description: The technical side of filing CBP Form 7501 data — AE/AX record formats, the rev 108/109 version split, UC status notifications, and census warning overrides.
tags: [entry-summary, ae, ax, abi, catair, 7501, process]
timestamp: 2026-07-18T20:15:00Z
---

The **Entry Summary Create/Update (AE/AX)** CATAIR chapter defines the record
formats for transmitting entry summary data (CBP Form 7501) to ACE — the
technical layer beneath [Entry Summary in ACE](/entry/entry-summary-ace.md),
which covers the business process. Input structure maps, the ES line and PGA
groupings, party/transportation reporting, and per-entry-type usage notes all
live in this one 246-page chapter.

# Which Version Is in Force — rev 108 vs rev 109

At the time of writing (2026-07-03), ACE production runs
**[Revision 108](/sources/catair-entry-summary-ae-ax-rev-108.md)**
(2025-11-01). **[Revision 109](/sources/catair-entry-summary-ae-ax-rev-109.md)**
(2025-11-06) is published with **deployment TBD** — it expands Global Business
Identifier (GBI) groupings to four repeats and widens the SE31/SE51
identifier field from 20 to 35 characters. File to rev 108 until CBP
announces the cutover; both revisions are retained locally for diffing.

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
  permitted when unknown).
- **Rev 106–107** (2025) carried the FY26 customs user-fee adjustments and
  Global Business Identifier "Test" renaming.

# Responses and Warnings

- **[Entry Summary Status Notification (UC), v30](/sources/catair-entry-summary-status-notification-uc.md)**
  (2025-06) — the unsolicited output messages ACE sends as processing
  conditions change (additional information required, rejections, CBP review
  statuses). Filers need to consume these, not just the synchronous AX
  response.
- **[ACE Error Dictionary — Entry Summary, v51 current](/sources/catair-entry-summary-error-dictionary.md)**
  (2026-07-17) — ~1,000 condition codes with explanations; what a reject
  actually means. Recent additions tracked through CSMS: **864 – PSC NOT
  ALLOWED – REFUND REQUESTED** (V44, blocks a PSC while an
  [IEEPA/CAPE refund](/tariff/ieepa-refunds-cape.md) is in process);
  **F865 – HTS NOT ALLOWED FOR IMPORTER** (V46); **F60D – LIC/CERT/PERM FOR
  HTS MISSING** (V48, USDA agricultural license type 14 on sugar/dairy quota
  HTS); **876** (V49, Section 232 auto-parts duty HTS filed without its
  paired non-duty HTS — the reject behind the rev 108 declaration code above);
  **F875 – IMPORTER INACTIVE FOR ENTRY PURPOSES** (v50, **live in production
  since 2026-07-16**), the entry-summary counterpart of
  [cargo release reject 333](/ace-filing/cargo-release.md) (both enforce the
  [EO 14411 IOR deactivation](/entry/right-to-make-entry.md)); and **F866 /
  F861** (v51, enforced from **2026-07-18**) — the auto-parts offset-license
  validations (license present → the paired Ch. 99 duty must be zero; the
  license balance must cover the claimed offset).
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

[1] [Entry Summary Create/Update (AE/AX), rev 108](/sources/catair-entry-summary-ae-ax-rev-108.md)
[2] [Entry Summary Create/Update (AE/AX), rev 109 — pending](/sources/catair-entry-summary-ae-ax-rev-109.md)
[3] [Entry Summary Status Notification (UC), v30](/sources/catair-entry-summary-status-notification-uc.md)
[4] [Appendix H — Census Warning Override Codes](/sources/catair-appendix-h-census-overrides.md)
[5] [ACE Error Dictionary — Entry Summary, v51 current](/sources/catair-entry-summary-error-dictionary.md)
[6] [ACE Error Dictionary — Entry Summary, v50 draft (superseded)](/sources/catair-entry-summary-error-dictionary-v50-draft.md)
[7] [CSMS # 69268077 — F875 deployed to production 2026-07-16](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/420f26d)
[8] [CSMS # 69271650 — F866/F861 offset-license validations, 2026-07-18](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41e30a7)
[9] [CSMS # 69252300 — copper smelt & cast reporting, effective 2026-07-30](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/420b4cc)
