---
type: Overview
title: US Import System Overview
description: Orientation to US customs — agencies, the entry lifecycle, key systems and parties, and the 2025–2026 low-value entry upheaval.
tags: [cbp, imports, orientation]
timestamp: 2026-07-03T23:59:00Z
---

Knowledge in this bundle is current as of **2026-07-03**. The low-value entry
regime is mid-transition (interim final rules with open comment periods), so
several concepts carry effective dates in the future.

# Who Regulates What

| Body | Role |
|------|------|
| **U.S. Customs and Border Protection (CBP)**, DHS | Administers entry, collects duties, enforces customs law (19 CFR chapter I). |
| **U.S. International Trade Commission (USITC)** | Maintains and publishes the [Harmonized Tariff Schedule](/tariff/hts.md). |
| **Partner Government Agencies (PGAs)** | FDA, FCC, EPA, USDA, CPSC and others impose admissibility data requirements enforced at entry through ACE. |
| **Department of Commerce / USTR / President** | Trade remedies (AD/CVD, Section 201/232/301) and emergency tariff actions — see [Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md). |

# The Entry Lifecycle

1. **Pre-arrival & manifest** — the carrier transmits cargo data to CBP
   (air: ACAS; ocean: ISF + manifest). Postal traffic moves on foreign postal
   operator (FPO) data.
2. **Entry / release** — an entry (e.g. CBP Form 3461 data, or an informal
   entry type) is filed in the Automated Commercial Environment (ACE) and CBP
   authorizes release. Who may file is restricted — see
   [Right to Make Entry](/entry/right-to-make-entry.md).
3. **Entry summary** — the detailed declaration (CBP Form 7501 data:
   classification, value, duties) filed in ACE, generally within 10 working
   days of release — see [Entry Summary in ACE](/entry/entry-summary-ace.md).
4. **Duty payment** — via ACH statement processing or, for the postal interim
   process, Pay.gov.
5. **Liquidation** — CBP's final computation of duties, after which limited
   correction windows (PSC, protest) apply.

Security at every step rides on [customs bonds](/entry/bonds.md).

# Formal vs Informal Entry

- **Formal entry** (19 U.S.C. 1484): required above $2,500 and for sensitive
  merchandise (AD/CVD, quota, some PGA goods); full 3461/7501 data and a bond.
- **Informal entry** (19 U.S.C. 1498): available at or below $2,500 for most
  goods with lighter procedure — see [Entry Types & Pathways](/entry/entry-types.md).

# The 2025–2026 Upheaval (why this bundle exists)

Until 2025, most ecommerce parcels entered duty-free under the $800
**de minimis** exemption (Section 321) with minimal data. That world is gone:

- **2025-08-29** — EO 14324 suspended de minimis globally.
- **2026-06-24** — twin interim final rules made the suspension indefinite for
  postal and non-postal modes; **Entry Type 86 and release-from-manifest were
  eliminated**. Non-postal low-value traffic now files
  [Entry Type 11](/entry/entry-types.md) or formal entry.
- **2026-07-24** — mail shipments move to the mandatory
  [postal informal entry / IMDW process](/entry/postal-informal-entry-imdw.md),
  with the electronic [Entry Type 13 test](/entry/entry-type-13-test.md)
  starting 2026-09-22.
- **2027-07-01** — statutory repeal of de minimis (One Big Beautiful Bill Act).

Full timeline and surviving exemptions:
[De Minimis Suspension](/entry/de-minimis-suspension.md). In parallel,
[EO 14411](/enforcement/eo-14411-enforcement.md) is tightening who may act as
importer of record and raising penalties, and tariff authority itself is in
flux — see [Tariff Actions 2025–2026](/tariff/tariff-actions-2025-2026.md).

# Key Systems

| System | Purpose |
|--------|---------|
| **ACE** (Automated Commercial Environment) | Single window for entries, entry summaries, manifests, PGA data, statements, reports. |
| **ABI** (Automated Broker Interface) | EDI channel filers use to transmit entries/entry summaries into ACE — specs and local copies in [ABI & CATAIR](/ace-filing/abi-catair-overview.md). |
| **eBond** | Electronic transmission of bonds to ACE — see [eBond Filing](/ace-filing/ebond-filing.md). |
| **Pay.gov** | Duty payment channel for the interim postal process. |

# Citations

[1] [De minimis suspension source documents](/sources/index.md)
[2] [19 CFR — Customs Duties](/regulations/cfr-title-19.md)
