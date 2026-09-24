# Adopt-a-Pixel 3 km

## Every pixel is a real place. Every place has a biography.

**Adopt-a-Pixel 3 km (AaP3Km)** is a place-based Earth observation and geographic stewardship framework. It begins with explicit local geography, follows evidence through time, and connects field observations and human interpretation with regional, national, and global observing systems.

This repository publishes the **AaP3Km Digital Visitor Center**, the public discovery and orientation layer for featured places, the local-to-global spatial framework, long-term evidence timelines, Place Biographies, Process STEPs, and reviewed Traveling Archives.

> **Repository status:** Initial public structure under development. A place, file, or link identified as a candidate is not yet a completed, accepted, or immutable release.

## Visit the Digital Visitor Center

[Open the AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

The live site is generated from the repository's [`index.html`](index.html) file and published from the `main` branch through GitHub Pages.

## Repository roles

AaP3Km uses two public repositories with different responsibilities. They must not be treated as interchangeable sources of truth.

### Canonical architecture and accepted records

The [`AaP3Km` repository](https://github.com/pedernelson/AaP3Km) is the primary version controller and accepted source of truth for:

- canonical schemas;
- versioned Process STEP applications and releases;
- accepted Process STEP and place registries;
- checkout, geometry, session, and check-in templates;
- place-specific accepted records;
- import and validation utilities;
- architecture and workflow guidance.

A Traveling Archive is a checked-out reSearch working object. Process STEP tools contribute records to one shared reSearch session. STEP03 assembles a check-in candidate, STEP04 reviews it, and an accepted candidate is committed externally without overwriting its parent.

The canonical control flow is:

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

### Digital Visitor Center and discovery

This [`Adopt-a-Pixel3km` repository](https://github.com/pedernelson/Adopt-a-Pixel3km) publishes:

- the public Digital Visitor Center;
- introductory and explanatory materials;
- featured-place discovery;
- public methods orientation;
- links to canonical accepted records and reviewed releases.

This repository may summarize and link to canonical objects, but it must not independently redefine canonical schemas, accepted records, Process STEP releases, or place registries.

## Durable place namespace

Canonical accepted place records use:

```text
Earth/{MGRS_PLACE_CODE}/
```

The **MGRS Place Code** is the durable place namespace. EPSG:4326 latitude and longitude remain the authoritative coordinates. Study geometry is a separately versioned support object and may initially be `NOT_ESTABLISHED`.

A coordinate describes a relationship to a real physical place. It does not create or define the existence of that place.

## The local-to-global framework

AaP3Km works outward from explicit local support while retaining relationships among scales:

```text
5 m × 5 m SSU interpretation footprint
        ↓
100 m × 100 m PSU place and history unit
        ↓
3 km × 3 km AOI
        ↓
Landscape and regional context
        ↓
National comparison
        ↓
Global observing systems
```

Time extends across the same framework:

```text
Deep physical history
→ geographic reference and surveys
→ aerial photography
→ Landsat and other satellite records
→ present field observations
→ interpretation history
→ future watches
```

## Naming and measurement conventions

The project-wide standard is maintained in:

```text
AaP3Km/docs/AaP3Km_PROJECT_STYLE_GUIDE_v001_20260924.md
```

The following conventions apply to public prose, figures, tables, maps, interfaces, Process STEPs, Place Biographies, Traveling Archives, and new machine-readable fields.

### Project names

- Write **Adopt-a-Pixel 3 km (AaP3Km)** on first use.
- Use **AaP3Km** thereafter.
- Use `AaP3Km` for the canonical repository name.
- Use `Adopt-a-Pixel3km` only for the Visitor Center repository slug or another system identifier that cannot contain spaces.
- Use **AaP3Km Digital Visitor Center** for the public site.

### Units and dimensions

- Use SI symbols with a space between number and unit: **5 m**, **10 m**, **100 m**, **500 m**, and **3 km**.
- Unit symbols remain singular and do not take periods.
- Use the multiplication sign with spaces for dimensions: **5 m × 5 m**, **100 m × 100 m**, and **3 km × 3 km**.
- Use an en dash for closed ranges, such as **2020–2021**.
- Use **±2.5 m** when expressing the half-width of the standard SSU interpretation footprint and when that uncertainty interpretation is explicitly intended.
- Do not treat nominal spatial resolution as positional accuracy, interpretation support, or thematic certainty.

### Sampling-unit names

On first use, write:

- **Area of Interest (AOI)**;
- **Primary Sample Unit (PSU)**;
- **Secondary Sample Unit (SSU)**.

Thereafter use **AOI**, **PSU**, and **SSU**.

Use **PSU 0** in ordinary prose. Use **PSU-00** in fixed-width machine identifiers and optional map-label layers.

### Coordinate wording

- Use **center point** as two words in prose.
- Preserve source-schema fields such as `centerpoint`, `aoi_center`, or `center_point` when quoting or exchanging machine-readable data.
- Display geographic coordinates as **latitude, longitude**.
- Identify the coordinate role, such as AOI center point, PSU center point, SSU footprint center, GLOBE site coordinate, GLOBE measurement coordinate, map-product query coordinate, or raster-pixel center.
- Preserve full source precision in machine-readable records. Shortened display precision must not imply greater positional accuracy.

### Formal object names

Capitalize formal AaP3Km objects and concepts, including:

- **Place Biography**;
- **Traveling Archive**;
- **Process STEP** and **Process STEPs**;
- **MGRS Place Code**;
- **Map Producer**;
- **Map User**;
- **Public Spectral Steward**;
- **Community Chronicles**;
- **Earth System**;
- **Human Intent**;
- **Human Experience**;
- **Observations**;
- **Interpretation History**.

Use **Earth observation** as a noun and **Earth-observation** as a compound adjective. Use **land cover** as a noun and **land-cover** as a compound adjective.

## Sampling geography

An AaP3Km Area of Interest is a **3 km × 3 km AOI** centered on a random or otherwise documented physical-place anchor.

- The AOI extends **±1,500 m** from its origin.
- The AOI contains **37 PSUs** using zero-based indexing.
- **PSU 0** is **100 m × 100 m** and centered on the AOI origin.
- PSUs 1–36 form a separate **6 × 6** surrounding array with **500 m** center-to-center spacing.
- Each PSU contains **100 SSUs** arranged in a **10 × 10 grid** with **10 m** center-to-center spacing.
- Each SSU has a standard **5 m × 5 m interpretation footprint** centered on its grid location.

The AOI center point, which is also the center point of PSU 0, identifies the Place Biography and Traveling Archive. SSU interpretations and field observations retain their actual coordinates, dates, spatial supports, source identities, coordinate roles, and uncertainties.

## Place Biographies

A Place Biography connects five synchronized evidence timelines:

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

No single observer or Map Producer defines the place. Evidence types remain distinct and traceable.

## Traveling Archives

A Traveling Archive is a durable, evidence-bearing representation of a Place Biography. It preserves:

- what was known;
- when it was known;
- how it was known;
- the spatial and temporal supports involved;
- source identities and processing lineage;
- accepted interpretations and claim boundaries;
- unresolved and open work;
- and future monitoring needs.

Traveling Archives are **dormant, not dead**. A released archive may later become the parent of a non-overwriting descendant when new observations, methods, plans, interpretations, or community knowledge become available.

A Traveling Archive is not independently authoritative. Canonical acceptance occurs through the `AaP3Km` repository control flow.

## Featured-place scope

The Digital Visitor Center remains balanced across geography:

- **Oregon roots**, including Corvallis and Oregon State University, the Willamette Stone as a geographic-reference story, Mount Hood, the Columbia Gorge, and the Oregon Coast.
- **United States breadth**, including participant and publication-linked examples from Maine, California, Texas, New York, and other locations.
- **International reach**, including cohort and GLOBE Observer examples from India, Taiwan, Thailand, Panama, Saudi Arabia, and other countries.

Oregon is an important project and stewardship foundation, but AaP3Km is not limited to Oregon. Each Place Biography begins with the geographic, physical, historical, and cultural foundations appropriate to that place.

## Repository structure

### Canonical `AaP3Km` repository

```text
apps/steps/                 Versioned Process STEP HTML applications
schemas/                    Canonical JSON schemas
registry/                   Accepted Process STEP release and place registries
templates/                  Checkout, geometry, session, and check-in templates
Earth/{MGRS_PLACE_CODE}/    Place-specific accepted records
scripts/                    Import and validation utilities
docs/                       Architecture and workflow guidance
```

### Visitor Center `Adopt-a-Pixel3km` repository

```text
Adopt-a-Pixel3km/
├── index.html              Public Digital Visitor Center homepage
├── README.md               Repository orientation and project principles
├── assets/
│   └── images/             Reviewed public images and graphics
├── places/                 Public Place Biography discovery pages
├── methods/                Public methods and terminology
└── rights/                 Rights, licenses, and third-party notices
```

Presentation paths should link to canonical accepted records rather than duplicate or redefine them.

## Archive candidate pipeline

Source records do not become public Traveling Archives automatically.

### 1. Resolve place identity

- Verify the AOI center point.
- Assign the durable MGRS Place Code.
- Identify country, region, and place name without replacing coordinate identity.
- Record whether each coordinate is an AOI center point, PSU center point, SSU footprint center, GLOBE site coordinate, GLOBE measurement coordinate, map-product query coordinate, or raster-pixel center.

### 2. Assemble evidence

- Preserve SSU labels and PSU relationships.
- Preserve actual GLOBE measurement coordinates rather than substituting site or grid coordinates.
- Retain directional photographs, dates, classifications, coordinate accuracy, source IDs, and native schemas.
- Attach Map Producer evidence such as WorldCover and time-series evidence such as Landsat or LCMAP without allowing those products to overwrite Map User interpretation.
- Carry incomplete and unresolved records forward as explicit open work.

### 3. Review before public release

- Run coordinate and support sanity checks.
- Resolve duplicates without deleting source lineage.
- Harmonize labels while preserving raw values.
- Separate accepted evidence, contextual evidence, caution states, QA-only records, and failed or unresolved sources.
- Review personal information, credentials, private links, participant identifiers, culturally sensitive information, redistribution rights, and third-party licenses.
- Document claim boundaries and unresolved blockers.

## Scientific principles

- **Geography first.** Establish and verify mapped geography before analysis or labeling.
- **Points are anchors, not infinitesimal supports.** Preserve the footprint, pixel, field of view, or other area represented by each record.
- **Same place, same time, and corresponding support come before thematic agreement.**
- **Map Producer and Map User uncertainty remain separate.**
- **Nominal spatial resolution is not positional accuracy or thematic certainty.**
- **Stable classes can contain restless pixels.** Preserve temporal and spectral evidence even where a thematic class appears unchanged.
- **Every PSU matters.** Stable, unresolved, low-priority, and no-event locations remain visible.
- **Raw source identities and values are preserved.** Derived and harmonized values must remain traceable to them.
- **Incomplete work is explicit.** Missing labels, failed requests, zero-result searches, and unresolved evidence do not silently disappear.

## Public-release and privacy policy

Before any archive, dataset, photograph collection, or repository package is released publicly, it must receive a disclosure and rights review.

Public releases must not expose:

- participant or contributor email addresses unless there is a documented public-use reason and permission;
- credentials, access tokens, secrets, or private service URLs;
- private reviewer or editorial material;
- restricted, culturally sensitive, or protected location information;
- third-party material without appropriate rights and attribution;
- unsupported claims of archive completeness, equivalence, acceptance, or scientific certainty.

Scientific provenance should be retained while public-facing personal information is minimized or separated.

## Current development priorities

1. Apply the project-wide style guide across the Digital Visitor Center, canonical documentation, maps, figures, and new records.
2. Add a credited local-to-global hero graphic.
3. Create structurally equivalent featured-place discovery pages for Oregon, the wider United States, and international examples.
4. Build the candidate registry around AOI center points and durable MGRS Place Codes.
5. Link Visitor Center presentations to canonical `Earth/{MGRS_PLACE_CODE}/` records.
6. Publish Process STEP overviews without presenting unresolved lanes as complete.
7. Release only disclosure-audited and rights-reviewed Traveling Archives.
8. Connect immutable release snapshots with formal citations, checksums, and archival identifiers.

## Contributing

Contributions should strengthen place identity, evidence traceability, temporal depth, support awareness, interpretation transparency, or long-term stewardship.

Before proposing a change:

1. Identify the physical place and coordinate role.
2. Identify the evidence source and native schema.
3. State the spatial and temporal support.
4. Preserve uncertainty and quality information.
5. Describe whether the contribution is an observation, context, interpretation, method, or open-work record.
6. Follow the project-wide naming and measurement standard.
7. Avoid overwriting accepted parent records. Submit lineage-preserving descendants.
8. Confirm that public disclosure and redistribution are appropriate.

## Citation and releases

Do not cite a moving branch as though it were an immutable scientific release. Use a tagged GitHub release, DOI-bearing repository record, or another version-specific identifier when citing a published archive state.

A `CITATION.cff` file and release-level citation instructions will be added when the first repository release is ready.

## Rights and attribution

Project-created text, graphics, code, data products, and archive presentations require an explicit repository license before reuse terms can be assumed. Third-party records retain their original licenses and attribution requirements.

A repository-wide license has not yet been declared in this initial Visitor Center repository. Until a license file and rights manifest are added, do not assume that every repository component has identical reuse terms.

## Contact and project context

AaP3Km is being developed through Oregon State University and related Earth observation, citizen science, education, publication, and stewardship collaborations.

This repository makes the project understandable as a network of digital visitor centers for real places. It is not merely a collection of HTML tools or data files, and it does not replace the canonical `AaP3Km` repository.
