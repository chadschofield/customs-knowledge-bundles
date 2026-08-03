---
type: Process
title: PGA Message Set Filing
description: How partner government agency data is filed with entries — PG records, tariff flags and enforcement, corrections, prior notice, status notifications, and the error dictionary.
tags: [pga, message-set, tariff-flags, fda, cpsc, aphis, abi, catair, process]
timestamp: 2026-08-03T15:30:00Z
---

The **PGA Message Set** is the single mechanism for submitting partner
government agency data (FDA, CPSC, EPA, APHIS, FWS, NHTSA, TTB, …) with
[cargo release](/ace-filing/cargo-release.md) and
[entry summary](/ace-filing/entry-summary-filing.md) filings: **PG01–PG60
records** nested under the line's OI record. With ecommerce goods now filing
real entries post-[de minimis](/entry/de-minimis-suspension.md), PGA data
requirements hit parcel traffic that never used to see them.

# Core Documents

- **[PGA Message Set chapter, rev 28](/sources/catair-pga-message-set.md)**
  (2026-04-28 at the time of writing) — the PG record layouts and correction
  capability.
- **[Appendix PGA](/sources/catair-appendix-pga.md)** (2026-03-02, 303 pages)
  — the master code tables: agency program codes, processing codes,
  qualifiers, units, species codes.
- **[PGA Error Dictionary, v16](/sources/pga-error-dictionary.md)** (XLSX,
  2026-06-01) — ~1,000 P-series reject codes with agency, record, and
  resolution detail.
- **[Appendix V — agency codes](/sources/catair-appendix-v-agency-codes.md)**,
  **[Appendix R — intended use codes](/sources/catair-appendix-r-intended-use-codes.md)**.

# Tariff Flags: When PGA Data Is Demanded

HTS numbers carry per-agency **tariff flags** — MUST (data required), MAY
(data or disclaim), and flags restricting which disclaim codes an agency
accepts. The rule logic is defined in the
**[ACE Agency Tariff Code Reference](/sources/ace-agency-tariff-codes.md)**
(2026-03-04). Whether a flag is actually *enforced* (blocks release) varies
by entry type and condition per the **flag enforcement matrix**:

- **[Production table](/sources/pga-flag-enforcement-table.md)** (2021-12-15
  edition, XLSX)
