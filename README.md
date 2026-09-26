## Adopt-a-Pixel 3 km Digital Visitor Center

**Live site:** [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

This repository is the public discovery, learning, and presentation layer for Adopt-a-Pixel 3 km (AaP3Km). The separate [canonical AaP3Km repository](https://github.com/pedernelson/AaP3Km) remains the architecture and accepted-record system.

### Three connected public pathways

1. **Visit** — discover published Place Biographies and open versioned Traveling Archives.
2. **Learn** — use place-and-time-anchored learning tools, including the reusable GLOBE ground-to-satellite workflow.
3. **reSearch** — check out evidence, review unresolved work, and create non-overwriting descendants with explicit lineage.

### Repository organization

```text
Earth/{MGRS_PLACE_CODE}/{FULL_VERSIONED_ARTIFACT_FILENAME}
learn/GroundToSatellite/{VERSIONED_LEARNING_TOOL_FILENAME}
docs/{VERSIONED_PROJECT_STANDARD_FILENAME}
```

Human-readable place names support discovery, but MGRS Place Codes remain the durable place namespace.

### Course-neutral entry point

The public learning architecture is intentionally not named for a single course. GEOG 580, other courses, workshops, cohorts, and independent investigations can use the same ground-to-satellite entry point while maintaining course-specific instructions in their own learning-management-system pages or subfolders.

Course-specific materials may use paths such as `learn/courses/GEOG580/`, but the shared explorer remains at `learn/GroundToSatellite/`.

### Ground-to-satellite learning integration contract

The GLOBE ground-to-satellite explorer is a cumulative weekly learning tool. Each weekly record begins with a GLOBE Observer measurement coordinate and time, then searches the satellite and remote-sensing registry for potential measurement partners. The accepted record must preserve:

- stable GLOBE observation identity;
- measurement coordinates, time, and location accuracy when supplied;
- directional ground photographs;
- every satellite retrieval attempt and outcome;
- collection, item, asset, acquisition time, bands, QA, CRS, and spatial support;
- temporal and spatial relationship to the ground observation;
- one or more accepted adjacent remote-sensing measurements;
- map-producer interpretations as a separate evidence class;
- student interpretation and unresolved uncertainty.

The final term view places accepted remote-sensing measurements adjacent to ground photographs. It must not present discovery links, placeholders, stale canvases, or unverified products as retrieved evidence.

**Reserved public path:** `learn/GroundToSatellite/GLOBE_GroundToSatellite_Explorer.html`

Do not activate the Visitor Center link until multi-record testing verifies GLOBE retrieval, satellite provenance, evidence persistence, exports, and GitHub Pages behavior.

### Current public Traveling Archives

- `Earth/10TDQ772346/` — Corvallis and Oregon State University
- `Earth/19TEJ5375298161/` — Bass Harbor
- `Earth/19TEK6001717522/` — Acadia Welcome Center
- `Earth/21MXT6386590592/` — Óbidos, Brazil

The Acadia Welcome Center v1.4.1 map-display repair is the current public target. The v1.4.0 parent remains preserved for lineage.

### Project standards

- [Project style guide](docs/AaP3Km_PROJECT_STYLE_GUIDE_v003.md)
- [Traveling Archive public contract](docs/AaP3Km_TRAVELING_ARCHIVE_PUBLIC_CONTRACT_v002.md)
- [Traveling Archive migration plan](docs/AaP3Km_TRAVELING_ARCHIVE_MIGRATION_PLAN_v002.md)

A Traveling Archive is a checked-out reSearch working object, not an independent source of truth. New interpretations and repairs become non-overwriting descendants with explicit parent lineage.
