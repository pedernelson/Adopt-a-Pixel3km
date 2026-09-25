# Adopt-a-Pixel 3 km Digital Visitor Center

**Live site:** [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

This repository is the public presentation and discovery layer for Adopt-a-Pixel 3 km (AaP3Km). The separate [AaP3Km repository](https://github.com/pedernelson/AaP3Km) remains the canonical architecture and accepted-record system.

## Repository organization

Place-specific artifacts preserve the durable MGRS Place namespace:

```text
Earth/{MGRS_PLACE_CODE}/{FULL_VERSIONED_ARTIFACT_FILENAME}
```

Human-readable Place names appear in page titles and discovery cards but do not replace MGRS Place Codes.

## Current public Traveling Archives

- `Earth/10TDQ772346/` · Corvallis and Oregon State University
  - `AaP3Km_10TDQ772346_TravelingArchive_OSUCorvallis_v004_UnfilledFocus_OptionalLabels_20260912.html`
- `Earth/19TEJ5375298161/` · Bass Harbor
  - `AaP3Km_19TEJ5375298161_BassHarbor_TravelingArchive_v1.4.0_ReaderFirstCumulative_20260901.html`
- `Earth/19TEK6001717522/` · Acadia Welcome Center
  - Current Visitor Center target: `AaP3Km_19TEK6001717522_WelcomeCenter_TravelingArchive_v1.4.1_MapDisplayFix_20260925.html`
  - Preserved parent: `AaP3Km_19TEK6001717522_WelcomeCenter_TravelingArchive_v1.4.0_ReaderFirstCumulative_20260901.html`
- `Earth/21MXT6386590592/` · Óbidos, Brazil
  - `AaP3Km_21MXT6386590592_Obidos_Brazil_TravelingArchive_v1.16.0_UserFacingAuditClean_20260903.html`
  - `AaP3Km_21MXT6386590592_Obidos_Brazil_TravelingArchive_v1.32.0_AdvancedSTEPHandoff_20260904.html`

## Coordinated repair record

The Acadia Welcome Center map-display repair is a non-overwriting descendant. The Visitor Center homepage and this README now identify v1.4.1 as the current public target while preserving v1.4.0 as its parent.

## Project standards

- [`docs/AaP3Km_PROJECT_STYLE_GUIDE_v003.md`](docs/AaP3Km_PROJECT_STYLE_GUIDE_v003.md)
- [`docs/AaP3Km_TRAVELING_ARCHIVE_PUBLIC_CONTRACT_v002.md`](docs/AaP3Km_TRAVELING_ARCHIVE_PUBLIC_CONTRACT_v002.md)
- [`docs/AaP3Km_TRAVELING_ARCHIVE_MIGRATION_PLAN_v002.md`](docs/AaP3Km_TRAVELING_ARCHIVE_MIGRATION_PLAN_v002.md)

A Traveling Archive is a checked-out reSearch working object, not an independent source of truth. New interpretations and repairs become non-overwriting descendants with explicit parent lineage.
