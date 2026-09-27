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
steps/STEP00/{VERSIONED_STEP00_TOOL_FILENAME}
docs/{VERSIONED_PROJECT_STANDARD_FILENAME}
```

Human-readable place names support discovery, but MGRS Place Codes remain the durable place namespace.

### Generic STEP00 learning entry point

The shared learning pathway begins with a course-neutral, map-first STEP00: **Explore a Place and Begin Its Observation Record**. Courses, workshops, cohorts, and independent investigations can use this same entry point while keeping their own instructions in Canvas or another learning context.

**Public route:** `steps/STEP00/AaP3Km_STEP00_ExplorePlace_MapFirst.html`

STEP00 guides a visitor through five actions: explore, compare, establish, validate, and preserve. The resulting baseline Traveling Archive carries place identity, authoritative geometry, AOI/PSU/SSU supports, source roles, observations, retrieval outcomes, open questions, geometry audit, and the STEP00 to STEP00.5 handoff.

The initial reflection uses four plain-language prompts:

- What do you want to investigate at this place?
- Which observation, image, or map product may help?
- What does that source help you notice or measure?
- What additional evidence would help you check, refine, or challenge your first impression?

The last question replaces the less clear wording, “It cannot establish ___ by itself.”

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
