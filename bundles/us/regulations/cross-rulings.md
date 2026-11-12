---
type: Reference
title: CROSS — Customs Rulings
description: CBP's database of binding ruling letters (classification, valuation, origin) — legal force, the JSON search API, search strategy, and the citation convention this bundle enforces.
resource: https://rulings.cbp.gov/
tags: [rulings, cross, classification, valuation, origin, precedent]
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

# The API (undocumented — may change; access re-verified 2026-11-12)

| Endpoint | Anonymous access (as of 2026-11-12) | Returns |
|----------|-------------------------------------|---------|
| `https://rulings.cbp.gov/api/search?term=<urlencoded>&collection=ALL&pageSize=30&page=1&sortBy=DATE_DESC` | **Gated** — HTTP 403 `Security parameters are missing from this request context.` | `{rulings: […], totalHits: N}` — each record: `rulingNumber`, `subject`, `categories`, `rulingDate`, `collection` (ny/hq), `tariffs`, `relatedRulings`, `modifies`/`modifiedBy`, `revokes`/`revokedBy`, `operationallyRevoked` |
| `https://rulings.cbp.gov/api/ruling/<number>` | Open (404 if no such ruling) | The full ruling: same metadata plus `text` and a short-lived PDF `url`; the link fields (`revokes`, `revokedBy`, `modifies`, `modifiedBy`, `relatedRulings`) come back null |
| `https://rulings.cbp.gov/ruling/<number>` | Open | Human-readable UI page — **the citation link form** |

**Search requires reCAPTCHA (since 2026-11-12).** The web UI loads
`/api/app-config`, which now carries a Google reCAPTCHA `siteKey`, and the
search page's own API calls succeed while direct calls get the 403 above.
Search is therefore usable only through the
[web UI](https://rulings.cbp.gov/search) in a browser; scripts and agents
should not try to obtain or replay reCAPTCHA tokens. Single-ruling lookups
still work without a token.

In the UI's search, `collection` accepts `ALL`, `NY`, `HQ`. Quote
multi-word terms (`"de minimis"`) for phrase search.

**Revocation status needs search.** The single-ruling endpoint's link fields
are null even for revoked rulings — e.g. NY N334409 comes back with no
`revokedBy`, though HQ H336180 revokes it (both left unlinked here on
purpose, since N334409 is not good law) — and in search results links were only ever populated in the
*forward* direction (the revoking ruling lists its targets in `revokes`). To
test whether a ruling is still good law, search its number as a quoted term
in the web UI and check the *other* results for one that revokes or modifies
it (a revoking ruling always cites its target).

`scripts/check_rulings.py` tries the search API first and does that reverse
scan automatically if search answers. On a 403 it falls back to the
single-ruling endpoint: a missing ruling is still an ERROR, but an existing
one is reported as a WARN ("revocation status unverified") with a search
link to check by hand.

# Search Strategy

- Combine a product term with an HTS heading (`"lithium battery" 8507`) to
  cut noise; the `tariffs` field confirms what a ruling actually classified.
- Beware term collisions: "de minimis" in CROSS usually means the **textile
  rules-of-origin tolerance** (19 CFR 102.21) or minor-ingredient doctrines —
  not the Section 321 $800 exemption covered in
  [De Minimis Suspension](/entry/de-minimis-suspension.md).
- Before relying on any ruling, confirm validity (see the quirk above) and
  check `modifies`/`relatedRulings` for the fuller precedent chain.
- For valuation fact patterns, start with the
  [Valuation Encyclopedia](/valuation/customs-valuation.md), which digests
  rulings by topic, then pull the current text from CROSS.

# Citation Convention (enforced)

Cite rulings in concepts as links using the UI form:
`[N-number or H-number](https://rulings.cbp.gov/ruling/<number>)` inside a
sentence stating what the ruling held. That exact URL pattern is what
`scripts/check_rulings.py` scans — the weekly `update-sources` workflow
re-verifies every cited ruling against CROSS and **fails on revoked or
missing rulings** and warns on modified ones (while search is gated, it can
only confirm existence and warns on every found ruling — see above). Bare ruling numbers in prose
are not scanned; use the link form.

Archive a ruling as a bundle source (stub + file) only when it governs a
recurring BoxC fact pattern; otherwise cite by link — CROSS is the system of
record.

# Citations

[1] [CROSS](https://rulings.cbp.gov/)
[2] [19 CFR Part 177 — in the local Title 19 copy](/regulations/cfr-title-19.md)
[3] [CBP Valuation Encyclopedia](/sources/valuation-encyclopedia.md)
