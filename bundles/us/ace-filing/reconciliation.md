---
type: Process
title: Reconciliation Filing (RE)
description: Entry Type 09 Reconciliation in ACE — flagging entries whose value, classification, 9802, or FTA elements are undeterminable at entry and filing the reconciling summary later.
tags: [reconciliation, entry-type-09, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
---

**Reconciliation** lets an importer file entry summaries with certain
elements estimated — value (e.g. transfer pricing, assists), HTS
classification pending a ruling, 9802 content, or FTA eligibility — by
flagging the underlying entries, then filing an **Entry Type 09
Reconciliation entry summary** that trues them up within the reconciliation
period.

# The Technical Vehicle

The **[Reconciliation Entry Summary Create/Update (RE) chapter](/sources/catair-reconciliation-re.md)**
(June 2025 edition at the time of writing) provides the record formats and
processing instructions for submitting the Type 09 summary to ACE —
association with flagged underlying entries, header/line data, and response
processing. The business rules (which elements may be reconciled, timeframes,
bond riders) are in the ESBP —
[v12.0, reconciliation chapter](/sources/ace-esbp-v12.md).

# When It Matters for Parcel Operations

Reconciliation is mostly a formal-entry program for importers with unsettled
valuation — relevant to BoxC-scale operations where
[transfer pricing or later adjustments](/valuation/customs-valuation.md)
make entered values provisional, rather than to routine low-value traffic.

# Citations

[1] [Reconciliation Entry Summary Create/Update (RE), v12](/sources/catair-reconciliation-re.md)
[2] [ACE Entry Summary Business Rules and Process v12.0](/sources/ace-esbp-v12.md)
