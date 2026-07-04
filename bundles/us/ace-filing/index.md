# ACE Filing (ABI / CATAIR)

The technical layer of filing into ACE: the Automated Broker Interface and
the CATAIR specifications — transaction chapters, code appendices, PGA data,
and the error dictionaries that explain rejections. Business-process context
for entries lives in [Entry](../entry/index.md).

* [ABI & CATAIR Overview](abi-catair-overview.md) - The document set, its quirks (DRAFT footers, pub numbers), and how to track versions and deployments.
* [Cargo Release Filing (SE)](cargo-release.md) - Release record formats, business rules, validation/error codes — including the 2026 importer-inactive reject.
* [Entry Summary Filing (AE/AX)](entry-summary-filing.md) - 7501-data record formats; rev 108 in production, rev 109 pending; status notifications, error dictionary, census overrides.
* [In-Bond Filing (QP)](in-bond-filing.md) - Moving merchandise under bond without entry: IT/T&E/IE transactions and their error dictionary.
* [Statements & Duty Payment](statements-duty-payment.md) - Daily and periodic monthly statements over ACH, and the de-minimis-driven 2,000-entry cap.
* [Reconciliation Filing (RE)](reconciliation.md) - Entry Type 09 reconciliation of estimated value/classification/FTA elements.
* [eBond Filing (CB/CX)](ebond-filing.md) - How sureties put bonds on file in ACE electronically.
* [Importer & Manufacturer Identity Filing (5106 / MID)](importer-manufacturer-ids.md) - The identity records every entry depends on.
* [Importer Security Filing (ISF 10+2)](importer-security-filing.md) - Ocean security filing: ISF-10/ISF-5, status advisories, error codes.
* [PGA Message Set Filing](pga-message-set.md) - Agency data with entries: PG records, tariff flags and enforcement, corrections, prior notice, error dictionary.
* [CPSC eFiling](cpsc-efiling.md) - Consumer-product certificate data mandatory in ACE production 2026-07-08.
* [CATAIR Reference Appendices](catair-reference-appendices.md) - Valid codes, entry numbers, duty calculation, and other cross-chapter tables.
