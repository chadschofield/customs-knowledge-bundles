---
type: Regulatory Change
title: CPSC eFiling — Mandatory 2026-07-08
description: CPSC certificate data (eFiling) becomes enforced in ACE production on 2026-07-08 — what must be filed via the PGA Message Set, disclaimers, and registration.
tags: [cpsc, efiling, pga, certificates, consumer-products, deadline]
timestamp: 2026-07-03T23:59:00Z
---

**CPSC eFiling** requires importers of consumer products regulated by the
Consumer Product Safety Commission to file **certificate of compliance data
electronically** with the entry, through the
[PGA Message Set](/ace-filing/pga-message-set.md) (PG19/PG20/PG30/PG60
records — full message set or a reference to a certificate registered in
CPSC's **Product Registry**).

# Status at the Time of Writing (2026-07-03)

CBP's CATAIR page lists **CPSC eFiling (IG v2.5) for production deployment
2026-07-08**, alongside the matching
[draft PGA flag enforcement table](/sources/pga-flag-enforcement-table-draft-2026.md)
— i.e. CPSC tariff-flag enforcement and eFiling go live together, **five days
after this bundle's as-of date**. Filers must be registered (eFiling
self-registration is open) and able to transmit or disclaim per the guide.

# Why This Bites Parcel Traffic

Toys, children's products, electronics, and household goods — core ecommerce
categories — are CPSC-regulated. Under de minimis these parcels filed no
entry data at all; post-[suspension](/entry/de-minimis-suspension.md) they
file [Entry Type 11 or formal entries](/entry/entry-types.md), which exposes
them to CPSC tariff flags. The IG's own history tracks this shift: **v2.3
(April 2026) removed the guide's de minimis references and dropped the
"Voluntary Stage"** language.

# Governing Documents

- **[CPSC eFiling Implementation Guide v2.5](/sources/catair-cpsc-efiling-ig-v2.5.md)**
  (May 2026, current) — filing methods, Disclaim A/B rules (v2.5 updated
  Disclaim A scenarios; v2.4 added an intended-use restriction on Disclaim
  B), message-set details, hierarchy and examples.
- **[v2.3](/sources/catair-cpsc-efiling-ig-v2.3.md)** (April 2026) — retained
  superseded copy.
- Supporting documents: [CPSC eFiling document library](https://www.cpsc.gov/eFiling-Document-Library).

# Citations

[1] [CPSC eFiling Implementation Guide v2.5](/sources/catair-cpsc-efiling-ig-v2.5.md)
[2] [CPSC eFiling Implementation Guide v2.3 (superseded)](/sources/catair-cpsc-efiling-ig-v2.3.md)
[3] [PGA Flag Enforcement table — draft deploying 2026-07-08](/sources/pga-flag-enforcement-table-draft-2026.md)
[4] [CBP CATAIR page — deployment schedule](https://www.cbp.gov/trade/ace/catair)
