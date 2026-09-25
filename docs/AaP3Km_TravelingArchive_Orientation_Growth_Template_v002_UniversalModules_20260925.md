# AaP3Km Traveling Archive Orientation and Growth Template

**Version:** v002  
**Date:** 2026-09-25  
**Scope:** Reusable for eGEOG580, other courses, independent reSearch, public interpretation, and long-term Place stewardship.

## Core orientation

Every Traveling Archive should help a reader understand:

1. what already exists;
2. what is currently known, interpreted, or unresolved;
3. what information is planned for later investigation modules;
4. what was added or revised in the current descendant;
5. what evidence and questions carry forward.

The archive is one cumulative record rather than a collection of disconnected exercises.

## Persistent page header

```text
Adopt-a-Pixel 3 km Traveling Archive

[HUMAN-READABLE PLACE NAME]
[MGRS PLACE CODE]

AOI center point: [latitude, longitude]
AOI support: 3 km × 3 km
Sampling design: 37 PSUs and 3,700 SSUs
Current descendant: [full filename]
Parent archive: [full filename]
Current investigation stage: [Baseline / Module 1 / ... / Synthesis]
Evidence maturity: [Unresolved / Partial / Substantial / Reviewed]
Interface maturity: [Technical / Reader-first / Map-first / Handoff-ready]
Release state: [Working object / Check-in candidate / Reviewed / Public release]
```

## Persistent navigation

```text
Place
Research Question
Investigation Roadmap
Map
Evidence
Findings
Uncertainty
reSearch
Sources
Lineage
```

Navigation remains stable even when a section contains no evidence yet.

# 1. Place

## Existing information

```text
Place name
MGRS Place Code
AOI center point and coordinate role
Construction CRS
Exchange CRS
AOI boundary
37 PSU locations
3,700 SSU locations
SSU interpretation footprints
Known geographic names
Initial contextual description
```

## Information that may be added

```text
Verified Place-name sources
Survey, benchmark, cadastral, or coordinate history
Regional setting
Physical geography
Hydrology, terrain, vegetation, and climate context
Human Intent records
Human Experience records
Disclosure or sensitive-Place constraints
```

# 2. Research question and hypothesis

```text
Environmental question:
[What is being investigated at this Place?]

Evaluated support:
[AOI / selected PSUs / native pixels / observation supports]

Evaluated period:
[explicit dates or Not established]

H0:
No defensible spectral change is detected for the evaluated Place,
period, and support after accounting for quality, missing observations,
seasonality, sensor-era differences, scaling, and method.

H1:
Defensible spectral change is detected for the evaluated Place,
period, and support.

Current decision:
[Not evaluated / Supported / Not supported / Inconclusive]

Alternative explanations:
[list]
```

# 3. Investigation roadmap

This section distinguishes existing evidence from information planned for later modules.

| Investigation stage | Guiding question | Evidence or record added | State before completion |
|---|---|---|---|
| Baseline | What arrived with the parent archive? | Existing geometry, sources, observations, interpretations, open work, and lineage | Preserved from parent |
| Module 1 · Define the Place | What Place is being investigated? | MGRS identity, AOI/PSU/SSU geography, source ledger, observation inventory, and research question | Planned |
| Module 2 · Establish the observing-system record | How has this Place been observed through time? | Mission and product records, retrieval requests, QA, cadence, gaps, and support comparison | Planned |
| Module 3 · Build spectral-time evidence | Is spectral change detectable? | Quality-screened trajectories, gaps, candidate intervals, and provisional H0 decision | Planned |
| Module 4 · Interpret visible/NIR evidence | What does suitable high-resolution reference evidence show? | Date-verified imagery, SSU interpretation, calibration records, and preliminary fractions | Planned |
| Module 5 · Relate composition and spectral behavior | How do composition and measured spectral behavior correspond? | PSU fractions, bands, indices, transformations, feature space, and endmember-prior cards | Planned |
| Module 6 · Evaluate Map Producer claims | What do existing mapped products claim about the Place? | Product versions, legends, native supports, correspondence gates, agreement, disagreement, and omissions | Planned |
| Module 7 · Connect human observation | What do observers record at the Place? | Field observations, photographs, direction, visibility, coordinate quality, notes, and field-to-satellite relationships | Planned |
| Module 8 · Add thermal and structural perspectives | What additional processes or structures are measured? | Thermal, radar, lidar, elevation, or other structural evidence with units, geometry, QA, and support | Planned |
| Module 9 · Audit reproducibility and archive readiness | Can another person reproduce and evaluate the work? | Complete SSU accounting, metadata, provenance, citations, disclosure, rights, accessibility, and data dictionary | Planned |
| Module 10 · Synthesize the Place Biography | What does the complete evidence chain support? | Findings, interpretations, boundaries, figures, tables, and narrative synthesis | Planned |
| Synthesis and transfer | Does the interpretation withstand review and transfer? | Corrected archive, defense or review, second-Place comparison, release decision, and future watches | Planned |

## Universal status labels

```text
PRESERVED_FROM_PARENT
ADDED_THIS_DESCENDANT
REVISED_THIS_DESCENDANT
PLANNED_FOR_LATER_MODULE
NOT_ATTEMPTED
ATTEMPTED_FAILED
SUCCESS_ZERO_RESULTS
DATA_RETURNED_NOT_REVIEWED
ACCEPTED_FOR_INTERPRETATION
UNRESOLVED_OPEN_REQUIRED
EXCLUDED_WITH_REASON
NOT_APPLICABLE
```

