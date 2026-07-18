---
type: Overview
title: ABI & CATAIR — the Technical Filing Layer
description: How electronic filing into ACE actually works — the Automated Broker Interface, the CATAIR document set (chapters, appendices, business rules, error dictionaries), and how to track versions.
tags: [abi, catair, ace, edi, orientation]
timestamp: 2026-07-03T23:59:00Z
---

The **Automated Broker Interface (ABI)** is the EDI channel through which
filers (brokers, self-filers, service providers) transmit entries, entry
summaries, and related data into ACE. Its specifications are the **CATAIR** —
*CBP and Trade Automated Interface Requirements* — a family of documents CBP
publishes and revises continuously at
[cbp.gov/trade/ace/catair](https://www.cbp.gov/trade/ace/catair). With the
[de minimis suspension](/entry/de-minimis-suspension.md) forcing parcel
volumes into Entry Type 11, formal entry, and the coming
[Entry Type 13](/entry/entry-type-13-test.md), this technical layer is now
load-bearing for ecommerce logistics — this area of the bundle holds the
CATAIR documents that matter for that traffic and distills what each governs.

# How the Document Set Is Organized

| Kind | What it is | Examples in this bundle |
|------|-----------|------------------------|
| **Chapters** | Record-by-record formats for one transaction type (input + response) | [Cargo Release (SE)](/ace-filing/cargo-release.md), [Entry Summary (AE/AX)](/ace-filing/entry-summary-filing.md), [In-Bond (QP)](/ace-filing/in-bond-filing.md), [Reconciliation (RE)](/ace-filing/reconciliation.md), [eBond (CB/CX)](/ace-filing/ebond-filing.md), [ISF](/ace-filing/importer-security-filing.md), [5106 / MID](/ace-filing/importer-manufacturer-ids.md), [statements](/ace-filing/statements-duty-payment.md) |
| **Appendices** | Cross-chapter code tables and reference algorithms | [Appendices B–V](/ace-filing/catair-reference-appendices.md), [Appendix PGA](/sources/catair-appendix-pga.md) |
| **Business-rules documents** | Process-level companions to the record formats | [Cargo Release Business Rules v4.0](/sources/catair-cargo-release-business-rules.md), ESBP ([v12.0](/sources/ace-esbp-v12.md)) |
| **Error dictionaries / validation rules** | What a reject code means and why it fired | [SE input validation rules](/sources/catair-cargo-release-validation-rules.md), [entry summary error dictionary](/sources/catair-entry-summary-error-dictionary.md), [PGA error dictionary](/sources/pga-error-dictionary.md), [Appendix T (in-bond)](/sources/catair-appendix-t-in-bond-errors.md) |
| **PGA implementation guides** | Agency-specific usage of the PGA Message Set | [CPSC eFiling IG](/ace-filing/cpsc-efiling.md) |

# Reading CATAIR Documents — Quirks That Confuse

- **Publication numbers:** most CATAIR documents carry Pub # 0875-0419;
  [Appendix B](/sources/catair-appendix-b-valid-codes.md) carries
  Pub # 3913-1124. Neither number distinguishes versions.
- **The eternal DRAFT footer:** many chapters state they are "considered
  final" yet retain a DRAFT footer "until an official OPA publication number
  has been assigned" — DRAFT in the footer does **not** mean the document is
  inoperative.
- **Version discovery:** the CATAIR page lists each chapter with its current
  production version, and a separate table of **published-but-not-deployed
  revisions** with target production dates. A newer PDF being posted does not
  mean ACE accepts it yet — see the
  [rev 108 vs rev 109 situation](/ace-filing/entry-summary-filing.md) for the
  entry summary chapter. CBP also posts a notional
  [ACE Development and Deployment Schedule](https://www.cbp.gov/document/guidance/ace-development-and-deployment-schedule),
  refreshed periodically and announced via CSMS — target dates there slip
  (the "Inactive for Entry Purposes" status moved 07-14 → 07-16), so treat
  deployment CSMS messages, not the schedule, as the ground truth.
- **Point-in-time copies:** the local files here are snapshots with "as of"
  dates in their [source stubs](/sources/index.md); CBP revises in place, so
  verify against the CATAIR page before relying on record-level details.

# What This Area Covers

* [Cargo Release Filing (SE)](/ace-filing/cargo-release.md)
* [Entry Summary Filing (AE/AX)](/ace-filing/entry-summary-filing.md)
* [In-Bond Filing (QP)](/ace-filing/in-bond-filing.md)
* [Statements & Duty Payment](/ace-filing/statements-duty-payment.md)
* [Reconciliation Filing](/ace-filing/reconciliation.md)
* [eBond Filing](/ace-filing/ebond-filing.md)
* [Importer & Manufacturer Identity Filing](/ace-filing/importer-manufacturer-ids.md)
* [Importer Security Filing](/ace-filing/importer-security-filing.md)
* [PGA Message Set Filing](/ace-filing/pga-message-set.md)
* [CPSC eFiling](/ace-filing/cpsc-efiling.md)
* [CATAIR Reference Appendices](/ace-filing/catair-reference-appendices.md)

The business-process view of the same machinery lives in
[Entry Summary in ACE](/entry/entry-summary-ace.md); systems context in the
[US Import System Overview](/overview.md).

# Citations

[1] [CBP CATAIR page](https://www.cbp.gov/trade/ace/catair) — current versions and deployment schedule
[2] [Entry Summary Create/Update rev 108](/sources/catair-entry-summary-ae-ax-rev-108.md)
[3] [ACE Cargo Release (SE) chapter v40](/sources/catair-cargo-release-se.md)
[4] [PGA Message Set rev 28](/sources/catair-pga-message-set.md)
