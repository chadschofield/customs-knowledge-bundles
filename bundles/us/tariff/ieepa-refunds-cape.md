---
type: Process
title: IEEPA Duty Refunds & the CAPE Tool
description: After the courts invalidated IEEPA tariffs, CBP must refund the duties collected — the CAPE tool in the ACE Portal is the electronic pathway for consolidated refund claims.
tags: [ieepa, refunds, cape, tariffs, ace-portal, process]
timestamp: 2026-07-12T20:00:00Z
---

The IEEPA tariffs were held unlawful (see
[Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md)), so the
duties collected under them must be **refunded**. Because the volume and value
are unprecedented, CBP built the **Consolidated Administration and Processing
of Entries (CAPE)** tool in the **ACE Secure Data Portal** to process refund
claims in bulk rather than entry-by-entry. Any BoxC client that paid IEEPA
duties on imports may be owed a refund through this pathway.

# Legal Basis for the Refunds

| Date | Court action |
|------|--------------|
| 2026-03-02 | The Court of Appeals for the Federal Circuit (CAFC) issued its formal mandate to the Court of International Trade (CIT) on IEEPA duties. |
| 2026-03-04 | *Atmus Filtration, Inc. v. United States* (CIT Ct. No. 26-01259): CBP directed to liquidate all unliquidated entries **without regard to IEEPA duties**, and reliquidate non-final liquidated entries the same way. |
| 2026-03-06 | CIT suspended the immediacy requirement so CBP could build an automated refund tool (CAPE). |
| 2026-04-07 | *Euro-Notions Florida, Inc. v. United States*: parallel CIT order to liquidate/reliquidate without IEEPA duties. |

# CAPE at a Glance

- **Launched 2026-04-20** (Phase 1), announced via CSMS and CBP's
  [IEEPA Duty Refunds page](https://www.cbp.gov/trade/programs-administration/trade-remedies/ieepa-duty-refunds).
- **Consolidates** refunds (principal **plus interest**) across many entries
  into one declaration, instead of per-entry claims.
- **Phase 1 scope**: certain **unliquidated** entries and entries **within 80
  days** of liquidation. CBP is adding functionality in later phases.
- **Who files**: Importers of Record and authorized customs brokers with an
  established **ACE Portal account**; refund recipients register bank details
  in the portal for **ACH** payment (Treasury issued first refunds from
  ~2026-05-12).
- **How**: submit a **CAPE Declaration** in the ACE Portal
  (see CBP's CAPE Declarations Quick Reference Guide). Monitoring reports
  include **ES-022** (CAPE Entry Summary) and **REV-603** (Trade Refund).

# Phase 1 Rollout (what changed, when)

| Effective | Change |
|-----------|--------|
| 2026-04-20 | CAPE Phase 1 live for eligible unliquidated / near-liquidation entries. |
| 2026-06-29 | Accepts entries **flagged for reconciliation** (entry types 01/02/06) with **no** reconciliation entry (type 09) on file, within the same Phase 1 limits. |
| 2026-07-07 | **Warehouse entries** (types 21/22) **no longer accepted** on a CAPE Declaration (rejected as ENTRY TYPE NOT ALLOWED); warehouse **withdrawals** (31/32/34/38) still accepted, refunded on (re)liquidation of the warehouse entry. |

# Interactions With Other Filing

- A **CAPE refund in process blocks a Post-Summary Correction**: entry summary
  error **864 – PSC NOT ALLOWED – REFUND REQUESTED** fires
  ([Entry Summary Filing](/ace-filing/entry-summary-filing.md)).
- Entries refunded through CAPE liquidate with **Liquidation Reason Code 36
  ("CAPE")**, returned by the ACE Entry Summary Query (v26).

# Fraud Warning

CBP warns that scammers target importers over IEEPA refunds. The **only** way
to claim a refund is a CAPE Declaration through a **verified ACE Portal
account**; CBP does not request SSNs, bank details, or passwords by email or
text, and all CBP addresses end in `@cbp.dhs.gov`. Advise clients accordingly.

# Citations

[1] [CSMS # 68315804 — CAPE introduction](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4126a9c)
[2] [CSMS # 68340863 — CAPE update (CIT/CAFC legal background)](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/412cc7f)
[3] [CSMS # 68396594 — CAPE available now](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4126a9c)
[4] [CSMS # 68536553 — ACE reports for CAPE monitoring](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/415c8e9)
[5] [CSMS # 68569567 — refund fraud best practices](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41649df)
[6] [CSMS # 69035485 / # 69066837 — reconciliation-flagged entries](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41de055)
[7] [CSMS # 69127837 — warehouse entries and CAPE](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41ece9d)
[8] [Tariff Actions 2025–2026 (IEEPA invalidation)](/tariff/tariff-actions-2025-2026.md)