# 4. Current evidence state

| Evidence lane | Current state | Coverage | What it can support | Primary limitation | Contributing module or source |
|---|---|---|---|---|---|
| Place geometry | [state] | [coverage] | Place and support identity | [limitation] | Module 1 or parent |
| Source ledger | [state] | [coverage] | Provenance and source roles | [limitation] | Cumulative |
| Spectral-time record | [state] | [period] | Change evaluation | [limitation] | Modules 2–3 |
| SSU interpretation | [state] | [count of 3,700] | Composition and PSU fractions | [limitation] | Modules 4–5 |
| Map Producer evidence | [state] | [products/years] | Producer claims and fit for use | [limitation] | Module 6 |
| Human observation | [state] | [records/dates] | Field and observer evidence | [limitation] | Module 7 |
| Thermal evidence | [state] | [product/dates] | Emitted-energy context | [limitation] | Module 8 |
| Structural evidence | [state] | [product/dates] | Vertical or 3D context | [limitation] | Module 8 |
| Human Intent | [state] | [records/dates] | Plans and management context | [limitation] | Cumulative |
| Human Experience | [state] | [records/dates] | Community evidence | [limitation] | Cumulative |
| Interpretation History | [state] | [versions] | Revision and lineage | [limitation] | Every descendant |
| Open-science audit | [state] | [scope] | Reproducibility and release | [limitation] | Module 9 through synthesis |

# 5. Explore the Place

Every map includes a purpose, geographic extent, scale, data date, source, meaningful legend or direct labels, text summary, and accessible source table.

Default visible:

```text
orientation basemap when available
AOI boundary
37 unfilled PSU outlines
selected evidence layer
```

Default hidden:

```text
3,700 SSU centers
3,700 SSU footprints
PSU labels including PSU-00
Map Producer cells
modeled correspondence
contextual masks
```

Every selection reports identity, coordinate role, support, date/time, source/version, evidence state, QA, uncertainty, interpretation state, related records, and claim boundary.

# 6. Spectral-time record

## Existing orientation

```text
Mission timeline
Available product history
Usable observation period
Known temporal gaps
Existing trajectories
Existing interpretations
```

## Information that may be added

```text
Product and collection version
Evaluated support
Variables and transformations
Scale factors
QA and masking logic
Seasonal controls
Sensor-era handling
Trajectory figures
Candidate intervals
H0 decision history
Alternative explanations
```

# 7. SSU interpretation and fractions

```text
3,700 SSUs total

Accepted: [count]
Provisional: [count]
Unresolved: [count]
Revised: [count]
Non-labelable: [count]
Skipped with reason: [count]
```

Complete accounting does not require a confident thematic class for every SSU.

# 8. Map Producer claims

For each product, report product/version, producer, effective date, native support, legend, method, QA, validation evidence, Place intersection, comparison population, correspondence gates, fit-for-use statement, omissions, and claim boundary.

```text
Same Place: PASS / FAIL / UNRESOLVED
Same time: PASS / FAIL / UNRESOLVED
Support: PASS / FAIL / UNRESOLVED
Meaning: PASS / FAIL / UNRESOLVED
Quality: PASS / FAIL / UNRESOLVED

Thematic comparison enabled: YES / NO
```

# 9. Human observation

Each observation records protocol, observation ID, date/time, measurement coordinate, positional accuracy, support relationship, observer classification, notes, photographs, visibility, weather or surface condition, related remote-sensing evidence, interpretation status, and claim boundary.

# 10. Thermal and structural evidence

Each observer records mission/instrument, product/version, measurement domain, acquisition time, units, native footprint, viewing geometry, vertical target or reference surface, QA, Place intersection, derived output, interpretive role, limitations, and future-watch status.

# 11. Findings and claim boundaries

## Accepted findings

Directly supported by embedded and reviewed evidence.

## Working interpretations

Reasoned, source-linked, and revisable.

## Claim boundaries

What the current evidence does not establish.

# 12. Uncertainty and open work

Organize uncertainty consistently:

```text
Spatial
Temporal
Spectral
Thematic
Measurement
Geolocation
Support
Quality
Vocabulary
Processing
Interpretation
Disclosure
Licensing
Accessibility
Reproducibility
```

Show no more than five leading unresolved questions in the reader view. Preserve the complete queue in the payload.

# 13. Provenance, sources, and citations

Every source records source identity, source role, product/version applicability, project use, QA or validation role, limitations, and citation status.

Every archive records parent filename/hash, current filename/hash, generated date, embedded and linked files, services, software, material AI assistance, disclosure review, rights review, accessibility review, and release decision.

# 14. Final orientation panel

```text
This archive currently establishes:
[accepted findings]

This archive currently suggests:
[working interpretations]

This archive does not establish:
[claim boundaries]

The most important unresolved question is:
[question]

The next recommended observation is:
[observation]

The next descendant should add:
[evidence or artifact]
```

## Applicability

This module-based structure can function as:

- an eGEOG580 instructional sequence;
- a different course with renamed modules;
- an independent research workflow;
- a public reSearch pathway;
- a long-term stewardship and monitoring plan.

The archive reports actual evidence states. Modules describe an accumulation pathway, not a demand to populate evidence that does not exist.
