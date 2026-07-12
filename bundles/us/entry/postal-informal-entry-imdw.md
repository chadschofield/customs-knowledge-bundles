---
type: Process
title: Postal Informal Entry (IMDW)
description: The mandatory postal informal entry process effective 2026-07-24 — broker-filed 14-field International Mail Duty Worksheet, bonds, monthly email filing, and Pay.gov payment.
tags: [postal, mail, imdw, informal-entry, process]
timestamp: 2026-07-12T19:30:00Z
---

From **2026-07-24**, international mail shipments valued at **$2,500 or less**
(HTSUS Chapters 1–97) enter via a new postal informal entry process (19 CFR
Part 145; new § 145.15): a licensed US customs broker files a monthly Excel
**International Mail Duty Worksheet (IMDW)** by email, duties are paid on
Pay.gov, and every shipment must be bonded. This replaces the EO 14324 interim
"Qualified Party" spreadsheet and achieves full duty parity with commercial
entries. CBP intends to replace it in turn with the electronic
[Entry Type 13](/entry/entry-type-13-test.md).

# The Four Phases of the Postal Transition

| Phase | Window | Mechanism | Duties |
|-------|--------|-----------|--------|
| 0 | 2025-08-29 → 2026-07-23 | EO 14324 QP spreadsheet, 9 fields, Qualified Party (broker not required) | Method A ad valorem (Method B per-item tiers ended 2026-02-28); in practice only the Section 122 surcharge |
| 1 | 2026-07-24 → | **IMDW**, 14 fields, licensed broker only, bond mandatory | **All applicable duties, taxes, and fees** |
| 2 | 2026-09-22 → (voluntary) | [Entry Type 13](/entry/entry-type-13-test.md) in ACE, 12 elements | All applicable duties, taxes, and fees |
| 3 | 2026-10-22 → | Compliance cliff: PGA / Ch. 98-99 / FTA mail must use formal entry or ET13 | — |

# Eligibility & Exclusions

| Shipment characteristic | IMDW | ET13 (test) | Formal entry |
|---|---|---|---|
| Value ≤ $2,500, HTSUS Ch. 1–97 | ✅ | ✅ | ✅ |
| Value > $2,500 | ❌ | ❌ | ✅ required |
| PGA data requirements (FDA/EPA/FCC…) | ⚠️ only until 2026-10-22 | ✅ (waived) | ✅ |
| HTSUS Ch. 98/99 duties, or Ch. 98/FTA duty-free claim | ⚠️ only until 2026-10-22 | ✅ (waived; FTA claims → formal) | ✅ |
| AD/CVD orders | ❌ | ❌ | ✅ required |
| Absolute or tariff-rate quota | ❌ | ❌ | ✅ required |
| Alcohol; tobacco products (cigars, cigarettes, papers/tubes, snuff…) | ❌ | ❌ | ✅ required |

CBP may require formal entry of **any** mail shipment regardless of value.

# The 14 IMDW Fields (19 CFR Part 145, mail IFR)

| # | Field | Notes |
|---|-------|-------|
| i | Filer Code | NEW — validates the filer is a licensed broker |
| ii | Bond Number | NEW |
| iii | Description of Merchandise | NEW |
| iv | Country of Origin | carried over from QP spreadsheet |
| v | All applicable 10-digit HTSUS classification(s) | NEW |
| vi | Quantity / Weight | NEW — required **only** if a specific (per-unit) duty rate applies |
| vii | Duty Rate | carried over |
| viii | Value | carried over |
| ix | Total Duty Owed | carried over |
| x | Carrier | carried over |
| xi | Flight / Conveyance Number | carried over |
| xii | Tracking Number (foreign post operator) | carried over |
| xiii | Arrival Port | carried over |
| xiv | Arrival Date | carried over |

# Filing Logistics

- **Who files**: a party with the right to make entry — in practice a
  **licensed US customs broker** (filer code validates the license). Foreign
  postal operators, USPS, forwarders, and carriers must engage a broker — see
  [Right to Make Entry](/entry/right-to-make-entry.md).
- **Where**: email the Excel IMDW to **CBPDM@cbp.dhs.gov** — use the
  **official template and CBP's operational guidance**, both in this bundle:
  [CBP Global Guidance for International Mail + IMDW template](/sources/cbp-global-guidance-international-mail.md)
  (CSMS # 69183472, 2026-07-08).
- **When**: by the **7th day of the month following the month of arrival**
  (arrived 2026-08-15 → file and pay by 2026-09-07).
- **Payment**: **Pay.gov**, same 7th-of-month deadline.
- **Bond**: basic importation & entry bond (single-transaction or continuous)
  per 19 CFR 113.62 (new § 145.15); no release from CBP custody without one.
  Carriers moving mail also need an international carrier bond (19 CFR
  113.64) — see [Customs Bonds](/entry/bonds.md).
- **Duty-rate timing**: the rate in effect when entry preparation is complete,
  i.e. when properly transmitted to CBP (19 U.S.C. 1315(a)(1); 19 CFR
  141.68(h)) — significant while tariff schedules are in flux
  ([Tariff Actions](/tariff/tariff-actions-2025-2026.md)).

# Citations

[1] [IFR — mail de minimis suspension & postal informal entry (FR 2026-12669)](/sources/ifr-mail-de-minimis.md)
[2] [EO 14324 — original interim postal process](/sources/eo-14324.md)
[3] [CBP Global Guidance for International Mail + official IMDW template (CSMS # 69183472)](/sources/cbp-global-guidance-international-mail.md)
