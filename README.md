# AaP3Km

## Canonical repository for Adopt-a-Pixel 3 km

**Adopt-a-Pixel 3 km (AaP3Km)** is a place-based Earth observation and geographic stewardship framework. This repository is the primary version controller and accepted source of truth for canonical schemas, Process STEP applications and releases, accepted registries, place-specific accepted records, checkout and check-in templates, and repository validation utilities.

> **Repository role:** Canonical architecture and accepted records. Public discovery and visitor-facing presentation are provided separately through the [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/) and its [Visitor Center repository](https://github.com/pedernelson/Adopt-a-Pixel3km).

## Core control statement

GitHub is the primary version controller and accepted source of truth. A Traveling Archive is a checked-out reSearch working object. Process STEP tools contribute records to one shared reSearch session. STEP03 assembles a check-in candidate, STEP04 reviews it, and an accepted candidate is committed externally without overwriting its parent.

## Durable place namespace

```text
Earth/{MGRS_PLACE_CODE}/
```

The **MGRS Place Code** is the durable place namespace. EPSG:4326 latitude and longitude remain the authoritative coordinates. Study geometry is a separately versioned support object and may initially be `NOT_ESTABLISHED`.

A Place is a real physical location on Earth. Coordinates, coordinate reference systems, MGRS codes, survey records, sampling geometry, and raster supports describe relationships to that Place; they do not create or define the Place's existence.

## Canonical control flow

```text
accepted Git commit
→ canonical checkout
→ Traveling Archive / reSearch working session
→ Process STEP contributions
→ STEP03 check-in candidate
→ STEP04 review
→ external Git commit
→ repository receipt
```

### Control rules

- Accepted records originate from an accepted Git commit.
- A canonical checkout creates a working object without changing the accepted parent.
- A Traveling Archive carries evidence, provenance, lineage, relationships, and open work into a reSearch session.
- All Process STEPs contribute to one shared reSearch session ledger.
- STEP03 assembles a check-in candidate; it does not accept the candidate.
- STEP04 reviews the check-in candidate.
- Accepted changes are committed externally through Git and do not overwrite the parent record.
- The repository receipt records the resulting accepted state and lineage.

## Repository layout

```text
apps/steps/                 Versioned Process STEP HTML applications
schemas/                    Canonical JSON schemas
registry/                   Accepted Process STEP release and Place registries
templates/                  Checkout, geometry, session, and check-in templates
Earth/{MGRS_PLACE_CODE}/    Place-specific accepted records
scripts/                    Import and validation utilities
docs/                       Architecture, workflow, and style guidance
```

### `apps/steps/`

Stores versioned Process STEP HTML applications. Each accepted application release must retain its STEP identity, build or release identifier, provenance, source hash, and validation record.

### `schemas/`

Stores canonical JSON schemas governing repository records, sessions, geometry, lineage, evidence, status, and check-in objects. Schema changes must be versioned and must not silently reinterpret existing accepted records.

### `registry/`

Stores accepted Process STEP release registries and Place registries. Registry entries are accepted records, not informal indexes.

### `templates/`

Stores canonical templates for checkouts, geometry, reSearch sessions, shared session ledgers, and check-in candidates.

### `Earth/{MGRS_PLACE_CODE}/`

Stores accepted records for one durable Place namespace. The MGRS Place Code organizes the repository, while authoritative EPSG:4326 latitude and longitude and versioned support geometries remain explicit within the records.

### `scripts/`

Stores deterministic import, validation, registry, hash, and release utilities. Scripts must report failures explicitly and must not silently normalize away source differences.

### `docs/`

Stores architecture, workflow, governance, terminology, naming, measurement, and release guidance. The project-wide style guide belongs here.

## Repository-role boundary

AaP3Km uses two public repositories with distinct responsibilities.

### This canonical `AaP3Km` repository

Controls:

- canonical schemas;
- accepted Process STEP releases;
- accepted Process STEP and Place registries;
- canonical templates;
- accepted Place-specific records;
- import and validation utilities;
- architecture and governance documentation.

### The `Adopt-a-Pixel3km` Visitor Center repository

Publishes:

- the AaP3Km Digital Visitor Center;
- introductory and explanatory content;
- featured-place discovery;
- public methods orientation;
- links to canonical accepted records and reviewed releases.

The Visitor Center may summarize, discover, and link to canonical objects. It must not independently redefine canonical schemas, accepted records, Process STEP releases, or Place registries.

## Project-wide naming and measurement standard

The authoritative style guide is:

```text
docs/AaP3Km_PROJECT_STYLE_GUIDE_v001_20260924.md
```

The guide applies to new and actively revised public prose, figures, tables, maps, interfaces, Process STEPs, schemas, registries, Place Biographies, Traveling Archives, release packages, and teaching materials.

### Project names

- First use: **Adopt-a-Pixel 3 km (AaP3Km)**
- Later use: **AaP3Km**
- Canonical repository: `AaP3Km`
- Visitor Center repository slug: `Adopt-a-Pixel3km`
- Public site name: **AaP3Km Digital Visitor Center**

Repository slugs, historical filenames, source fields, and established machine identifiers retain their actual values for provenance.

### Formal object names

Capitalize formal AaP3Km objects and concepts:

- **Place**
- **Place Biography**
- **Traveling Archive**
- **Process STEP** and **Process STEPs**
- **MGRS Place Code**
- **Map Producer**
- **Map User**
- **Public Spectral Steward**
- **Community Chronicles**
- **Earth System**
- **Human Intent**
- **Human Experience**
- **Observations**
- **Interpretation History**

### Metric units and dimensions

Use SI unit symbols with a space between the numerical value and the unit:

- `5 m`
- `10 m`
- `100 m`
- `500 m`
- `1,500 m`
- `3 km`

Use the multiplication sign with spaces for dimensions:

- `5 m × 5 m`
- `100 m × 100 m`
- `3 km × 3 km`
- `10 × 10 grid`

Unit symbols remain singular and do not take periods. Do not treat nominal spatial resolution as positional accuracy, interpretation support, or thematic certainty.

### Sampling-unit names

On first use:

- **Area of Interest (AOI)**
- **Primary Sample Unit (PSU)**
- **Secondary Sample Unit (SSU)**

Thereafter use **AOI**, **PSU**, and **SSU**.

Use **PSU 0** in prose. Use **PSU-00** in fixed-width machine identifiers and optional map-label layers.

### Coordinates and coordinate roles

- Public display order: **latitude, longitude**
- Authoritative exchange coordinates: EPSG:4326 latitude and longitude
- Durable namespace: MGRS Place Code
- Prose form: **center point**
- Machine fields: preserve established forms such as `centerpoint`, `aoi_center`, or `center_point`

Identify coordinate role whenever ambiguity is possible:

- AOI center point
- PSU center point
- SSU grid point
- SSU interpretation-footprint center
- GLOBE site coordinate
- GLOBE measurement coordinate
- map-product query coordinate
- raster-pixel center

Preserve full source precision in machine-readable records. Displaying more decimal places does not establish greater positional accuracy.

## Canonical sampling geometry

An AaP3Km Area of Interest is a **3 km × 3 km AOI** centered on a documented physical-place anchor.

- The AOI extends **±1,500 m** from its origin.
- The AOI contains **37 PSUs** using zero-based indexing.
- **PSU 0** is **100 m × 100 m** and centered on the AOI origin.
- PSUs 1–36 form a separate **6 × 6** surrounding array with **500 m** center-to-center spacing.
- Each PSU contains **100 SSUs** arranged in a **10 × 10 grid** with **10 m** center-to-center spacing.
- Each SSU has a standard **5 m × 5 m interpretation footprint** centered on its grid location.

The AOI center point is also the center point of PSU 0. Points are anchors to explicit supports; they are not assumed to be infinitesimal locations.

Study geometry is independently versioned and may be `NOT_ESTABLISHED` during early checkout or unresolved work. Geometry status must not be inferred from the presence of a Place namespace alone.

## Place Biography evidence model

A Place Biography synchronizes five evidence timelines:

1. **Earth System**  
   Physical history, geology, climate, hydrology, vegetation, disturbance, and recovery.

2. **Human Intent**  
   Plans, proposals, policies, management decisions, restoration, implementation actions, and future watches.

3. **Human Experience**  
   Community Chronicles, field experience, cultural relationships, local knowledge, and stewardship history.

4. **Observations**  
   Survey records, field photographs, GLOBE Observer measurements, aerial imagery, Landsat, Sentinel, lidar, radar, thermal observations, and other evidence.

5. **Interpretation History**  
   Labels, maps, scientific analyses, disagreements, uncertainty, reconciliation, revision, and accepted archive states.

No single observer or Map Producer defines the Place. Evidence types remain distinct and traceable.

## Traveling Archive and reSearch rules

A Traveling Archive is a checked-out, evidence-bearing reSearch working object. It carries:

- Place identity and lineage;
- source-native observations;
- authoritative coordinates and coordinate roles;
- versioned spatial and temporal supports;
- processing and retrieval provenance;
- Map Producer records;
- Map User interpretations;
- uncertainty and QA states;
- accepted findings and claim boundaries;
- unresolved and open work;
- future watches.

A Traveling Archive is not independently authoritative. It may become the parent of a non-overwriting descendant after review and external Git acceptance.

Traveling Archives are **dormant, not dead**. An inactive archive remains available for later reactivation, extension, reinterpretation, or comparison when new observations, plans, methods, or community knowledge emerge.

## Shared reSearch session ledger

All Process STEPs contribute records to a shared reSearch session ledger. A STEP contribution must preserve:

- STEP identity and release;
- session identity;
- Place identity;
- source record identity;
- operation date and status;
- input and output relationships;
- coordinate and support roles;
- evidence status;
- unresolved conditions;
- responsible review state;
- parent and descendant lineage.

STEP-specific files or interface state must not substitute for the shared ledger.

## Status vocabulary

Use explicit status values. Do not collapse distinct states into *missing* or *failed*.

Recommended public and machine-readable concepts include:

- **Accepted record**
- **Reviewed release**
- **Working object**
- **Check-in candidate**
- **Candidate Place**
- **Accepted as Place evidence**
- **Accepted with caution**
- **Accepted as context evidence**
- **QA only**
- **Diagnostic only**
- **Unresolved / open work**
- **Failed source**
- **Not attempted**
- **Zero results**
- `NOT_ESTABLISHED`

A successful zero-result query is not a failure. A failed request is not equivalent to not attempted. Geometry that is `NOT_ESTABLISHED` is not equivalent to missing accepted geometry.

## Process STEP HTML import

Place the 13 Build002 HTML source files beside:

```text
scripts/import_step_html.sh
```

Run the importer from the repository root. The importer verifies each source SHA-256 before copying the file into:

```text
apps/steps/{STEP}/releases/Build002/
```

Do not bypass hash verification, rename Build002 source files without updating the verified import manifest, or present unverified files as accepted Process STEP releases.

## Source-schema preservation

Do not normalize away scientifically meaningful source differences.

Preserve:

- native field names;
- raw producer values;
- original labels;
- source IDs;
- retrieval timestamps;
- coordinate roles;
- declared accuracy;
- spatial and temporal supports;
- QA states;
- processing lineage;
- source license and attribution.

Harmonized labels, summaries, and public cards are derived views and must link back to source-native records.

## Scientific principles

- **Geography first.** Establish and verify mapped geography before analysis or labeling.
- **Points are anchors, not infinitesimal supports.** Preserve the footprint, pixel, field of view, or other support represented by each record.
- **Same place, same time, and corresponding support come before thematic agreement.**
- **Map Producer and Map User uncertainty remain separate.**
- **Nominal spatial resolution is not positional accuracy or thematic certainty.**
- **Stable classes can contain restless pixels.** Preserve temporal and spectral evidence even where a thematic class appears unchanged.
- **Every PSU matters.** Stable, unresolved, low-priority, and no-event locations remain visible.
- **Raw source identities and values are preserved.** Derived records must remain traceable to them.
- **Incomplete work is explicit.** Missing labels, failed requests, zero-result searches, and unresolved evidence do not silently disappear.
- **Parents are not overwritten.** Accepted descendants preserve ancestry and decision history.

## Map and figure requirements

When showing AOI, PSU, or SSU geometry, identify the object and support:

- `AOI · 3 km × 3 km`
- `PSU 0 · 100 m × 100 m`
- `SSU interpretation footprint · 5 m × 5 m`

AOI, PSU, and SSU geometry should remain visually unobscured and unfilled when interpreted against imagery. If shading is needed, apply it outside the focus geometry. Plot and PSU labels, including `PSU-00`, should be a separate optional layer.

Scientific captions should identify the Place, time, support, observer or Map Producer, coordinate or CRS basis when relevant, interpretation boundary, uncertainty, source, and reuse attribution.

## Validation and acceptance

A candidate is not accepted merely because it renders or exists in the repository working tree.

Before acceptance, verify as applicable:

- canonical schema conformance;
- source-file identity and SHA-256;
- coordinate order and coordinate role;
- geometry status and CRS;
- spatial and temporal support;
- source-native values and lineage;
- evidence and QA statuses;
- unresolved conditions;
- parent and descendant relationships;
- disclosure and rights readiness;
- registry update requirements.

Acceptance must produce a repository receipt or equivalent traceable record.

## Public disclosure and rights

Before public release, inspect for:

- personal data and participant identifiers;
- email addresses and phone numbers;
- credentials and tokens;
- private URLs;
- reviewer and editorial material;
- restricted or culturally sensitive records;
- redistribution restrictions;
- third-party attribution and license requirements.

Retain scientific provenance while minimizing or separating public-facing personal information. Public Visitor Center cards must not expose raw participant identifiers merely because they are present in source exports.

## File, version, and release naming

- Use descriptive filenames with version identifiers and `YYYYMMDD` dates.
- Preserve historical source filenames in provenance records.
- Never overwrite a delivered release silently.
- Use SHA-256 for import and release verification.
- Use immutable Git tags or DOI-bearing records for scientific citation.
- Do not cite a moving branch as though it were an immutable release.
- Preserve parent-child lineage for descendant Place Biographies and Traveling Archives.

Examples:

```text
AaP3Km_PROJECT_STYLE_GUIDE_v001_20260924.md
AaP3Km_SCHEMA_SESSION_LEDGER_v001_20260924.json
AaP3Km_STEP03_CHECKIN_CANDIDATE_v001_20260924.json
```

## Contributing

Contributions should strengthen canonical architecture, Place identity, evidence traceability, support awareness, temporal depth, interpretation transparency, or long-term stewardship.

Before proposing a change:

1. Identify the Place and MGRS Place Code, if established.
2. Identify authoritative coordinates and coordinate roles.
3. Identify the source and preserve its native schema.
4. State spatial and temporal support.
5. Preserve uncertainty, QA, and unresolved status.
6. Identify the relevant Process STEP, schema, registry, or accepted Place record.
7. Preserve parent and descendant lineage.
8. Follow the project-wide naming and measurement standard.
9. Confirm disclosure and redistribution readiness.
10. Do not overwrite accepted parent records.

## Citation and releases

Use a tagged GitHub release, DOI-bearing repository record, or another immutable version-specific identifier when citing an accepted release.

A `CITATION.cff` file and release-level citation instructions should accompany the first formal repository release. Third-party records retain their original licenses and attribution requirements.

## Current canonical priorities

1. Add the project-wide style guide under `docs/`.
2. Audit existing repository prose, schemas, interfaces, and labels for naming and measurement consistency.
3. Preserve the canonical repository and Visitor Center repository role boundary.
4. Verify the Build002 Process STEP import manifest and source SHA-256 values.
5. Maintain the shared reSearch session ledger across Process STEPs.
6. Build and validate accepted Place registries under the durable MGRS namespace.
7. Keep study geometry independently versioned and explicitly statused.
8. Maintain disclosure, rights, lineage, and immutable-release discipline.

## Related public site

- [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)
- [Visitor Center source repository](https://github.com/pedernelson/Adopt-a-Pixel3km)

The Digital Visitor Center is the public discovery layer. This `AaP3Km` repository remains the canonical architecture and accepted-record system.
