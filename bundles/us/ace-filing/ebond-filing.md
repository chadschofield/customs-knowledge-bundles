---
type: Process
title: eBond Filing (CB/CX)
description: How sureties and surety agents transmit customs bonds electronically to ACE — the CB/CX record formats behind every bond that secures an entry.
tags: [ebond, bonds, surety, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
---

**eBond** is the electronic transmission of customs bond data to ACE. The
filer here is not the importer or broker but the **surety or surety agent**:
they submit single-transaction and continuous bonds via the **CB** input
records and receive **CX** responses, so the bond is on file in ACE before
the entry that draws on it arrives.

# Governing Document

**[Customs eBond Create/Update (CB/CX), v1.9](/sources/catair-ebond-cb-cx.md)**
(2020-04-10 at the time of writing) — input/output EDI record formats for
bond creation and update, covering both STB and continuous bonds.

# Why It Matters More Now

Since the [de minimis suspension](/entry/de-minimis-suspension.md), every
low-value pathway requires a bond on file — see
[Customs Bonds](/entry/bonds.md) for bond types, activity codes, and who is
obligated. Bond sufficiency rulemaking under
[EO 14411](/enforcement/eo-14411-enforcement.md) (minimum asset/bonding
levels, foreign-IOR continuous bond restrictions) will land on this same
filing machinery: an STB per shipment at parcel volumes only works because
eBond is electronic.

# Citations

[1] [Customs eBond Create/Update (CB/CX), v1.9](/sources/catair-ebond-cb-cx.md)
[2] [Customs Bonds](/entry/bonds.md)
