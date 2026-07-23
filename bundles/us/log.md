# US Bundle Update Log

## 2026-07-23

* **Triage**: Worked the 7-message CSMS queue (2026-07-20 → 07-23). **Section 301 goes live on Brazil**: 25% on all Brazil products effective 2026-07-22 (91 FR 45516; heading 9903.05.01, in-transit exemption window closing with entries 2026-07-29) — [Tariff Actions](/tariff/tariff-actions-2025-2026.md) updated and the exemption HTS list archived as a [source](/sources/csms-section-301-brazil.md). **ET13 implementation confirmed**: INT-057/CBP-290 deploy to CERT 2026-07-24 and PROD 2026-09-22, with draft implementation guides posted — new "Implementation in ACE" section in [Entry Type 13 Test](/entry/entry-type-13-test.md). HSU 2616 absorbed (carries the Brazil records). Dismissed three cotton TRQ quota bulletins and added "quota bulletin" to the feed deny list.

## 2026-07-20

* **Update**: Auto-refreshed the eCFR Title 19 XML to point-in-time 2026-07-16 (latest amendment 2026-06-24).

## 2026-07-18

* **Triage**: Worked the 7-message CSMS queue from the repaired feed (2026-07-13 → 07-17). IOR auto-deactivation reconciled to its actual deployment — "Inactive for Entry Purposes" live **2026-07-16** (366-day rule, 19 CFR 24.5(e); non-entry functions unaffected) — in [Right to Make Entry](/entry/right-to-make-entry.md) and [EO 14411](/enforcement/eo-14411-enforcement.md). [Entry Summary Filing](/ace-filing/entry-summary-filing.md) gains the **copper smelt & cast reporting** requirement (effective 2026-07-30) and the **F866/F861** auto-parts offset-license validations (2026-07-18); [CPSC eFiling](/ace-filing/cpsc-efiling.md) notes its CP1/CP2 flags loaded via HSU 2615. Dismissed: FWS shellfish flag relaxation (out of scope), deployment-schedule pointer (link added to [ABI & CATAIR overview](/ace-filing/abi-catair-overview.md) instead).
* **Update**: Rolled the entry summary **ACE Error Dictionary to v51** (2026-07-17, fetched from cbp.gov) — v50 marked deployed 2026-07-16 and superseded; version history table added to the [source stub](/sources/catair-entry-summary-error-dictionary.md).

## 2026-07-12

* **Update**: Auto-refreshed the eCFR Title 19 XML to point-in-time 2026-07-09 (latest amendment 2026-06-24).

