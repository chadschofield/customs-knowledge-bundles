---
type: Reference
title: CROSS — Customs Rulings
description: CBP's database of binding ruling letters (classification, valuation, origin) — legal force, the CROSS API and its reCAPTCHA-gated search, the AMCROSS mirror for programmatic search, search strategy, and the citation convention this bundle enforces.
resource: https://rulings.cbp.gov/
tags: [rulings, cross, amcross, classification, valuation, origin, precedent]
timestamp: 2026-11-12T17:00:00Z
---

**CROSS** (Customs Rulings Online Search System, [rulings.cbp.gov](https://rulings.cbp.gov/))
is CBP's public database of binding ruling letters from 1989 to the present —
tariff classification (most of the corpus), valuation, country of origin and
marking, and trade-program eligibility. When a classification, valuation, or
origin question has a non-obvious answer, a ruling on near-identical facts is
often the fastest authoritative resolution.

# Legal Force (19 CFR Part 177)

- A ruling letter is **binding on CBP** for the transaction and party it was
  issued to, and represents CBP's official position for **identical
  merchandise and facts** — brokers and importers rely on rulings for
  classification certainty.
- A ruling that has been in effect **60+ days** can only be modified or
  revoked through notice-and-comment in the **Customs Bulletin**
  (19 U.S.C. 1625(c)), taking effect 60 days after the final notice — so
  revocations are visible, published events.
- Rulings are administrative precedent, not case law; courts (CIT, CAFC) can
  override them.

# NY vs HQ Rulings

| Collection | Issuer | Typical subject |
|------------|--------|-----------------|
| **NY** (e.g. N360170) | National Commodity Specialist Division, New York | Prospective classification, origin, marking — the everyday workhorse; requested via [eRulings](https://erulings.cbp.gov/), ~30-day turnaround |
| **HQ** (e.g. H336180) | Regulations & Rulings, Headquarters | Valuation, carrier matters, complex/policy questions, internal advice, protest further review, and the modification/revocation of earlier rulings |

# The CBP API (undocumented — may change; access re-verified 2026-11-12)

| Endpoint | Anonymous access (as of 2026-11-12) | Returns |
|----------|-------------------------------------|---------|
| `https://rulings.cbp.gov/api/search?term=<urlencoded>&collection=ALL&pageSize=30&page=1&sortBy=DATE_DESC` | **Gated** — HTTP 403 `Security parameters are missing from this request context.` | `{rulings: […], totalHits: N}` — each record: `rulingNumber`, `subject`, `categories`, `rulingDate`, `collection` (ny/hq), `tariffs`, `relatedRulings`, `modifies`/`modifiedBy`, `revokes`/`revokedBy`, `operationallyRevoked` |
| `https://rulings.cbp.gov/api/ruling/<number>` | Open (404 if no such ruling) | The full ruling: same metadata plus `text` and a short-lived PDF `url`; the link fields (`revokes`, `revokedBy`, `modifies`, `modifiedBy`, `relatedRulings`) come back null |
| `https://rulings.cbp.gov/ruling/<number>` | Open | Human-readable UI page — **the citation link form** |

**Search requires reCAPTCHA (since 2026-11-12).** The web UI loads
`/api/app-config`, which now carries a Google reCAPTCHA `siteKey`, and the
search page's own API calls succeed while direct calls get the 403 above.
Scripts and agents should not try to obtain or replay reCAPTCHA tokens:
search programmatically through AMCROSS (next section)
instead, or use the [CROSS web UI](https://rulings.cbp.gov/search) in a
browser. Single-ruling lookups still work without a token, so CROSS stays
the place to confirm a ruling exists and to read the authoritative text.

# AMCROSS — Searchable Mirror

[AMCROSS](https://amcross.us/) is a search service over the same NY and HQ
ruling letters, built and operated by MetaPhase — **not a CBP or DHS
system**. It reloads from CROSS regularly, reproduces ruling text verbatim
under `text`, and publishes a documented, keyless JSON API
([OpenAPI](https://amcross.us/openapi.yaml)):

| Endpoint (`https://amcross.us/api/v1/…`) | Returns |
|------------------------------------------|---------|
| `search?q=<text>&sort=date_desc` | `{total, results: […]}` — each result: `rulingNumber`, `collection`, `subject`, `category`, `rulingDate`, `status`, `htsCodes`, `sourceUrl`. Filters: `collection` (`ny`/`hq`), `hts-chapter`, `hts-heading`, `hts-code`, `country`, `authority` (e.g. `19 CFR 102.11`), `status`, `program`, `date-from`/`date-to`; `page`, `limit` (≤100) |
| `rulings/<number>` | One ruling: metadata, `htsCodes`, cited `authorities`, its own outbound `relationships`, `text`, and `source` (the CROSS URL it came from) |
| `rulings/<number>/related` | The relationship graph two hops out: `nodes` and `edges` (`from`, `to`, `kind` = `references`/`modifies`/`modified_by`/`revokes`/`revoked_by`, `depth`) |
| `stats` | `rulingCount`, `cbpReportedCount`, `reconciled`, `mostRecentRulingDate`, `lastIngestedAt` |
| `export?…`, `bulk` | Any search as CSV/JSON/XLSX; whole-dataset JSON Lines/CSV |

`q` takes ruling numbers, HTS codes, citations, quoted phrases, and Boolean
in capitals (`OR`, `AND NOT`, leading `-`). Requests are rate-limited per
address — pace scripted calls and back off on HTTP 429.

**Use it with these checks:**

- **Revocation status lives in `/related`, not on the ruling.** As in CROSS,
  relationships are recorded on the revoking ruling: NY N334409's own
  AMCROSS record shows `status: active` and no relationships, while its
  `/related` graph has the edge `H336180 → N334409 revokes` (both left
  unlinked here on purpose, since N334409 is not good law). Look for
  `revokes`/`modifies` edges whose `to` is the ruling.
- **Edges are only as complete as CBP's metadata.** H336180's subject line
  says it revokes NY 817807, but the published edge is only `references`.
  Read the subject and text of any ruling that points at yours.
- **Check freshness.** `stats` reports whether AMCROSS's count matches what
  CBP publishes; on 2026-11-12 it held 222,339 rulings against CBP's 222,344
  (`reconciled: false`). A ruling missing from AMCROSS may still exist in
  CROSS.
- **Confirm in CROSS and cite CROSS.** Before relying on a ruling found
  through AMCROSS, open it at `rulings.cbp.gov/ruling/<number>`, and cite
  that link (see below) — not the AMCROSS page.
- **Ignore generated text.** AMCROSS shows labelled AI overviews and
  "insights"; only the ruling's `text` is CBP's.

`scripts/check_rulings.py` combines the two: CROSS's single-ruling endpoint
for existence (a missing ruling is an ERROR), AMCROSS's `/related` graph for
revocations (ERROR) and modifications (WARN). A ruling AMCROSS does not hold,
or a run where AMCROSS is unreachable, is a WARN ("revocation status
unverified") with a CROSS search link to check by hand.

# Search Strategy

- Combine a product term with an HTS filter (AMCROSS:
  `q="lithium battery"&hts-heading=8507`) to cut noise; `htsCodes`
  (`tariffs` in CROSS) confirms what a ruling actually classified.
- Beware term collisions: "de minimis" in CROSS usually means the **textile
  rules-of-origin tolerance** (19 CFR 102.21) or minor-ingredient doctrines —
  not the Section 321 $800 exemption covered in
  [De Minimis Suspension](/entry/de-minimis-suspension.md).
- Before relying on any ruling, confirm validity through AMCROSS's
  `/related` graph (see the checks above), which also gives the fuller
  precedent chain.
- For valuation fact patterns, start with the
  [Valuation Encyclopedia](/valuation/customs-valuation.md), which digests
  rulings by topic, then pull the current text from CROSS.

# Citation Convention (enforced)

Cite rulings in concepts as links using the UI form:
`[N-number or H-number](https://rulings.cbp.gov/ruling/<number>)` inside a
sentence stating what the ruling held. That exact URL pattern is what
`scripts/check_rulings.py` scans — the weekly `update-sources` workflow
re-verifies every cited ruling against CROSS and AMCROSS and **fails on
revoked or missing rulings** and warns on modified or unverified ones. Bare
ruling numbers in prose are not scanned; use the link form.

Archive a ruling as a bundle source (stub + file) only when it governs a
recurring BoxC fact pattern; otherwise cite by link — CROSS is the system of
record.

# Citations

[1] [CROSS](https://rulings.cbp.gov/)
[2] [19 CFR Part 177 — in the local Title 19 copy](/regulations/cfr-title-19.md)
[3] [CBP Valuation Encyclopedia](/sources/valuation-encyclopedia.md)
[4] [AMCROSS](https://amcross.us/) — MetaPhase's mirror of CROSS; API documented at [amcross.us/api](https://amcross.us/api)
