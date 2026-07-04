---
type: Process
title: Cargo Release Filing (SE)
description: The ACE Cargo Release (SE) transaction — record formats, business rules, the combined ISF + release dataset, validation/error codes, and disposition codes.
tags: [cargo-release, se, abi, catair, entry, process]
timestamp: 2026-07-03T23:59:00Z
---

**ACE Cargo Release** (transaction **SE**, formerly "Simplified Entry") is
how release data — the CBP Form 3461 equivalent — is filed electronically for
step 2 of the [entry lifecycle](/overview.md). Every non-postal low-value
shipment that used to ride de minimis now needs a release filing
([Entry Type 11 or 01](/entry/entry-types.md)), which makes the SE dataset
the front door for parcel traffic.

# Governing Documents (all in this bundle)

- **[Cargo Release (SE) chapter, v40](/sources/catair-cargo-release-se.md)**
  (2025-07-01 at the time of writing) — record formats and syntax, including
  filing a **single dataset that satisfies both ISF and cargo release**
  requirements for ocean shipments (see
  [Importer Security Filing](/ace-filing/importer-security-filing.md)).
- **[ACR Business Rules and Process Document v4.0 draft](/sources/catair-cargo-release-business-rules.md)**
  (2025-03-17) — the process-level companion: lifecycle, statuses, and
  trade-facing rules.
- **[SE Input Validation Rules](/sources/catair-cargo-release-validation-rules.md)** —
  the condition/error codes a filing can reject with.
- **[Appendix N — Disposition Codes](/sources/catair-appendix-n-disposition-codes.md)**
  (2023-06) — codes carried on cargo status notifications (release, hold,
  exam, AMS/FTZ closures).

# Enforcement Is Now Visible in the Error Codes

The validation rules were updated **2026-06-24** to add error
**333 – IMPORTER OF RECORD INACTIVE FOR ENTRY** — plumbing for the 2025–2026
importer-of-record tightening under
[EO 14411](/enforcement/eo-14411-enforcement.md) and the
[right-to-make-entry rules](/entry/right-to-make-entry.md): a release filing
naming a deactivated IOR now rejects at the gate. The same update retired a
set of dormant codes (098, 119, 207, 209, 223, 242, …).

# Operational Notes

- PGA data rides the same filing via the
  [PGA Message Set](/ace-filing/pga-message-set.md); whether a given agency's
  tariff flag blocks release depends on the flag-enforcement matrix there.
- Release is followed within 10 working days by the
  [entry summary filing](/ace-filing/entry-summary-filing.md) and secured by a
  [bond](/entry/bonds.md).
- Version and edition dates are volatile — the source stubs above carry the
  point-in-time copies; check the CATAIR page before relying on record-level
  formats.

# Citations

[1] [ACE Cargo Release (SE) chapter v40](/sources/catair-cargo-release-se.md)
[2] [ACR Business Rules and Process Document for Trade, draft v4.0](/sources/catair-cargo-release-business-rules.md)
[3] [SE Input Validation Rules (2026-06-24)](/sources/catair-cargo-release-validation-rules.md)
[4] [Appendix N — Disposition Codes](/sources/catair-appendix-n-disposition-codes.md)