* **Creation**: Built the CSMS ingestion pipeline — `scripts/check_csms.py` polls the self-hosted email→RSS feed weekly, filters titles via `scripts/csms-filters.json` (maintenance/CERT/webinar noise dropped), downloads attachments, and queues survivors privately for triage. Backfilled 50 messages (2026-04 → 2026-07): 2 dropped, 48 queued.
* **Creation**: Added [Regulatory Watch](/regulatory-watch.md) — a rolling, newest-first record of operative CSMS/regulatory announcements, distinct from this log (world changes vs bundle changes).
* **Creation**: First CSMS triage — archived [CBP Global Guidance for International Mail + the official IMDW template](/sources/cbp-global-guidance-international-mail.md) (CSMS # 69183472, 2026-07-08) and cited it from [Postal Informal Entry (IMDW)](/entry/postal-informal-entry-imdw.md).
* **Triage**: Worked the full 47-message CSMS backlog (2026-04 → 2026-07). New concepts: [IEEPA Duty Refunds & the CAPE Tool](/tariff/ieepa-refunds-cape.md) and [Forced Labor Enforcement](/enforcement/forced-labor.md). Updated [Tariff Actions](/tariff/tariff-actions-2025-2026.md) (Section 232 metals Proclamation 11021, now live; IEEPA refund mandate), [HTS](/tariff/hts.md) (HSU mechanism), [CPSC eFiling](/ace-filing/cpsc-efiling.md) (live 07-08, advisory-only), [PGA Message Set](/ace-filing/pga-message-set.md), [Entry Summary Filing](/ace-filing/entry-summary-filing.md) (CAPE errors 864/liq code 36), [Right to Make Entry](/entry/right-to-make-entry.md) + [EO 14411](/enforcement/eo-14411-enforcement.md) (IOR deactivation). Archived the [Section 232 metals HTS lists](/sources/csms-section-232-metals.md). Populated [Regulatory Watch](/regulatory-watch.md); dismissed routine items (HSUs absorbed by the HTS pipeline, out-of-scope PGA/export/drawback/portal notices).

## 2026-07-03

* **Initialization**: Created the US customs bundle — concepts covering entry pathways, the de minimis suspension, postal informal entry (IMDW), the Entry Type 13 test, entry summary in ACE, right to make entry, bonds, HTS, 2025–2026 tariff actions, customs valuation, EO 14411 enforcement, and 19 CFR.
* **Creation**: Imported 13 primary source documents into [sources](/sources/index.md) (Federal Register EOs and IFRs, CBP directives and ACE guides, HTS 2026 Rev 11, Valuation Encyclopedia, two analysis reports).
* **Update**: Downloaded eCFR Title 19 full-text XML, point-in-time 2026-07-01 (latest amendment 2026-06-24) via the eCFR Versioner API — see [eCFR Title 19 source](/sources/ecfr-title-19.md).
* **Update**: Downloaded the HTS current-release JSON export (2026 Revision 11) via the USITC `reststop` API — see [HTS source](/sources/hts.md).
* **Update**: Removed the trade-press article source (secondary analysis, member content); its factual content is fully covered by the [mail IFR](/sources/ifr-mail-de-minimis.md) — the bundle favors official primary documentation.
* **Update**: Adopted a latest-only policy for the HTS PDF: renamed to `sources/files/hts-current.pdf`, replaced in place per revision; prior editions live in git history and the USITC archive.
* **Update**: Refreshed the [internal report](/sources/report-regulation-changes.md) with a BoxC copyright-notice footer marking internal authorship — the convention for internally authored documents going forward.
* **Creation**: Added [CROSS — Customs Rulings](/regulations/cross-rulings.md) (legal force, verified JSON API, search strategy), a ruling-citation convention, and `scripts/check_rulings.py` — the weekly workflow now re-verifies every cited ruling and fails on revocations.
* **Creation**: Imported 39 CBP ACE ABI CATAIR source documents into [sources](/sources/index.md) — transaction chapters (cargo release SE v40, entry summary AE/AX rev 108 + pending rev 109, reconciliation, eBond, statements, 5106/MID, ISF), the PGA filing set (message set rev 28, Appendix PGA, error dictionary v16, flag enforcement tables, prior notice, corrections), CPSC eFiling IGs (v2.5 current + v2.3 superseded), and eleven general appendices. All are official CBP publications; every stub's `resource:` is a verified cbp.gov landing page.
* **Creation**: Added the [ACE Filing (ABI/CATAIR)](/ace-filing/abi-catair-overview.md) concept area — 11 concepts distilling the technical filing layer (cargo release, entry summary AE/AX, statements, reconciliation, eBond, 5106/MID, ISF, PGA message set, CPSC eFiling, reference appendices) — and cross-linked it from the overview, entry summary, and bonds concepts.
* **Update**: Time-sensitive facts recorded from CBP's CATAIR deployment schedule (as of 2026-07-03): CPSC eFiling v2.5 and the draft PGA flag enforcement table deploy to production **2026-07-08**; entry summary AE/AX rev 109 is published with deployment TBD (rev 108 remains production).
* **Creation**: Filled the gaps the CATAIR intake surfaced — fetched from cbp.gov and imported the [In-Bond chapter (Amendment 51)](/sources/catair-in-bond.md) with a new [In-Bond Filing](/ace-filing/in-bond-filing.md) concept, and the entry summary [ACE Error Dictionary v49](/sources/catair-entry-summary-error-dictionary.md) plus [draft v50](/sources/catair-entry-summary-error-dictionary-v50-draft.md) (deploys **2026-07-14**; adds error 875, the entry-summary counterpart of cargo-release reject 333).
