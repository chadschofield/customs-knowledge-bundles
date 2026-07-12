---
type: Regulatory Change
title: Tariff Actions 2025–2026
description: IEEPA tariffs struck down (Feb 2026) and now being refunded via CAPE, the temporary 10% Section 122 surcharge expiring ~2026-07-24, and the live Section 232 metals duties (Proclamation 11021).
tags: [tariffs, ieepa, section-122, section-301, section-232, regulatory-change]
timestamp: 2026-07-12T20:00:00Z
---

> **Volatility warning (as of 2026-07-12).** This is the fastest-moving topic
> in the bundle. The Section 122 surcharge expires ~2026-07-24, Section 232
> metals duties are live and still being adjusted, and IEEPA refunds are mid-
> rollout. Verify against current Federal Register notices, CBP CSMS messages,
> and the latest [HTS revision](/tariff/hts.md) before quoting rates.

# How We Got Here

| Date | Action | Effect |
|------|--------|--------|
| 2025 (from Feb) | IEEPA tariff EOs (14193/14194/14195/14200/14226/14227/14228/14257…) with stacking rules in EO 14289 | Country-based ad valorem tariffs on top of HTS column 1 rates; EO 14324's postal duty methods referenced these IEEPA rates. |
| 2026-02-20 | ***Learning Resources, Inc. v. Trump***, 607 U.S. ___ (2026), 6–3 | IEEPA **does not authorize tariffs**; IEEPA-based tariff programs invalidated. |
| 2026-02-20 | **EO 14388** | Keeps the [de minimis suspension](/entry/de-minimis-suspension.md) alive independent of the tariff ruling. |
| 2026-02-20 → 2026-02-24 | **Proclamation 11012** (Section 122, Trade Act of 1974) | Temporary **10% global ad valorem surcharge** — the statute allows max 15% for max **150 days** without Congress. |
| 2026-03/04 | CIT orders in *Atmus Filtration* and *Euro-Notions* | CBP must liquidate/reliquidate IEEPA entries **without** the duties — refunds now flow through the **[CAPE tool](/tariff/ieepa-refunds-cape.md)**. |
| **2026-04-02 → 2026-04-06** | **Proclamation 11021** (Section 232, 19 U.S.C. 1862) | **10–50% duties on aluminum, steel, and copper** articles and derivatives from all countries — the successor regime, already live (see below). |
| ~**2026-07-24** | Section 122 authority lapses | Surcharge expires — the same day the [postal IMDW process](/entry/postal-informal-entry-imdw.md) begins (designed for duty parity when it does). |

# The Successor Regime Is Arriving

The expected shift to authorities with **no statutory expiration** is now
happening — assessed per **HTSUS line via Chapter 99 secondary
classifications**, not as a flat surcharge, so 10-digit
[classification accuracy](/tariff/hts.md) directly determines duty cost:

- **Section 232** (national security) — **live**. Proclamation 11021
  (2026-04-02, effective 2026-04-06) imposes **10–50% duties on aluminum,
  steel, and copper** articles and derivatives from all countries; a
  multi-metal good pays only one rate, and non-metal derivative value can be
  excluded. Annex IV received **technical corrections** (2026-04-29). Also
  extended to **medium/heavy-duty vehicles and auto parts** and modified for
  certain **Taiwan** aircraft/auto/wood products (Trade & Security Agreement,
  effective 2026-05-01). Covered HTS lists and filing detail:
  [Section 232 metals source](/sources/csms-section-232-metals.md).
- **Section 301** (unfair trade practices) — country/product-specific lists,
  historically China-focused; Large Civil Aircraft lines refreshed in 2026
  HSUs.
- **Section 201** (safeguards) — product-specific, time-limited.

These changes reach ACE through **Harmonized System Updates (HSUs)** — see
[HTS](/tariff/hts.md); the bundle's HTS JSON refresh absorbs the resulting
record changes.

# Operational Guidance

- Rate quoting: the applicable rate is the one in effect **when the entry is
  transmitted** (19 U.S.C. 1315(a)(1)) — batching/timing decisions around
  2026-07-24 have real duty consequences.
- Postal parity: through 2026-07-23 mail pays only the Section 122 surcharge;
  from 2026-07-24 it pays **all applicable duties** like commercial cargo.
- Monitor: Federal Register (presidential documents, USTR/Commerce notices),
  CBP CSMS, and [HTS revisions](/tariff/hts.md); update this concept and
  [De Minimis Suspension](/entry/de-minimis-suspension.md) as the successor
  regime lands.

Refunds of the invalidated IEEPA duties are their own operational track —
see [IEEPA Duty Refunds & the CAPE Tool](/tariff/ieepa-refunds-cape.md).

# Citations

[1] [Internal report — US Customs Shipment Regulation Changes (timeline & Section 122 analysis)](/sources/report-regulation-changes.md)
[2] [IFR — mail de minimis suspension (Section 122 context, 10% rate)](/sources/ifr-mail-de-minimis.md)
[3] [EO 14324 — IEEPA-era postal duty methods (superseded)](/sources/eo-14324.md)
[4] [Section 232 Metals Guidance + HTS Lists (Proclamation 11021)](/sources/csms-section-232-metals.md)
[5] [IEEPA Duty Refunds & the CAPE Tool](/tariff/ieepa-refunds-cape.md)
