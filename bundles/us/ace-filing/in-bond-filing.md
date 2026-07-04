---
type: Process
title: In-Bond Filing (QP)
description: Moving merchandise under bond without entry — QP in-bond transactions against eManifest/Truck bills, arrival/export/transfer of liability, and the error dictionary.
tags: [in-bond, qp, it, te, ie, bonded-carrier, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
---

**In-bond** moves merchandise that has not been entered — under bond, in CBP
custody — between US ports: **IT** (Immediate Transportation, entry filed at
the destination port), **T&E** (Transportation & Exportation), and **IE**
(Immediate Exportation). For parcel logistics it is the mechanism behind
moving arriving consolidations inland to a hub port before
[entry](/entry/entry-types.md) is filed there.

# Governing Documents (both in this bundle)

- **[In-Bond implementation guide, Amendment 51](/sources/catair-in-bond.md)**
  (April 2026 at the time of writing) — **QP** transaction record formats:
  in-bond bill of lading input/output against ACE eManifest (Air/Sea/Rail)
  and ACE Truck bills, update and transfer-of-liability records, arrival and
  export transactions, and status notifications.
- **[Appendix T — In-bond Common Errors](/sources/catair-appendix-t-in-bond-errors.md)**
  (2025-09) — the error dictionary for QP/WP transmissions.

# Operational Notes

- The party moving in-bond freight needs a **custodian of bonded merchandise
  bond** (activity code 2) — see [Customs Bonds](/entry/bonds.md).
- Arrival and export must be reported electronically within regulatory
  deadlines (19 CFR Part 18); overdue in-bonds generate liquidated-damages
  exposure against that bond.
- In-bond status rides the same status-notification machinery as release —
  disposition codes in
  [Appendix N](/sources/catair-appendix-n-disposition-codes.md).

# Citations

[1] [ACE CATAIR — In-Bond, Amendment 51](/sources/catair-in-bond.md)
[2] [Appendix T — In-bond Common Errors](/sources/catair-appendix-t-in-bond-errors.md)
