---
type: Regulatory Change
title: Regulatory Watch
description: Rolling record of recent operative CBP/CSMS announcements affecting this bundle — newest first; entries leave the list once fully absorbed into concepts and no longer time-critical.
tags: [watch, csms, monitoring]
timestamp: 2026-07-23T18:20:00Z
---

Dated one-liners of recent regulatory and operational announcements — mostly
from CBP's **Cargo Systems Messaging Service (CSMS)** — that affect the
knowledge in this bundle. This page tracks *the world changing*;
[log.md](/log.md) tracks *this bundle changing*. An entry is pruned once its
content is fully reflected in the concepts it names and its dates have passed.
Messages are cited as `CSMS # <number>` with their public GovDelivery
bulletin.

# Watch List

## 2026-07-22 — Section 301: 25% on products of Brazil

USTR's first big Section 301 country action of the successor regime
(91 FR 45516): 25% on all Brazil products via heading 9903.05.01, exemptions
9903.05.02–.09 — including an **in-transit window that closes with entries on
2026-07-29**. Reflected in
[Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md); exemption
HTS list archived as a [source](/sources/csms-section-301-brazil.md). Status:
**absorbed**; the in-transit deadline is the time-critical part.

## 2026-07-24 / 09-22 — Entry Type 13 lands in ACE (CERT, then PROD)

The ET13 build (INT-057/CBP-290) deploys to Certification **2026-07-24** and
Production **2026-09-22**, confirming the test start; draft implementation
guides are posted (CSMS # 69289734, # 69298180). Reflected in
[Entry Type 13 Test](/entry/entry-type-13-test.md). Status: **absorbed** —
watch for revised IGs and the production go-live.

## 2026-07-30 — Copper smelt & cast reporting becomes mandatory

Per Proclamation 11021, entry summary lines for copper articles under HTS
8544.42.10/.20/.90 and 8544.49.10 must report primary country of smelt and
country of cast from **2026-07-30** (CSMS # 69252300). Reflected in
[Entry Summary Filing](/ace-filing/entry-summary-filing.md). Status:
**upcoming** — prune after the effective date.

## 2026-07-16/18 — IOR auto-deactivation live; offset-license validations live

ACE now auto-deactivates IORs with no entry in 366 days ("Inactive for Entry
Purposes", 2026-07-16; CSMS # 69241265) and rejects their filings (cargo
release 333 / entry summary F875, error dictionary v50; CSMS # 69268077).
The Section 232 auto-parts offset license is validated from 2026-07-18
(F866/F861, v51; CSMS # 69271650). Reflected in
[Right to Make Entry](/entry/right-to-make-entry.md) and
[Entry Summary Filing](/ace-filing/entry-summary-filing.md). Status:
**absorbed**.

## 2026-07 — CPSC eFiling live; CPSC is advisory-only

CPSC's PGA Message Set went to production **2026-07-08**; CSMS # 69177694
clarifies CPSC will **not** reject entries for missing data (advisory flags
only). Reflected in [CPSC eFiling](/ace-filing/cpsc-efiling.md) and
[PGA Message Set](/ace-filing/pga-message-set.md).

## 2026-07-08 — CSMS # 69183472 — Updated Global Guidance for International Mail

CBP's operational guidance and the **official IMDW template** for the postal
informal entry process effective **2026-07-24**. Archived as a
[source](/sources/cbp-global-guidance-international-mail.md); reflected in
[Postal Informal Entry (IMDW)](/entry/postal-informal-entry-imdw.md).

## 2026-06 — Forced-labor operational guidance + Jordan WROs

CBP consolidated its 19 U.S.C. 1307 / UFLPA / CAATSA guidance
(CSMS # 68927213) and issued WROs on Jordan garment producers
(CSMS # 69031301). Captured in [Forced Labor Enforcement](/enforcement/forced-labor.md).

## 2026-04 → ongoing — IEEPA refunds via CAPE

Court-ordered refunds of invalidated IEEPA duties are processed through the
CAPE tool (launched 2026-04-20; reconciliation-flagged entries from 06-29;
warehouse-entry rule from 07-07). Captured in
[IEEPA Duty Refunds & the CAPE Tool](/tariff/ieepa-refunds-cape.md).

## 2026-04 → ongoing — Section 232 metals duties live

Proclamation 11021 (10–50% on aluminum/steel/copper, effective 2026-04-06),
Annex IV technical corrections, and Taiwan/MHDV modifications. Captured in
[Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md); covered-HTS
lists archived as a [source](/sources/csms-section-232-metals.md).

## Ongoing — recurring feeds folded into concepts

- **Harmonized System Updates (HSU 2607–2616):** ACE tariff-record loads,
  absorbed by the [HTS](/tariff/hts.md) JSON refresh.
- **Commodity quota bulletins** (cotton TRQ openings, etc.): out of scope
  for parcel traffic; now dropped by the feed filter.
- **Entry-summary error dictionary additions** (864, F865, F60D, 876, F875,
  F866/F861 — v51 current): [Entry Summary Filing](/ace-filing/entry-summary-filing.md).
- **PGA Message Set / flag-enforcement / error-dictionary revisions:**
  [PGA Message Set](/ace-filing/pga-message-set.md).

## 2026-02 → 2026-12 — AGOA / Haiti HOPE-HELP reauthorized

H.R.7148 extended duty-free treatment through **2026-12-31** with retroactive
refunds for the 2025-10-01 → 2026-02-03 lapse (CSMS # 68987884). Watch item
only — no preference-program concept in the bundle yet; revisit before the
December expiry.
