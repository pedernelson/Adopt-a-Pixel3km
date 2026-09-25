# Adopt-a-Pixel 3 km Digital Visitor Center

**Live site:** [AaP3Km Digital Visitor Center](https://pedernelson.github.io/Adopt-a-Pixel3km/)

This repository is the public presentation and discovery layer for Adopt-a-Pixel 3 km (AaP3Km). The separate [`AaP3Km`](https://github.com/pedernelson/AaP3Km) repository remains the canonical architecture and accepted-record system.

## Repository organization

Place-specific artifacts preserve the durable MGRS Place namespace:

```text
Earth/{MGRS_PLACE_CODE}/{FULL_VERSIONED_ARTIFACT_FILENAME}
```

Human-readable Place names appear in page titles and discovery cards but do not replace MGRS Place Codes.

## Current public Traveling Archives

- `Earth/10TDQ772346/` · Corvallis and Oregon State University
- `Earth/19TEJ5375298161/` · Bass Harbor
- `Earth/19TEK6001717522/` · Acadia Welcome Center
- `Earth/21MXT6386590592/` · Óbidos, Brazil, with audited-baseline and advanced-handoff versions

## Project standards

- [`docs/AaP3Km_PROJECT_STYLE_GUIDE_v003.md`](docs/AaP3Km_PROJECT_STYLE_GUIDE_v003.md)
- [`docs/AaP3Km_TRAVELING_ARCHIVE_PUBLIC_CONTRACT_v002.md`](docs/AaP3Km_TRAVELING_ARCHIVE_PUBLIC_CONTRACT_v002.md)
- [`docs/AaP3Km_TRAVELING_ARCHIVE_MIGRATION_PLAN_v002.md`](docs/AaP3Km_TRAVELING_ARCHIVE_MIGRATION_PLAN_v002.md)

A Traveling Archive is a checked-out reSearch working object, not an independent source of truth. New interpretations become non-overwriting descendants with explicit parent lineage.
