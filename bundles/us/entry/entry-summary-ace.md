---
type: Process
title: Entry Summary in ACE
description: How the detailed duty declaration (CBP Form 7501 data) is filed and processed in ACE — governing documents, statements, post-summary corrections, and liquidation.
tags: [entry-summary, ace, 7501, abi, process]
timestamp: 2026-08-31T21:00:00Z
---

The **entry summary** is the detailed declaration behind an entry — the CBP
Form 7501 data set (classification, valuation, origin, duties, taxes, fees)
transmitted to ACE, generally via ABI, within **10 working days of release**.
Every formal entry and informal Entry Type 11 rides on this machinery, which
is why it now matters for parcel volumes that used to bypass it entirely under
de minimis.

# Governing Documents (both in this bundle)

- **[ACE Entry Summary Business Rules and Process Document v12.0](/sources/ace-esbp-v12.md)**
  (CBP Pub. 3499-1223, Dec 2023) — the authoritative external description of
  entry summary processing in ACE. Chapters cover: entry summary, non-ABI /
  manual entry summary, bonds, blanket declarations, post-summary correction
  (PSC), quota, AD/CVD, reconciliation, protest and 520(d), warehouse entries
  and withdrawals, ACE reports, DCMA entries, foreign trade zones (Entry Type
  06), trade fair entries (Entry Type 24), collections, informal entries, and
  importer identification (CBP Form 5106). Version 11.0 is retained as a
  [superseded copy](/sources/ace-esbp-v11.md).
- **[ACE Entry Summary Instructions v2.4a](/sources/ace-entry-summary-instructions.md)**
  (2016) — field-level guidance for preparing entry summary data in ACE,
  aligned to the 7501 data elements (parties, HTSUS lines, value, duty
  computation, fees).

# Key Facts

| Topic | Rule of thumb |
|-------|---------------|
| Filing window | Entry summary + estimated duties generally due within 10 working days of entry/release. |
| Transmission | Via ABI to ACE — record formats in the AE/AX CATAIR chapter, see [Entry Summary Filing (AE/AX)](/ace-filing/entry-summary-filing.md); non-ABI/manual filing exists but is exceptional. |
| Duty payment | Via statement processing (daily/periodic monthly statements) and ACH — see [Statements & Duty Payment](/ace-filing/statements-duty-payment.md). |
| Corrections | **Post-Summary Correction (PSC)** — electronic amendment of an ACE entry summary within time limits before liquidation; some fields are non-correctable. Rejections may also be issued by CBP. From **2026-08-05**, increases in duties/taxes/fees resulting from a PSC must be paid electronically via **ACH** (debit or credit) — check and cash are no longer accepted (91 FR 41053; CSMS # 69428352). |
| Importer identification | CBP Form 5106 record in ACE (name/address/IOR number) is prerequisite to filing — see [Right to Make Entry](/entry/right-to-make-entry.md). |
| Liquidation | CBP's final duty computation, typically on a ~314-day cycle unless extended/suspended; remedies afterward run through protest (19 U.S.C. 1514) and 520(d) claims. |
| Census warnings | ACE validates trade statistics and issues warnings/overrides filers must resolve. |

For the bond that secures all of this, see [Customs Bonds](/entry/bonds.md);
for classification and rates, [HTS](/tariff/hts.md); for value,
[Customs Valuation](/valuation/customs-valuation.md).

# Caveats

- The ESBP is CBP's living business-rules document (v12.0 current here);
  procedural details (e.g. PSC windows, statement cut-offs) change between
  versions — verify against the latest edition on cbp.gov before relying on a
  specific deadline.
- The Instructions document dates to 2016; where it conflicts with the ESBP
  v12.0 or current CATAIR chapters, the newer documents control.

The record-level CATAIR chapters behind this process (AE/AX filing, UC status
notifications, statements, reconciliation) are distilled in the
[ACE Filing area](/ace-filing/abi-catair-overview.md).

# Citations

[1] [ACE Entry Summary Business Rules and Process Document v12.0](/sources/ace-esbp-v12.md)
[2] [ACE Entry Summary Instructions v2.4a](/sources/ace-entry-summary-instructions.md)
[3] [CBP entry summary program page](https://www.cbp.gov/trade/programs-administration/entry-summary)
[4] [Entry Summary Create/Update (AE/AX) CATAIR chapter, rev 108](/sources/catair-entry-summary-ae-ax-rev-108.md)
[5] [CSMS # 69428352 — PSC modifications: ACH-only payment of PSC increases from 2026-08-05 (91 FR 41053)](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4236480)
