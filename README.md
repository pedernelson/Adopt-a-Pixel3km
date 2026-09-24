# Adopt-a-Pixel 3 km

## Every pixel is a real place. Every place has a biography.

**Adopt-a-Pixel 3 km (AaP3Km)** is a place-based Earth-observation and geographic-stewardship framework. It begins with explicit local geography, follows evidence through time, and connects field observations and human interpretation with regional, national, and global observing systems.

This repository is the developing public home for the AaP3Km Digital Visitor Center, process STEPs, Place Biographies, and reviewed Traveling Archives.

> **Repository status:** Initial public structure under development. A file or place listed as a candidate is not yet a completed or accepted Traveling Archive.

## Visit the Digital Visitor Center

[Open the AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

The live site is the public, visitor-facing entrance to featured places, the local-to-global spatial framework, long-term evidence timelines, Place Biographies, process STEPs, and reviewed Traveling Archives.

The [GitHub repository](https://github.com/pedernelson/Adopt-a-Pixel3km) remains the source and version-history environment for the website and its supporting materials.

## Start here

The live Visitor Center is generated from the repository's [`index.html`](index.html) file.

GitHub Pages publishes the site from the `main` branch and repository root.

## The local-to-global framework

AaP3Km works outward from explicit local support while retaining the relationships among scales:

```text
5 m SSU interpretation footprint
        ↓
100 m PSU place and history unit
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

## Sampling geography

An AaP3Km Area of Interest is a **3 km × 3 km AOI** centered on a random or otherwise documented physical-place anchor.

- The AOI contains **37 Primary Sample Units (PSUs)** using zero-based indexing.
- **PSU 0** is centered on the AOI anchor.
- PSUs 1–36 form the surrounding systematic array.
- Each PSU is **100 m × 100 m**.
- Each PSU contains **100 Secondary Sample Units (SSUs)** arranged on a 10 m grid.
- The standard SSU interpretation support is a **5 m × 5 m footprint**, not an infinitesimal point.

The AOI centerpoint identifies the Place Biography and Traveling Archive. SSU interpretations and field observations retain their actual coordinates, dates, spatial supports, source identities, and uncertainties.

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

No single observer or map product defines the place. Evidence types remain distinct and traceable.

## Traveling Archives

A Traveling Archive is a durable, evidence-bearing representation of a Place Biography. It is designed to preserve:

- what was known;
- when it was known;
- how it was known;
- which physical and temporal supports were involved;
- what was interpreted;
- what remains unresolved;
- and what should be watched next.

Traveling Archives are **dormant, not dead**. A released archive can later become the parent of a non-overwriting descendant when new observations, methods, plans, interpretations, or community knowledge become available.

GitHub is the project controller and accepted source of truth. Traveling Archives function as checked-out research and interpretation objects carrying evidence, provenance, lineage, and relationships. Immutable public release snapshots may also be preserved through formal GitHub releases and external repositories such as Zenodo.

## Featured-place scope

The public visitor center is intended to remain balanced across geography:

- **Oregon roots**, including Corvallis and Oregon State University, the Willamette Stone as a geographic-reference story, Mount Hood, the Columbia Gorge, and the Oregon Coast.
- **United States breadth**, including participant and publication-linked examples from Maine, California, Texas, New York, and other locations.
- **International reach**, including cohort and GLOBE Observer examples from India, Taiwan, Thailand, Panama, Saudi Arabia, and other countries.

Oregon is an important project and stewardship foundation, but the framework is not limited to Oregon. Each Place Biography begins with the geographic, physical, historical, and cultural foundations appropriate to that place.

## Repository structure

```text
Adopt-a-Pixel3km/
├── index.html              Public visitor-center homepage
├── README.md               Repository orientation and project principles
├── assets/
│   └── images/             Reviewed public images and graphics
├── places/                 Public Place Biography entry pages
├── steps/                  Public AaP3Km process STEP documentation
├── archives/               Disclosure-audited Traveling Archives
├── methods/                Methods, terminology, and citation resources
├── rights/                 Rights, licenses, and third-party notices
└── releases/               Public release manifests and checksums
```

Folders will be populated incrementally. Empty or planned folders do not imply completed content.

## Archive candidate pipeline

Source records do not become public Traveling Archives automatically.

### 1. Resolve place identity

- Verify the AOI centerpoint.
- Assign the durable MGRS Place Code.
- Identify country, region, and place name without replacing the coordinate identity.
- Record whether each coordinate is an AOI anchor, PSU center, SSU footprint, GLOBE site coordinate, or actual measurement coordinate.

### 2. Assemble evidence

- Preserve SSU labels and PSU relationships.
- Preserve actual GLOBE measurement coordinates rather than substituting site or grid coordinates.
- Retain directional photographs, dates, classifications, coordinate accuracy, source IDs, and native schemas.
- Attach map-producer evidence such as WorldCover and time-series evidence such as Landsat or LCMAP without allowing those products to overwrite Map User interpretation.
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
- unsupported claims of archive completeness, equivalence, or scientific certainty.

Scientific provenance should be retained while public-facing personal information is minimized or separated.

## Current development priorities

1. Verify and refine the live visitor-center homepage.
2. Add a credited local-to-global hero graphic.
3. Create structurally equivalent featured-place pages for Oregon, the wider United States, and international examples.
4. Build the archive-candidate registry around AOI centerpoints and durable MGRS Place Codes.
5. Publish public STEP overviews without presenting unresolved lanes as complete.
6. Release only disclosure-audited and rights-reviewed Traveling Archives.
7. Connect immutable release snapshots with formal citations, checksums, and archival identifiers.

## Contributing

Contributions should strengthen place identity, evidence traceability, temporal depth, support awareness, interpretation transparency, or long-term stewardship.

Before proposing a change:

1. Identify the physical place and coordinate role.
2. Identify the evidence source and native schema.
3. State the spatial and temporal support.
4. Preserve uncertainty and quality information.
5. Describe whether the contribution is observation, context, interpretation, method, or open work.
6. Avoid overwriting accepted parent records. Submit lineage-preserving descendants.
7. Confirm that public disclosure and redistribution are appropriate.

## Citation and releases

Do not cite a moving branch as though it were an immutable scientific release. Use a tagged GitHub release, DOI-bearing repository record, or other version-specific identifier when citing a published archive state.

A `CITATION.cff` file and release-level citation instructions will be added when the first repository release is ready.

## Rights and attribution

Project-created text, graphics, code, data products, and archive presentations require an explicit repository license before reuse terms can be assumed. Third-party records retain their original licenses and attribution requirements.

A repository-wide license has not yet been declared in this initial README. Until a license file and rights manifest are added, do not assume that every repository component has identical reuse terms.

## Contact and project context

AaP3Km is being developed through Oregon State University and related Earth-observation, citizen-science, education, publication, and stewardship collaborations.

This repository is intended to make the project understandable as a network of digital visitor centers for real places, not merely as a collection of HTML tools or data files.
