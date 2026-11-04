---
type: Process
title: Importer & Manufacturer Identity Filing (5106 / MID)
description: Creating and updating the identity records entries depend on — importer/consignee (CBP Form 5106) records and manufacturer (MID) records via ABI.
tags: [5106, mid, importer-of-record, consignee, manufacturer, abi, catair, process]
timestamp: 2026-11-04T21:00:00Z
---

Two identity files in ACE underpin every entry: the **Importer/Consignee
File** (who is importing — the CBP Form 5106 data) and the **Manufacturer
File** (who made the goods — the MID). Both are maintained through ABI, and
an entry naming a party without a valid record rejects.

# Importer/Consignee (5106)

- **[Importer/Consignee Create/Update chapter, v12](/sources/catair-importer-consignee-5106.md)**
  (2019-03-13 edition) — record layouts to add or update name, address, and
  identity data; this is the electronic CBP Form 5106.
- **[5106 Appendix C — postal code requirements](/sources/catair-5106-appendix-c-zip-codes.md)**
  (XLSX) — per-country rules for whether and in what format a postal code is
  required on the record.
- The importer-of-record number this establishes is a **prerequisite to
  filing** — see [Right to Make Entry](/entry/right-to-make-entry.md). CBP
  deactivating an IOR now surfaces as cargo-release error 333
  ([Cargo Release Filing](/ace-filing/cargo-release.md)), and
  [EO 14411](/enforcement/eo-14411-enforcement.md) directs tighter vetting of
  exactly these records for foreign importers.
- **Accuracy is enforced by voiding (from 2026-09-18).** CBP voids IOR
  numbers with inaccurate 5106 data
  ([91 FR 53627](/sources/notice-ior-data-accuracy.md)). Software that
  creates 5106 records should never default the address, email or phone to
  the broker's or forwarder's details. It needs the IOR's own data and a
  direct POA.

# Manufacturer (MID)

- **[Add Manufacturer Name & Address chapter, v3.0](/sources/catair-add-manufacturer-mid.md)**
  (March 2023) — record formats to add a manufacturer (which constructs the
  **Manufacturer Identification Code**) and update an existing manufacturer's
  postal code.
- MIDs are required on entry summary lines and several PGA filings; for
  parcel consolidations the volume of distinct manufacturers makes automated
  MID creation part of the filing pipeline.
- **The MID may be replaced.** The EO 14411
  [supply-chain ANPRM](/sources/anprm-supply-chain-visibility.md) (comments
  close 2026-12-01) calls the MID non-unique and too late in the process. It
  asks whether to replace it with full manufacturer, shipper and exporter
  identity, mandatory Global Business Identifiers, or foreign tax IDs,
  provided at entry and possibly on the manifest.

# Citations

[1] [Importer/Consignee Create/Update (5106), v12](/sources/catair-importer-consignee-5106.md)
[2] [5106 Appendix C — Zip Codes](/sources/catair-5106-appendix-c-zip-codes.md)
[3] [Add Manufacturer Name & Address (MID), v3.0](/sources/catair-add-manufacturer-mid.md)
[4] [Notice — Accuracy of IOR data submitted to CBP (FR 2026-16911)](/sources/notice-ior-data-accuracy.md)
[5] [ANPRM — Heightened Import Disclosures for Supply Chain Visibility (FR 2026-17926)](/sources/anprm-supply-chain-visibility.md)
