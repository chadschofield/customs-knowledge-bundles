---
type: Process
title: Postal Returns, Refunds & Drawback
description: What happens to duty when inbound mail is refused, undeliverable, or sent back — the release-from-custody line (19 U.S.C. 1558), §§ 145.5/145.71/158.45 for mail returned from custody, Part 190 drawback after release, and the open gap for broker-filed IMDW/ET13 entries.
tags: [postal, mail, returns, refund, drawback, undeliverable, refused, et13, imdw]
timestamp: 2026-11-12T17:00:00Z
---

When an inbound mail parcel never reaches the addressee, or comes back after
delivery, how the duty is recovered depends on one question: **was the
parcel released from Government (CBP or postal) custody?** The line comes
from 19 U.S.C. 1558, implemented at 19 CFR 158.45:

| Situation | Route | Duty outcome | Rules |
|---|---|---|---|
| Refused, unclaimed, or undeliverable **while still in postal/CBP custody** and returned abroad | Return to country of origin by the Postal Service | No duty owed; any duty paid is refundable; mail entry cancelled | §§ 145.5, 145.71(a), (c)(1); § 158.45(a) |
| Not returned abroad (or forwarded) despite being undeliverable | Delivered to CBP | Disposed of under the seized/unclaimed merchandise rules | § 145.5 |
| Undeliverable mail carrying a **mail fine entry** (§ 145.4(c)) | Returned to the port that issued the entry | Disposition as seizable merchandise | §§ 145.4(c), 145.59 |
| **Released** to the addressee, then exported or destroyed | Drawback claim | Up to **99%** of duties paid | § 158.45(b); 19 CFR Part 190 |
| Dispute over the **amount** of duty assessed (parcel kept) | Administrative review / protest | Refund if the entry is amended | §§ 145.21–145.25 |

# Returned From Custody (No Drawback Needed)

- **§ 145.5 — Undeliverable packages.** Refused or undeliverable mail is
  marked by the postmaster with the reason and forwarded to the exchange post
  office for return to the country of origin. The mail entries are removed
  and **returned to Customs for cancellation**.
- **§ 145.71 — Exportation from continuous Government custody.** Merchandise
  that stayed continuously in CBP or postal custody may be exported by mail
  **without payment of duties**, inspected and mailed under CBP supervision,
  with a signed waiver of the right to withdraw it from the mails. Paragraph
  (c)(1) **waives the export entry** (§ 18.25) for mail that is unclaimed or
  refused and being returned by the Postal Service as undeliverable.
- **§ 158.45(a) — the general rule.** Merchandise in CBP custody whose entry
  is incomplete, or that stayed in continuous custody under a liquidated or
  unliquidated consumption entry, may be exported under supervision **with
  refund of any duties paid**. This is a full refund, not 99% drawback.
- Drawback's own continuous-custody provision (Part 190 subpart O, 19 U.S.C.
  1557(a)) **does not apply to mail**: § 190.165 bars exportation by mail
  under that subpart. For mail, the custody route is § 145.71 / § 158.45(a).

## The Gap: Broker-Filed Entries (IMDW and ET13)

§ 145.5's "returned to Customs for cancellation" was written for mail
entries CBP prepared and attached to the parcel. Under the 2026 regime the
entry is filed by a broker instead — a monthly emailed
[IMDW worksheet](/entry/postal-informal-entry-imdw.md) paid on Pay.gov, or
an [Entry Type 13](/entry/entry-type-13-test.md) entry in ACE — and neither
the mail IFR, the ET13 notices, nor CBP's Global Guidance for International
Mail (at the time of writing) says how a filer cancels the entry or recovers
duty already paid when a parcel is refused before delivery. Two related
facts:

- ET13 entry summaries **cannot be corrected by post-summary correction**:
  error B49, "PSC NOT ALLOWED – CANNOT BE INFORMAL/MAIL", covers entry types
  11, 12 and 13 (see [Entry Type 13](/entry/entry-type-13-test.md)).
- The [Low-Value Shipments NPRM](/sources/nprm-low-value-shipments.md)
  leaves §§ 145.5 and 145.71 unchanged. Its new § 145.6 covers the opposite
  case: mail of $2,500 or less **never entered** within 15 days of
  importation is deemed abandoned, is not released, and goes to USPS for
  disposition. Its regulatory analysis asks for comment on the cost of
  returning undeliverable mail (comments close 2026-12-07).

Until CBP publishes a procedure, confirm the refund mechanics for a refused,
already-entered parcel with CBP (for IMDW, the CBPDM@cbp.dhs.gov filing
mailbox). Rulings precedent in CROSS was not checked when this concept was
written: the CROSS search API began requiring a reCAPTCHA token on every
request (2026-11-12).

# After Release: Drawback (19 CFR Part 190)

Once the parcel has left custody, § 158.45(b) allows no refund on
exportation **unless drawback is provided by law**. Claims are filed under
**Part 190** (19 U.S.C. 1313 as amended in 2016). Part 191 is the legacy
regime and has been closed to new claims since 2019-02-23; the
cross-reference in § 145.72(e) to § 191.42 predates that switch, and the
current rejected-merchandise procedure is § 190.42.

Drawback types that fit returned parcels:

| Type | Rule | When it fits |
|---|---|---|
| Rejected merchandise — 19 U.S.C. 1313(c) | § 190.41 | Goods that do not conform to sample or specifications, were **shipped without the consignee's consent**, or were defective at importation |
| Returned retail merchandise — 1313(c)(1)(C)(ii) | § 190.45 | Sold at retail, returned to and accepted by the importer (the ecommerce return). Substitution allowed: designate an entry imported within **1 year** before export/destruction, same 8-digit HTSUS and same SKU/part number |
| Unused merchandise — 1313(j) | Part 190 subpart C | Exported or destroyed unused, direct identification or substitution |

Mechanics that matter for mail:

- **Amount:** 99% of duties paid (§ 190.41, § 190.45(c)).
- **Deadline:** exportation or destruction within 5 years of importation
  (§ 190.42(a)).
- **Notice of intent:** CBP Form 7553 at least **5 working days** before
  return to CBP custody (§ 190.42(c)), unless prior notice is waived
  (§ 190.91); for destruction, **7 working days** before (§ 190.71).
- **Proof of export by mail:** official postal records describing the
  shipment, identified on the drawback entry and retained (§§ 190.72(a)(3),
  190.74).
- **Designating the import:** the drawback entry names each **import entry
  number and line item** (§ 190.51(a)(2)(viii)). An ET13 filing is an ACE
  entry with an entry number. The bundle does not document whether an IMDW
  worksheet line yields an entry number that ACE drawback can designate —
  check before relying on drawback for IMDW-entered mail.

# Citations

[1] [eCFR Title 19 — §§ 145.4, 145.5, 145.21–145.25, 145.71, 145.72, 158.45, Part 190](/sources/ecfr-title-19.md)
[2] [IFR — mail de minimis suspension & postal informal entry (FR 2026-12669)](/sources/ifr-mail-de-minimis.md)
[3] [General notice — Entry Type 13 test (FR 2026-12668)](/sources/notice-entry-type-13.md)
[4] [CBP Global Guidance for International Mail (CSMS # 69183472)](/sources/cbp-global-guidance-international-mail.md)
[5] [ACE Error Dictionary — Entry Summary, v54 (B49)](/sources/catair-entry-summary-error-dictionary.md)
[6] [NPRM — Low-Value Shipments (FR 2026-20650)](/sources/nprm-low-value-shipments.md)
