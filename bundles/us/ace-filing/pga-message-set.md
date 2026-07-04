---
type: Process
title: PGA Message Set Filing
description: How partner government agency data is filed with entries — PG records, tariff flags and enforcement, corrections, prior notice, status notifications, and the error dictionary.
tags: [pga, message-set, tariff-flags, fda, cpsc, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
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
  (2026-04-27) — **scheduled for production 2026-07-08**, the same
  deployment that turns on [CPSC eFiling](/ace-filing/cpsc-efiling.md).
  Verify enforcement behavior against the current table after that date.

# Corrections, Prior Notice, and Status Flow

- **[PGA Data Corrections (CA/CC)](/sources/catair-pga-data-corrections-ca-cc.md)**
  (2025-06-20) — correcting PGA data already on file, pre- or post-release.
- **[Stand-alone Prior Notice (PE/PX)](/sources/catair-pga-standalone-pe-px.md)**
  (2018) and its **[status notification (PO)](/sources/catair-pga-standalone-po.md)**
  (2021) — FDA Prior Notice outside an entry filing.
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
