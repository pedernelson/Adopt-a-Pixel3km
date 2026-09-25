# AaP3Km Project Style Guide

**Version:** 3.0

## Durable Place organization

All Place-specific artifacts are organized beneath:

```text
Earth/{MGRS_PLACE_CODE}/
```

The MGRS Place Code is the durable namespace. EPSG:4326 latitude and longitude remain authoritative coordinates. Human-readable Place names are descriptive metadata and never replace the namespace.

Do not create human-name-only paths such as `archives/corvallis.html` or `archives/obidos.html`.

## Filenames

Preserve existing full filenames. New Place-specific artifacts use:

```text
AaP3Km_{MGRS_PLACE_CODE}_{PLACE_SLUG}_{ARTIFACT_TYPE}_{VERSION}_{STATE_OR_PURPOSE}_{YYYYMMDD}.{ext}
```

Historical files remain unchanged unless a new descendant is created.

## Names and measurements

- First use: **Adopt-a-Pixel 3 km (AaP3Km)**
- Later use: **AaP3Km**
- Area of Interest (AOI), Primary Sample Unit (PSU), Secondary Sample Unit (SSU)
- PSU 0 in prose; PSU-00 in fixed-width identifiers and optional map labels
- SI spacing: 5 m, 100 m, 3 km
- Dimensions: 5 m × 5 m, 100 m × 100 m, 3 km × 3 km
- Coordinates: latitude, longitude, with coordinate role
- Use center point in prose; preserve source-schema field names

## Canonical sampling geometry

- AOI: 3 km × 3 km
- AOI extent: ±1,500 m
- PSUs: 37, zero-based
- PSU support: 100 m × 100 m
- Surrounding PSU array: 6 × 6 at 500 m spacing
- SSUs per PSU: 100 in a 10 × 10 grid
- SSU spacing: 10 m
- SSU interpretation footprint: 5 m × 5 m

## Formal objects

Capitalize Place, Place Biography, Traveling Archive, Process STEP, MGRS Place Code, Map Producer, Map User, Earth System, Human Intent, Human Experience, Observations, and Interpretation History when referring to formal AaP3Km concepts.

## Public Traveling Archive order

1. Place
2. What is known
3. Explore the map
4. Evidence through time
5. What the evidence supports
6. Open reSearch
7. Provenance and archive lineage

## Status vocabulary

Accepted, Embedded, Partial, Open required, Unresolved, Zero results, Failed source, Not attempted, Not established, Not applicable, Working object, Check-in candidate, Reviewed release.

## Evidence and interface maturity

Report independently:

- Evidence maturity: Unresolved, Partial, Substantial, Reviewed
- Interface maturity: Technical, Reader-first, Map-first, Handoff-ready

A polished interface does not imply stronger evidence.

## Versioning

Never silently overwrite a delivered artifact. A revised archive is a versioned descendant with explicit parent filename and SHA-256. Preserve original evidence and source-native schemas.
