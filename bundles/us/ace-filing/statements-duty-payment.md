---
type: Process
title: Statements & Duty Payment
description: How duties are actually paid through ABI — daily statements and Periodic Monthly Statement (PMS), including the 2025 de-minimis-driven cap change.
tags: [statements, duty-payment, ach, pms, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
---

Duties, taxes, and fees on ACE entry summaries are normally paid by
**statement processing** over ACH rather than entry-by-entry: filers group
entry summaries onto statements, receive statement output records, and settle
the statement total.

# The Two Statement Cycles

| Cycle | Governing document | Gist |
|-------|-------------------|------|
| **Daily statement** | [Daily Statement chapter, rev 15](/sources/catair-daily-statement.md) (2025-04-23 at the time of writing) | Entry summaries scheduled to a preliminary daily statement; final statement confirms what was paid. |
| **Periodic Monthly Statement (PMS)** | [PMS chapter](/sources/catair-periodic-monthly-statement.md) (2019-03-06) | Eligible entry summaries consolidate onto one monthly statement (Q-series output records), deferring payment to the 15th working day of the following month — a meaningful cash-flow tool for high-volume importers. |

# De Minimis Fallout Reached the Statement Layer

Daily Statement **revision 15 (2025-04-23) cut the maximum entry summaries on
a statement update from 9,999 to 2,000**, explicitly "as a result of
restriction of de minimis treatment of low value shipments" — parcel volumes
moving into [Entry Type 11](/entry/entry-types.md) pushed statement sizes
past what the interface handled. High-volume parcel filers should plan
statement grouping around the 2,000-entry cap.

Note the interim postal process pays via **Pay.gov**, not statements — see
[Postal Informal Entry (IMDW)](/entry/postal-informal-entry-imdw.md).

# Citations

[1] [ACE CATAIR — Daily Statement, rev 15](/sources/catair-daily-statement.md)
[2] [ACE CATAIR — Periodic Monthly Statement](/sources/catair-periodic-monthly-statement.md)
[3] [Entry Summary in ACE](/entry/entry-summary-ace.md) — business context for statement processing
