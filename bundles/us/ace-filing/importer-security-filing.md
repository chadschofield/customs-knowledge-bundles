---
type: Process
title: Importer Security Filing (ISF 10+2)
description: The ocean-cargo security filing — ISF-10 and ISF-5 record formats, status advisories, and error codes; and the combined ISF + cargo release dataset.
tags: [isf, 10+2, ocean, security-filing, abi, catair, process]
timestamp: 2026-07-03T23:59:00Z
---

The **Importer Security Filing ("10+2")** is the pre-arrival security data
CBP requires for **ocean** shipments: **ISF-10** (ten data elements) for
cargo entering the US, **ISF-5** for FROB and T&E/IE movements. It is filed
no later than 24 hours before lading and is separate from entry — though it
can be satisfied in the same transmission as cargo release.

# Governing Documents (all in this bundle)

- **[ISF (ISF-10 / ISF-5) chapter, v3](/sources/catair-isf.md)** (July 2017
  at the time of writing) — transaction processing, loop definitions, and
  record formats for both filing types.
- **[ISF Status Advisory (SA), v1](/sources/catair-isf-status-advisory-sa.md)**
  (2016-08) — SA-series output records reporting the status of a submitted
  ISF.
- **[Appendix S — ISF Error Codes](/sources/catair-appendix-s-isf-error-codes.md)**
  (2012-10) — reject codes and the rules that trigger them.

# The Combined Filing Path

The [Cargo Release (SE) chapter](/ace-filing/cargo-release.md) supports a
**single dataset satisfying both ISF and cargo release** — the practical
route when a broker controls both filings. Ocean matters for parcel logistics
wherever consolidated ecommerce freight moves by sea; air parcel traffic is
outside ISF (air security data rides ACAS at the carrier level — see the
[entry lifecycle](/overview.md)).

# Citations

[1] [Importer Security Filing (ISF-10/ISF-5), v3](/sources/catair-isf.md)
[2] [ISF Status Advisory (SA), v1](/sources/catair-isf-status-advisory-sa.md)
[3] [Appendix S — ISF Error Codes](/sources/catair-appendix-s-isf-error-codes.md)
[4] [ACE Cargo Release (SE) chapter v40](/sources/catair-cargo-release-se.md)
