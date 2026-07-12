---
type: Regulatory Change
title: CPSC eFiling — Live 2026-07-08
description: CPSC certificate data (eFiling) went live in ACE production on 2026-07-08 — what must be filed via the PGA Message Set, disclaimers, registration, and CPSC's advisory-only (no-reject) stance.
tags: [cpsc, efiling, pga, certificates, consumer-products]
timestamp: 2026-07-12T20:00:00Z
---

**CPSC eFiling** requires importers of consumer products regulated by the
Consumer Product Safety Commission to file **certificate of compliance data
electronically** with the entry, through the
[PGA Message Set](/ace-filing/pga-message-set.md) (PG19/PG20/PG30/PG60
records — full message set or a reference to a certificate registered in
CPSC's **Product Registry**).

# Status: Live in Production (since 2026-07-08)

CPSC's PGA Message Set (IG v2.5) **deployed to ACE production on 2026-07-08**
(CERT since 2026-04-15), alongside the CPSC flags in the
[PGA flag enforcement table](/sources/pga-flag-enforcement-table-draft-2026.md).

**Critical operational nuance — CPSC does not reject.** Unlike most PGAs,
CPSC has chosen **not** to require CBP to reject entries for missing or
incomplete message-set data (CSMS # 69177694, 2026-07-08). Filers are
permitted by CPSC regulation to send **no** CPSC message even on an HTS code
flagged **CP1/CP2**; software should treat CPSC flags as **advisory**, not
blocking. This does not relieve the underlying certificate-of-compliance
obligation — it means the ACE tariff flag won't stop release on its own.
A dedicated **CP4** qualifier (component-part description) was added to the
PG60 record for CPSC (CSMS # 69166973).

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
[5] [CSMS # 69177694 — CPSC advisory-only (no reject) clarification](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41f915e)
[6] [CSMS # 69166973 — CP4 qualifier added for CPSC](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/41f677d)
