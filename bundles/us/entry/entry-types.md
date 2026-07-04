---
type: Reference
title: Entry Types & Pathways
description: Formal vs informal entry, the ACE entry-type codes relevant to parcel logistics, and which pathway applies by mode and value after the de minimis suspension.
tags: [entry, entry-types, informal-entry, formal-entry, et11, et13, et86]
timestamp: 2026-07-03T19:00:00Z
---

# The Two Statutory Tracks

| Track | Authority | Ceiling | Core requirements |
|-------|-----------|---------|-------------------|
| **Formal entry** | 19 U.S.C. 1484 | none | CBP Form 3461 (entry) + Form 7501 (entry summary) data in ACE, bond, full duty payment. Required for AD/CVD, quota, and other sensitive goods regardless of value. |
| **Informal entry** | 19 U.S.C. 1498 | ≤ $2,500 | Reduced procedure; still requires 10-digit HTSUS, value, duties, and (post-suspension) a bond. CBP may demand formal entry for any shipment. |

# Entry-Type Codes That Matter for Parcels

| Code | Name | Status (2026-07-03) | Notes |
|------|------|---------------------|-------|
| 01 | Consumption — formal | Active | Default formal entry. |
| 03 | Consumption — AD/CVD | Active | Formal entry with antidumping/countervailing duties. |
| 11 | Informal | Active — **primary low-value pathway, non-postal** | ≤ $2,500; 10-digit HTSUS, bond, all duties. No new data elements were added by the 2026 IFR. |
| 13 | Informal — mail (test) | Test begins **2026-09-22** | Electronic informal mail entry in ACE — see [Entry Type 13 Test](/entry/entry-type-13-test.md). |
| 86 | Section 321 de minimis (test) | **Suspended 2026-06-24** | The 2019 electronic de minimis filing is no longer available. |
| — | Release from manifest | **Eliminated for low-value 2026-06-24** | 19 CFR 143.23(j)(3) clearance off manifest/bill data is no longer available for these imports. |
| — | Postal informal entry (IMDW worksheet) | Effective **2026-07-24** | Not an ACE entry type — a monthly emailed worksheet; see [Postal Informal Entry](/entry/postal-informal-entry-imdw.md). |

# Choosing the Pathway (low-value, ≤ $2,500)

| Mode | Pathway | Filer | Bond |
|------|---------|-------|------|
| Express / air / ocean / land freight | **Entry Type 11** (or formal) | Owner, purchaser, or licensed broker | Required (19 CFR 113.62) |
| International mail, now → 2026-07-23 | EO 14324 interim QP spreadsheet (9 fields) | Qualified Party | Required |
| International mail, 2026-07-24 → | **IMDW worksheet** (14 fields) | Licensed US customs broker | Required |
| International mail, 2026-09-22 → (optional) | **Entry Type 13** in ACE (12 elements) | Broker or owner/purchaser | Required |
| Any mode, value > $2,500 | **Formal entry** | Owner, purchaser, or licensed broker | Required |

Shipments subject to AD/CVD or quota must use formal entry regardless of
pathway; alcohol and tobacco are excluded from postal informal entry. PGA-data
and HTSUS Chapter 98/99 goods have transition rules — see the
[eligibility matrix](/entry/postal-informal-entry-imdw.md).

Who may file any of these is constrained by
[Right to Make Entry](/entry/right-to-make-entry.md); foreign importers of
record lose informal entry entirely on 2026-11-30 under
[EO 14411](/enforcement/eo-14411-enforcement.md).

# Citations

[1] [IFR — non-postal de minimis suspension (FR 2026-12670)](/sources/ifr-non-postal-de-minimis.md)
[2] [IFR — mail de minimis suspension & postal informal entry (FR 2026-12669)](/sources/ifr-mail-de-minimis.md)
[3] [General notice — Entry Type 13 test (FR 2026-12668)](/sources/notice-entry-type-13.md)
[4] [ACE Entry Summary Business Process document v12.0](/sources/ace-esbp-v12.md)