- **[Draft update](/sources/pga-flag-enforcement-table-draft-2026.md)**
  (2026-04-27, reinserting footnote #4 per CSMS # 68510400) — **deployed to
  production 2026-07-08**, the same deployment that turned on
  [CPSC eFiling](/ace-filing/cpsc-efiling.md) and added CPSC flag enforcement.
  Verify enforcement behavior against the current table on CBP.gov.

The table has moved twice since, and in opposite directions — check which
section of the [CATAIR page](https://www.cbp.gov/trade/automated/catair)
you're pulling from:

- **2026-07-28** — the edition backing CPSC moved out of *Draft Chapters:
  Future Capabilities* into the production **PGA Message Set Documents**
  section, alongside the CPSC IG (CSMS # 69368723).
- **2026-07-29** — a *new* draft appeared in *Draft Chapters* adding the
  enforcement flag for **Entry Type 13** (CSMS # 69379627), tracking the
  [ET13 test](/entry/entry-type-13-test.md) deployment. ET13 flag enforcement
  is therefore draft-stage while the CPSC flags are production.

The message set and its tables are **living documents**; recent revisions
(mid-2026): PG60 qualifier codes **LAT/LON** (PG19) and a new PG30 lab/testing
status **N** (CSMS # 68510144); the CPSC **CP4** component-part qualifier
(CSMS # 69166973); and a quarterly **PGA Error Code Dictionary** refresh
adding PHI/PHJ/PHK and DEA/FDA program codes (CSMS # 68770001). Re-verify
record layouts against the current chapter before relying on a specific field.

## APHIS Plant Inspection Station Filings (draft; PROD 2026-08-27)

APHIS revised the Core Message Set Implementation Guide and Supplemental Trade
Guide for imports destined for **Plant Inspection Stations (PIS)**, with a
matching **Appendix PGA** draft (CSMS # 69379587 and # 69402038, both
2026-07-29/31, in *Draft Chapters: Future Capabilities*). Deployment: **CERT
2026-07-27**, **PRODUCTION 2026-08-27**.

- **Category code 406** is retitled **Tissue Culture** with a new definition,
  and now requires the **Growing Media (A43)** qualifier — values **AGAR** or
  **EXAR** (both newly added to the PG10 commodity-characteristic qualifier
  list). Report **physical state (A41)** where applicable — **WIRT** or
  **WORT**.
- **PG30** accepts **"I"** as a laboratory/testing status, required only for
  products proceeding to a PIS; it drives automated routing of the message set
  to the correct PIS for review and clearance.
- **Port of Arrival ("A") must still be reported** even when it differs from
  the anticipated inspection location — the PIS routing does not replace it.

# Corrections, Prior Notice, and Status Flow

- **[PGA Data Corrections (CA/CC)](/sources/catair-pga-data-corrections-ca-cc.md)**
  (2025-06-20) — correcting PGA data already on file, pre- or post-release.
- **[Stand-alone Prior Notice (PE/PX)](/sources/catair-pga-standalone-pe-px.md)**
  (2018) and its **[status notification (PO)](/sources/catair-pga-standalone-po.md)**
  (2021) — FDA Prior Notice outside an entry filing. A **draft PE/PX update
  adding Entry Type 13 guidance** was posted 2026-07-29
  (CSMS # 69379504) — relevant because ET13 waives the formal-entry
  requirement for PGA-flagged mail, so prior notice has to work on an informal
  mail entry; see [Entry Type 13 Test](/entry/entry-type-13-test.md).
- **[PGA Status Notification Codes](/sources/catair-pga-status-notification-codes.md)**
  (2023-08-09) — the SO70/SO71 and PO70/PO71 status and reason codes filers
  must interpret (may proceed, hold, documents required, …).

# Citations

[1] [PGA Message Set chapter, rev 28](/sources/catair-pga-message-set.md)
[2] [Appendix PGA](/sources/catair-appendix-pga.md)
[3] [ACE Agency Tariff Code Reference](/sources/ace-agency-tariff-codes.md)
[4] [PGA Flag Enforcement table (production)](/sources/pga-flag-enforcement-table.md)
[5] [PGA Flag Enforcement table (draft, deploys 2026-07-08)](/sources/pga-flag-enforcement-table-draft-2026.md)
[6] [PGA Error Dictionary v16](/sources/pga-error-dictionary.md)
[7] [PGA Data Corrections (CA/CC)](/sources/catair-pga-data-corrections-ca-cc.md)
[8] [Stand-alone Prior Notice (PE/PX)](/sources/catair-pga-standalone-pe-px.md)
[9] [Prior Notice Status Notification (PO)](/sources/catair-pga-standalone-po.md)
[10] [PGA Status Notification Codes](/sources/catair-pga-status-notification-codes.md)
[11] [Appendix V — Government Agency Codes](/sources/catair-appendix-v-agency-codes.md)
[12] [Appendix R — Intended Use Codes](/sources/catair-appendix-r-intended-use-codes.md)
[13] [CSMS # 68510144 — PG60 LAT/LON, PG30 status N](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41561c0)
[14] [CSMS # 68770001 — PGA Error Code Dictionary quarterly update](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41958d1)
[15] [CSMS # 69368723 — CPSC IG and flag enforcement table moved to production documents](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4227b93)
[16] [CSMS # 69379627 — draft flag enforcement table adds the Entry Type 13 flag](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/422a62b)
[17] [CSMS # 69379504 — draft PE/PX prior notice update for Entry Type 13](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/422a5b0)
[18] [CSMS # 69379587 — APHIS Plant Inspection Station message set updates](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/422a603)
[19] [CSMS # 69402038 — updated draft Appendix PGA (AGAR/EXAR, category 406)](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/422fdb6)
