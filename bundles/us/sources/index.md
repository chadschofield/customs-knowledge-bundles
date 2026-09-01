# Sources

Primary documents backing this bundle. Each stub records provenance and links
the local copy in [files/](files/) plus the canonical URL. Auto-refreshed
files (`ecfr-title-19.xml`, `hts-current.json`) keep stable names — versions
live in git history and [source-state.json](source-state.json).

# Executive & Regulatory Actions

* [EO 14324 — Suspending Duty-Free De Minimis for All Countries](eo-14324.md) - Signed 2025-07-30, effective 2025-08-29; FR Doc 2025-14897.
* [EO 14411 — Strengthening Customs Enforcement](eo-14411.md) - Signed 2026-06-03; FR Doc 2026-11595.
* [IFR — Mail De Minimis Suspension & Postal Informal Entry](ifr-mail-de-minimis.md) - FR Doc 2026-12669, published 2026-06-24.
* [IFR — Non-Postal De Minimis Suspension](ifr-non-postal-de-minimis.md) - FR Doc 2026-12670, published & effective 2026-06-24.
* [General Notice — Entry Type 13 Test](notice-entry-type-13.md) - FR Doc 2026-12668, published 2026-06-24; test from 2026-09-22.

# CBP Operational Guidance

* [Customs Directive 3530-002A — Right to Make Entry](customs-directive-3530-002a.md) - 2001 directive on Section 484 entry rights.
* [ACE Entry Summary Business Rules & Process v12.0](ace-esbp-v12.md) - CBP Pub. 3499-1223, December 2023.
* [ACE Entry Summary Business Rules & Process v11.0](ace-esbp-v11.md) - Superseded edition, retained for diffing.
* [ACE Entry Summary Instructions v2.4a](ace-entry-summary-instructions.md) - Field-level 7501-in-ACE guidance, 2016.

# CSMS Announcements

* [CBP Global Guidance for International Mail + IMDW Template](cbp-global-guidance-international-mail.md) - CSMS # 69183472 (2026-07-08): operational guidance and the official worksheet for the postal informal entry process effective 2026-07-24.
* [Section 232 Metals Guidance + HTS Lists (Proclamation 11021)](csms-section-232-metals.md) - CSMS # 68253075 / # 68554727: the 10–50% aluminum/steel/copper duties effective 2026-04-06, with covered-HTS lists.
* [Section 301 Brazil Guidance + Exemption HTS List](csms-section-301-brazil.md) - CSMS # 69302472: 25% on products of Brazil effective 2026-07-22, with the exempted-classifications list.
* [Section 301 Forced Labor Guidance + HTS List](csms-section-301-forced-labor.md) - CSMS # 69326983: 10%–12.5% on imports from 60 economies effective 2026-07-24, with the covered-classifications list.
* [Section 232 Pharmaceuticals Guidance + HTS List](csms-section-232-pharmaceuticals.md) - CSMS # 69395344 / # 69415934: up to 100% on patented pharmaceuticals from 2026-07-31 (all other companies 2026-09-29), with the covered-classifications list.
* [Section 338 Canada Guidance + HTS List](csms-section-338-canada.md) - CSMS # 69606660: 50% on certain goods of Canada via 9903.03.12–.16, applying to entries from 2026-08-22, with the covered-classifications list.

Other operative CSMS messages are cited directly in the concepts they
support (see [Regulatory Watch](/regulatory-watch.md)); only messages whose
attachments or standalone guidance are archived locally get a stub here.

# ACE ABI CATAIR — Chapters

* [Cargo Release (SE), v40](catair-cargo-release-se.md) - Release record formats incl. the combined ISF + release dataset, 2025-07-01.
* [Cargo Release Business Rules, draft v4.0](catair-cargo-release-business-rules.md) - Process companion to the SE chapter, 2025-03-17.
* [Cargo Release (SE) Input Validation Rules](catair-cargo-release-validation-rules.md) - Error/condition codes; 2026-06-24 added the importer-inactive reject.
* [Entry Summary Create/Update (AE/AX), rev 108](catair-entry-summary-ae-ax-rev-108.md) - Production version at the time of writing, 2025-11-01.
* [Entry Summary Create/Update (AE/AX), rev 109](catair-entry-summary-ae-ax-rev-109.md) - Published successor, deployment TBD — GBI changes.
* [Entry Summary Status Notification (UC), v30](catair-entry-summary-status-notification-uc.md) - Unsolicited status output records, 2025-06.
* [ACE Error Dictionary — Entry Summary, v52 current](catair-entry-summary-error-dictionary.md) - ~1,000 condition codes with explanations; v52 deployed 2026-08-21, earlier editions retained.
* [ACE Error Dictionary — Entry Summary, v50 draft](catair-entry-summary-error-dictionary-v50-draft.md) - Adds error 875 (importer inactive); deploys 2026-07-14.
* [In-Bond, Amendment 51](catair-in-bond.md) - QP in-bond record formats (IT/T&E/IE movements), 2026-04.
* [Reconciliation Entry Summary Create/Update (RE), v12](catair-reconciliation-re.md) - Entry Type 09 filing, 2025-06.
* [Customs eBond Create/Update (CB/CX), v1.9](catair-ebond-cb-cx.md) - Surety bond filing records, 2020-04-10.
* [Daily Statement, rev 15](catair-daily-statement.md) - Daily duty-payment statements; 2,000-entry cap since 2025-04-23.
* [Periodic Monthly Statement](catair-periodic-monthly-statement.md) - Monthly consolidated duty payment, 2019-03-06.
* [Importer/Consignee Create/Update (5106), v12](catair-importer-consignee-5106.md) - Electronic CBP Form 5106, 2019-03-13.
* [5106 Appendix C — Zip Codes](catair-5106-appendix-c-zip-codes.md) - Per-country postal-code requirements (XLSX), 2019-03-08.
* [Add Manufacturer Name & Address (MID), v3.0](catair-add-manufacturer-mid.md) - Manufacturer record / MID creation, 2023-03.
* [Importer Security Filing (ISF-10/ISF-5), v3](catair-isf.md) - Ocean 10+2 filing records, 2017-07.
* [ISF Status Advisory (SA), v1](catair-isf-status-advisory-sa.md) - ISF processing status output, 2016-08.

