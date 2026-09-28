# Adopt-a-Pixel 3 km Digital Visitor Center

**Live site:** [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

This repository is the public discovery, learning, and presentation layer for Adopt-a-Pixel 3 km. The canonical AaP3Km repository remains the architecture and accepted-record system.

## Public pathways

- **Visit:** locate Place Biographies and open their Traveling Archives.
- **Learn:** begin a course-neutral, map-first STEP00 investigation.
- **reSearch:** revisit evidence, preserve unresolved work, and create non-overwriting descendants with explicit lineage.

## Welcome Center map

The root `index.html` is an orientation map. It shows:

- Traveling Archive anchors;
- open-access published interpretation locations;
- HLS product-tile context; and
- unfilled 3 km × 3 km AaP3Km place areas.

The Welcome Center deliberately does not display PSU boundaries, SSU footprints, local HLS 30 m cells, or GLOBE observations. Those details belong in STEP00 and the Traveling Archives.

## STEP00

Public route:

```text
steps/STEP00/AaP3Km_STEP00_ExplorePlace_MapFirst.html
```

STEP00 begins with a real physical place and guides the user through five actions: explore, compare, establish, validate, and preserve. It includes live GLOBE API retrieval for `land_covers` and `tree_heights`; no separate GLOBE GeoJSON is required for the Welcome Center.

STEP00 creates the 3 km × 3 km AOI from the documented physical-place anchor, constructs the metric AOI/PSU/SSU geography, records retrieval outcomes and unresolved work, runs the geometry audit, and produces a baseline Traveling Archive for the STEP00 to STEP00.5 handoff.

## Repository paths

```text
index.html
README.md
steps/STEP00/AaP3Km_STEP00_ExplorePlace_MapFirst.html
Earth/{MGRS_PLACE_CODE}/{FULL_VERSIONED_ARCHIVE_FILENAME}
```

## Current Traveling Archive targets

```text
Earth/10TDQ772346/AaP3Km_10TDQ772346_TravelingArchive_OSUCorvallis_v004_UnfilledFocus_OptionalLabels_20260912.html
Earth/19TEK6001717522/AaP3Km_19TEK6001717522_WelcomeCenter_TravelingArchive_v1.4.1_MapDisplayFix_20260925.html
Earth/19TEJ5375298161/AaP3Km_19TEJ5375298161_BassHarbor_TravelingArchive_v1.4.0_ReaderFirstCumulative_20260901.html
Earth/21MXT6386590592/AaP3Km_21MXT6386590592_Obidos_Brazil_TravelingArchive_v1.16.0_UserFacingAuditClean_20260903.html
Earth/21MXT6386590592/AaP3Km_21MXT6386590592_Obidos_Brazil_TravelingArchive_v1.32.0_AdvancedSTEPHandoff_20260904.html
```

## Upload layout

Place each file at the exact path above. GitHub Pages paths are case-sensitive. Do not upload the versioned Welcome Center filename as the public entry point; rename `index_UPLOAD_20260926.html` to `index.html` during upload.

## Public-release boundary

The Welcome Center is an orientation and discovery layer. A Traveling Archive is a generated, read-only evidence carrier and is not independently authoritative. Open or unresolved evidence must remain explicit. Before publication, review personal information, credentials, private URLs, culturally sensitive material, editorial content, and redistribution or licensing constraints.
