---
type: Regulatory Change
title: CPSC eFiling — Live 2026-07-08
description: CPSC certificate data (eFiling) went live in ACE production on 2026-07-08 — what must be filed via the PGA Message Set, disclaimers, registration, and CPSC's advisory-only (no-reject) stance with SO-message review and retained enforcement.
tags: [cpsc, efiling, pga, certificates, consumer-products]
timestamp: 2026-08-03T15:30:00Z
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
PG60 record for CPSC (CSMS # 69166973), and the **CP1/CP2 tariff flags** were
loaded into ACE via Harmonized System Update 2615 (created 2026-07-10,
CSMS # 69239974).

**What "advisory" means for filing software** (CSMS # 69382435, 2026-07-29,
updating # 69177694). Per CPSC's
[certificates final rule](https://www.federalregister.gov/documents/2025/01/08/2024-30826/certificates-of-compliance)
and [eFiling FAQ](https://cpsc.gov/FAQ/eFiling-Frequently-Asked-Questions-FAQ),
ACE accepts entries with **no CPSC message set at all**, and entries whose
CPSC message set is **missing some CPSC data** — provided the overall CATAIR
PGA message-set spec is still satisfied. Three consequences:

- **Developers must not gate submission on CPSC flags.** Software should let
  users transmit CPSC data even where the flagging requirements are not met.
- **No SX reject, but CPSC still answers.** CBP won't reject the entry, but
  CPSC may respond in an **SO message** reviewing the submitted CPSC data —
  including **rejecting the CPSC data** itself. Build for an SO response, not
  silence.
- **Enforcement is retained.** CPSC may take enforcement action on any entry
  that lacks eFiling data where it was required. "Won't reject" is a
  release-mechanics statement, not a compliance waiver.

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
  B), message-set details, hierarchy and examples. As of **2026-07-28** the
  CPSC IG and the PGA Flag Enforcement Table moved out of CBP.gov's
  *Draft Chapters: Future Capabilities* section into the production
  **PGA Message Set Documents** section (CSMS # 69368723) — they are no longer
  drafts; pull them from the
  [CATAIR page](https://www.cbp.gov/trade/automated/catair).
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
[7] [CSMS # 69382435 — CPSC advisory-only mechanics: no SX reject, SO review, retained enforcement](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/422b123)
[8] [CSMS # 69368723 — CPSC IG and PGA Flag Enforcement Table moved to production documents](https://content.govdelivery.com/accounts/USDHSCBP/bulletins/4227b93)