# PGA Filing & CPSC eFiling

* [PGA Message Set, rev 28](catair-pga-message-set.md) - PG01–PG60 record layouts and corrections, 2026-04-28.
* [Appendix PGA](catair-appendix-pga.md) - Master PGA code tables, 303 pp., 2026-03-02.
* [PGA Error Dictionary, v16](pga-error-dictionary.md) - ~1,000 P-series reject codes (XLSX), 2026-06-01.
* [PGA Flag Enforcement Table](pga-flag-enforcement-table.md) - Production enforcement matrix (XLSX), 2021-12-15.
* [PGA Flag Enforcement Table — draft](pga-flag-enforcement-table-draft-2026.md) - 2026-04-27 draft, scheduled production 2026-07-08.
* [PGA Data Corrections (CA/CC)](catair-pga-data-corrections-ca-cc.md) - Correcting filed PGA data, 2025-06-20.
* [Stand-alone Prior Notice (PE/PX)](catair-pga-standalone-pe-px.md) - FDA Prior Notice outside an entry, 2018-08-29.
* [Stand-alone Prior Notice Status (PO)](catair-pga-standalone-po.md) - PO output records, 2021-04-06.
* [PGA Status Notification Codes](catair-pga-status-notification-codes.md) - SO70/SO71 & PO70/PO71 status/reason codes, 2023-08-09.
* [ACE Agency Tariff Code Reference](ace-agency-tariff-codes.md) - Tariff-flag rule logic (MUST/MAY, disclaims), 2026-03-04.
* [Appendix V — Government Agency Codes](catair-appendix-v-agency-codes.md) - Three-letter agency codes, 2020-06-08.
* [CPSC eFiling Implementation Guide v2.5](catair-cpsc-efiling-ig-v2.5.md) - Current guide for the 2026-07-08 go-live, 2026-05.
* [CPSC eFiling Implementation Guide v2.3](catair-cpsc-efiling-ig-v2.3.md) - Superseded edition, retained for diffing.

# CATAIR General Appendices

* [Appendix B — Valid Codes](catair-appendix-b-valid-codes.md) - Country/currency and general code tables (Pub # 3913-1124), 2026-03-03.
* [Appendix C — Tariff Abbreviations](catair-appendix-c-tariff-abbreviations.md) - HTS units of measure, 2016-02-22.
* [Appendix D — Metric Conversion](catair-appendix-d-metric-conversion.md) - Inch-pound ↔ metric factors, 2011-04.
* [Appendix E — Valid Entry Numbers](catair-appendix-e-valid-entry-numbers.md) - Entry number format + check digit, 2012-05.
* [Appendix F — Duty Calculation](catair-appendix-f-duty-calculation.md) - Duty computation formulas/codes, 2011-04.
* [Appendix H — Census Warning Overrides](catair-appendix-h-census-overrides.md) - Census warnings and override codes, 2008-05-30.
* [Appendix I — Hold Harmless Agreement](catair-appendix-i-hold-harmless.md) - Model data-release agreement, 2011-04.
* [Appendix N — Disposition Codes](catair-appendix-n-disposition-codes.md) - Cargo status disposition codes, 2023-06.
* [Appendix R — Intended Use Codes](catair-appendix-r-intended-use-codes.md) - PGA intended-use codes, 2022-11-23.
* [Appendix S — ISF Error Codes](catair-appendix-s-isf-error-codes.md) - ISF reject codes, 2012-10.
* [Appendix T — In-bond Common Errors](catair-appendix-t-in-bond-errors.md) - QP/WP error dictionary, 2025-09.

# Tariff, Valuation & Regulations

* [HTS — current edition](hts.md) - Latest-only PDF + JSON export under stable filenames; the stub names the current release and PDF publication number.
* [CBP Valuation Encyclopedia (1980–2021)](valuation-encyclopedia.md) - Compendium of valuation rulings and policy.
* [eCFR Title 19 — full text XML](ecfr-title-19.md) - Point-in-time 2026-07-01, refreshed by script.

# Analysis & Internal Reports

* [Internal report — US Customs Shipment Regulation Changes](report-regulation-changes.md) - BoxC employee guide to the 2025–2026 transition.
