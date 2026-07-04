---
okf_version: "0.1"
---

# US Customs Knowledge Bundle

United States customs (CBP) regulations and operational knowledge for
cross-border ecommerce and parcel logistics. Knowledge is current as of
**2026-07-03**; the 2025–2026 de minimis suspension and its successor entry
processes are interim rules that change quickly — check
[log.md](log.md) for update history and verify dates against the Federal
Register before relying on them.

# Start Here

* [US Import System Overview](overview.md) - Orientation: agencies, entry lifecycle, systems, and the 2025–2026 low-value entry upheaval.

# Entry

* [Entry Types & Pathways](entry/entry-types.md) - Formal vs informal entry and the entry-type codes that matter for low-value shipments.
* [De Minimis Suspension](entry/de-minimis-suspension.md) - Status, full timeline, surviving exemptions, and the road to statutory repeal on 2027-07-01.
* [Postal Informal Entry (IMDW)](entry/postal-informal-entry-imdw.md) - The mandatory mail entry process effective 2026-07-24: 14-field worksheet, broker filing, bonds, deadlines.
* [Entry Type 13 Test](entry/entry-type-13-test.md) - Voluntary electronic informal mail entry in ACE, starting 2026-09-22.
* [Entry Summary in ACE](entry/entry-summary-ace.md) - CBP Form 7501 data filed in ACE: business process, corrections, liquidation.
* [Right to Make Entry](entry/right-to-make-entry.md) - Who may file entry (owner, purchaser, licensed broker) and importer-of-record rules.
* [Customs Bonds](entry/bonds.md) - Basic importation, carrier, and single-transaction vs continuous bonds — now required for all low-value entry.

# ACE Filing (ABI / CATAIR)

* [ABI & CATAIR Overview](ace-filing/abi-catair-overview.md) - The technical filing layer: how the CATAIR document set works and how to track versions/deployments.
* [Cargo Release Filing (SE)](ace-filing/cargo-release.md) - Release record formats, business rules, and error codes — including the 2026 importer-inactive reject.
* [Entry Summary Filing (AE/AX)](ace-filing/entry-summary-filing.md) - 7501-data record formats: rev 108 in production, rev 109 pending; status notifications; error dictionary; census overrides.
* [In-Bond Filing (QP)](ace-filing/in-bond-filing.md) - Moving merchandise under bond without entry: IT/T&E/IE transactions and their error dictionary.
* [Statements & Duty Payment](ace-filing/statements-duty-payment.md) - Daily and periodic monthly statements, and the de-minimis-driven 2,000-entry cap.
* [Reconciliation Filing (RE)](ace-filing/reconciliation.md) - Entry Type 09 reconciliation of estimated value/classification/FTA elements.
* [eBond Filing (CB/CX)](ace-filing/ebond-filing.md) - How sureties put bonds on file in ACE.
* [Importer & Manufacturer Identity Filing (5106 / MID)](ace-filing/importer-manufacturer-ids.md) - The importer/consignee and manufacturer records entries depend on.
* [Importer Security Filing (ISF 10+2)](ace-filing/importer-security-filing.md) - Ocean security filing and its status/error machinery.
* [PGA Message Set Filing](ace-filing/pga-message-set.md) - Agency data with entries: PG records, tariff flags, enforcement matrix, error dictionary.
* [CPSC eFiling](ace-filing/cpsc-efiling.md) - Consumer-product certificate data mandatory in ACE production 2026-07-08.
* [CATAIR Reference Appendices](ace-filing/catair-reference-appendices.md) - Valid codes, entry numbers, duty calculation, and other cross-chapter tables.

# Tariff

* [Harmonized Tariff Schedule (HTS)](tariff/hts.md) - Structure, revision cadence, machine-readable access, and why 10-digit classification is now unavoidable.
* [Tariff Actions 2025–2026](tariff/tariff-actions-2025-2026.md) - IEEPA tariffs struck down, the Section 122 surcharge, and the expected shift to Section 301/232.

# Valuation

* [Customs Valuation](valuation/customs-valuation.md) - Appraisement methods under 19 U.S.C. 1401a and the CBP Valuation Encyclopedia.

# Enforcement

* [EO 14411 Customs Enforcement Overhaul](enforcement/eo-14411-enforcement.md) - Foreign-IOR restrictions, penalty floors, disclosure mandates, and implementation deadlines.

# Regulations

* [19 CFR — Customs Duties](regulations/cfr-title-19.md) - The customs regulations themselves: structure, key parts, and the local full-text copy.
* [CROSS — Customs Rulings](regulations/cross-rulings.md) - Binding rulings on classification, valuation, and origin — how to search them and cite them so revocations are caught.

# Sources

* [Source Documents](sources/index.md) - Primary documents backing this bundle, with local copies in `sources/files/`.
