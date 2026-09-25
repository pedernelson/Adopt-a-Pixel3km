# AaP3Km GitHub, STEP, and Traveling Archive Control Instructions

**Version:** v001  
**Date:** 2026-09-25  
**Audience:** AaP3Km investigators, eGEOG580 students, Course Assistant, Instructor, reviewers, and repository maintainers  
**Status:** Proposed controlling workflow for review and adoption

## 1. Purpose

GitHub controls the accepted investigation state for each durable Place. The STEP HTML files control how evidence and interpretation are created, reviewed, assembled, and prepared for check-in. Traveling Archive HTML files are versioned, read-only representations of the investigation state. The Visitor Center presents reviewed public representations.

These are separate roles:

```text
Physical Place
→ MGRS Place namespace in GitHub
→ checked-out Traveling Archive
→ STEP HTML work session
→ STEP export and session ledger
→ check-in candidate
→ review
→ accepted non-overwriting descendant
→ optional reviewed public representation
```

A STEP HTML file is not the repository. A Traveling Archive is not independently authoritative. GitHub is the accepted source of truth.

## 2. Controlling principles

1. Begin with the physical Place.
2. Use the MGRS Place Code as the durable namespace.
3. Retain latitude and longitude as authoritative coordinates.
4. Carry one Place Grounding Package through all STEPs.
5. Preserve source-native schemas and provenance.
6. Keep requests, returned data, accepted evidence, interpretation, and claims distinct.
7. Never overwrite a parent archive.
8. Every accepted update is a descendant with parent identity and SHA-256.
9. Unresolved work may continue downstream as explicit open work.
10. GitHub commits, reviews, and releases occur outside the browser-based STEP files.

## 3. System roles

### Canonical `AaP3Km` GitHub repository

Controls:

- Place namespaces;
- accepted Place Docket and Place Grounding;
- STEP releases;
- schemas and controlled vocabularies;
- evidence, source, uncertainty, claim, citation, and provenance ledgers;
- archive registry and lineage;
- review records;
- accepted Traveling Archive descendants;
- release decisions.

### STEP00–STEP11 HTML files

Control investigation actions and data creation within a checked-out session. They must preserve the shared session ledger and return structured exports that can be reviewed and checked into GitHub.

### Traveling Archive HTML

A read-only, result-centered carrier of:

- Place identity and support geometry;
- accepted and unresolved evidence;
- investigation roadmap;
- findings, interpretations, and claim boundaries;
- provenance and citation records;
- parent-child lineage;
- future observations and reSearch questions.

### `Adopt-a-Pixel3km` Visitor Center

Presents reviewed public artifacts. It does not determine canonical scientific state.

## 4. GitHub Place structure

Established canonical root:

```text
Earth/
└── {MGRS_PLACE_CODE}/
    ├── PLACE_DOCKET/
    └── PLACE_GROUNDING/
```

Recommended controlled additions, to be adopted in the repository standard:

```text
Earth/
└── {MGRS_PLACE_CODE}/
    ├── PLACE_DOCKET/
    ├── PLACE_GROUNDING/
    ├── INVESTIGATION/
    │   ├── investigation.yml
    │   ├── module_status.yml
    │   └── research_queue.yml
    ├── LEDGERS/
    │   ├── session_ledger.json
    │   ├── source_ledger.csv
    │   ├── observation_ledger.csv
    │   ├── uncertainty_ledger.csv
    │   ├── claim_ledger.csv
    │   ├── citation_ledger.csv
    │   └── provenance_ledger.csv
    ├── ARCHIVES/
    │   ├── parents/
    │   ├── candidates/
    │   └── accepted/
    ├── REVIEWS/
    └── RELEASES/
```

Until these additions are formally adopted, do not silently invent competing directories. Preserve the MGRS namespace and document the exact path used.

## 5. STEP-to-archive control model

The repository contains STEP00, STEP00.5, and STEP01–STEP11 releases. The STEP suite collectively controls the end-to-end investigation. The exact scientific purpose of a STEP is controlled by its current release documentation and embedded schema, not by this guide alone.

The workflow roles below are authoritative where already established and otherwise are proposed control functions to verify against the current STEP release before adoption.

| STEP | Controlling function | Required contribution to the Traveling Archive |
|---|---|---|
| STEP00 | Initiate or re-enter a Place investigation; establish parent and baseline readiness | Place identity, parent identity/hash, session identity, archive baseline, initial status records |
| STEP00.5 | Orchestrate Place evidence discovery and support-aware retrieval | Request records, returned-source inventory, intersection/support records, explicit failure or zero-result states |
| STEP01 | Map User interpretation and labeling | SSU interpretation records, imagery provenance, review state, unresolved/non-labelable states, fractions when valid |
| STEP02 | Human/GLOBE observation review | Measurement coordinates, reported accuracy, photo manifests, direction, field evidence, support candidates, claim boundaries |
| STEP03 | Assemble archive state and check-in candidate | Consolidated read-only candidate, session-ledger compilation, candidate filename/version, parent linkage |
| STEP04 | Review and reconciliation gate | Accepted/rejected/revised records, correspondence gates, adjudication history, unresolved queue |
| STEP05 | Map Producer comparison and fit-for-use evaluation | Product/version records, native support, comparison populations, agreement/disagreement, omissions, fit-for-use boundaries |
| STEP06 | Landsat-era and spectral-time interpretation | Quality-screened trajectories, vertices/segments, stable/change evidence, H0 state, alternate explanations |
| STEP07 | Additional observer or evidence-lane integration | Source-specific measurement records and support relationships, with no silent relabeling |
| STEP08 | Thermal, structural, radar, lidar, elevation, or advanced measurement integration | Units, acquisition geometry/time, native support, QA, vertical target, derived outputs, limitations |
| STEP09 | Open-science and archive-readiness audit | Provenance, citations, reproducibility, disclosure, rights, accessibility, full-population accounting |
| STEP10 | Place Biography synthesis and scientific communication | Findings, working interpretations, claim boundaries, figures/tables, narrative synthesis, leading reSearch questions |
| STEP11 | Transfer, release, and future-watch preparation | Review disposition, second-Place transfer notes, release decision, future watches, final accepted descendant package |

**Important:** If a current STEP HTML release defines a different function, the repository release documentation wins. Update this table through a reviewed documentation change rather than changing practice informally.

## 6. Shared reSearch session ledger

Every STEP contributes records to one shared session ledger. A new STEP does not start a separate investigation.

Minimum session fields:

```text
session_id
place_code
parent_archive_filename
parent_archive_sha256
parent_archive_version
current_step
step_release_filename
step_release_sha256
operator_or_contributor
session_started_utc
session_updated_utc
geometry_identity
geometry_sha256
records_imported
records_created
records_revised
records_unresolved
requests_attempted
requests_failed
successful_zero_results
data_returned
accepted_for_interpretation
excluded_with_reason
claim_boundaries_added
research_queue_items_added
candidate_archive_filename
candidate_archive_sha256
```

Each ledger event records:

```text
event_id
event_time_utc
step
module_or_investigation_stage
action
input_artifact
input_sha256
output_artifact
output_sha256
evidence_status
support
source_role
interpretation_role
claim_boundary
review_state
notes
```

## 7. Evidence-state vocabulary

Use only:

```text
NOT_ATTEMPTED
ATTEMPTED_FAILED
SUCCESS_ZERO_RESULTS
CANDIDATE_SOURCE_FOUND
DATA_RETURNED_NOT_REVIEWED
ACCEPTED_FOR_INTERPRETATION
EXCLUDED_WITH_REASON
UNRESOLVED_OPEN_REQUIRED
NOT_APPLICABLE
```

Prepared request JSON is not observational evidence. A catalog link is not returned data. Returned data is not automatically accepted interpretation.

## 8. Student instructions

### Before opening a STEP

1. Obtain the current parent Traveling Archive from the location specified in the module.
2. Record its full filename, version, byte count, and SHA-256 when supplied.
3. Confirm the MGRS Place Code and AOI center point.
4. Confirm the STEP HTML release filename specified by the module.
5. Create no replacement files using the parent filename.
6. Keep source files and parent archive unchanged.

### During the STEP session

1. Import the parent archive and required evidence files.
2. Confirm that the displayed Place Code, geometry, and record counts match the parent.
3. Perform only the investigation action assigned to the STEP and module.
4. Record requests even when they fail or return zero results.
5. Preserve raw returned values, QA, units, dates, supports, source IDs, and lineage.
6. Mark uncertainty and unresolved work explicitly.
7. Do not treat Map Producer classes or field observations as automatic Map User labels.
8. Add citations and source roles when evidence first enters the investigation.
9. Update the shared session ledger.
10. Export a new descendant and required handoff files.

### Before submission

Verify:

```text
[ ] Parent filename and hash are recorded.
[ ] Descendant filename is new.
[ ] MGRS Place Code is unchanged.
[ ] Geometry identity and counts reconcile.
[ ] Source and imagery provenance are present.
[ ] Every request has an explicit status.
[ ] Unresolved and non-labelable records remain explicit.
[ ] Findings are separated from working interpretations.
[ ] Claim boundaries state what is not established.
[ ] Citation and provenance records are current.
[ ] Accessibility checks are complete.
[ ] Files open locally.
```

### What students submit

Unless the module states otherwise:

1. a new read-only Traveling Archive descendant;
2. the STEP/session handoff export;
3. the module evidence report or response;
4. the one-page archive check-in record;
5. only specifically requested supporting artifacts.

Students do not commit directly to the accepted canonical branch unless explicitly authorized.

## 9. Instructor and repository-maintainer instructions

### Before publishing a module

1. Identify the approved STEP release.
2. Identify the approved parent or baseline archive.
3. State the module's investigation question and expected archive contribution.
4. Publish exact input and output filenames, schemas, and status vocabulary.
5. State the approved fallback for external-service failure.
6. Provide accessibility and disclosure requirements.
7. Test the STEP with the supplied parent and sample evidence.

### Intake review

Perform an operational review before scientific interpretation:

```text
file opens
filename/version
parent-child lineage
MGRS Place identity
expected row and feature counts
geometry identity/hash
missing or duplicate IDs
status vocabulary
imagery/source provenance
fraction reconciliation
accessibility checklist
```

Then perform scientific review:

```text
support correspondence
same-Place and same-time gates
label-dictionary or class adjudication
spectral interpretation
fit-for-use conclusions
hypothesis decision
claim boundaries
release suitability
```

### STEP03 and STEP04 control

STEP03 assembles a check-in candidate. STEP04 reviews and reconciles it. An accepted result is committed externally to GitHub as a non-overwriting descendant. The browser STEP does not itself make the canonical commit.

### Public release

A technically complete archive is not automatically public. Confirm:

- scientific review;
- authorship/contributor review;
- accessibility;
- privacy and sensitive-Place review;
- redistribution rights and licenses;
- exact-coordinate suitability;
- archive and source hashes;
- Visitor Center link and README consistency.

## 10. GitHub branch and pull-request workflow

Recommended branch:

```text
investigation/{MGRS_PLACE_CODE}/{STEP-or-MODULE}/{short-purpose}
```

Example:

```text
investigation/19TEK6001717522/STEP05/worldcover-reconciliation
```

Pull-request title:

```text
{MGRS_PLACE_CODE} · {STEP} · {purpose}
```

Pull-request description records:

```text
Parent artifact
Parent SHA-256
STEP release
STEP release SHA-256
Investigation stage
Question addressed
Evidence added
Evidence revised
Evidence excluded
Zero results and failures
Findings proposed
Claim boundaries retained or added
Unresolved work
Validation results
Disclosure/accessibility/rights state
Expected descendant filename
```

The accepted branch should require review and passing validation checks. Do not force-push or delete accepted history.

## 11. Required validation before acceptance

Automated or repeatable checks should verify:

- valid MGRS path;
- existing parent and matching hash;
- new descendant filename;
- no parent overwrite;
- required archive sections;
- parseable embedded JSON;
- map initialization;
- expected AOI/PSU/SSU counts;
- controlled status values;
- reconcileable ledgers;
- internal links;
- accessibility checks;
- disclosure and rights declarations;
- coordinated update of public `index.html` and `README.md` when the public target changes.

Human review is required for thematic labels, scientific interpretation, attribution, correspondence judgments, fit-for-use conclusions, and release approval.

## 12. Archive registry

Each archive record should include:

```yaml
place_code: 19TEK6001717522
artifact_filename: AaP3Km_19TEK6001717522_WelcomeCenter_TravelingArchive_v1.4.1_MapDisplayFix_20260925.html
artifact_sha256: f500a44f789e864667d4e052bd176c78d4dfe4241addbbcdd1680a8a2f171823
parent_filename: AaP3Km_19TEK6001717522_WelcomeCenter_TravelingArchive_v1.4.0_ReaderFirstCumulative_20260901.html
parent_sha256: 7f3e8a17d9379e2281b41e72746d627e141e6e0ff239e9e9dd79d9a3d07655db
artifact_role: reviewed_descendant
evidence_maturity: substantial
interface_maturity: reader_first
public_target: true
release_state: reviewed
```

The Visitor Center should be updated from reviewed registry records, not from an independently maintained list of filenames.

## 13. GitHub Issues as reSearch queue

Each unresolved scientific or technical question should have:

```text
Place Code
STEP or module
Question
Affected support
Evidence needed
Current evidence state
Blocker
Expected descendant
Review type
```

The Traveling Archive may show the five leading questions. GitHub holds the complete operational queue.

## 14. Responsibilities summary

### Student or contributor

- operates the assigned STEP;
- preserves parent and source files;
- creates traceable evidence and a new descendant;
- records uncertainty, citations, and provenance;
- submits a check-in candidate.

### Course Assistant or operational reviewer

- checks file integrity, naming, lineage, identity, counts, controlled statuses, provenance completeness, and accessibility checklist.

### Instructor or scientific reviewer

- reviews scientific interpretation, correspondence, mixed-cover decisions, hypotheses, claim boundaries, release suitability, and final acceptance.

### Repository maintainer

- merges accepted records;
- protects canonical history;
- updates registries and releases;
- coordinates public index and README changes;
- preserves hashes and lineage.

## 15. Immediate repository changes

Add or update:

```text
docs/AaP3Km_GitHub_STEP_TravelingArchive_Control_Instructions_v001_20260925.md
docs/AaP3Km_TravelingArchive_Orientation_Growth_Template_v002_UniversalModules_20260925.md
.github/pull_request_template.md
.github/ISSUE_TEMPLATE/research-question.yml
schemas/session-ledger.schema.json
schemas/archive-registry.schema.json
ARCHIVE_REGISTRY.yml
MODULE_REGISTRY.yml
```

Before changing the five example archives, register each parent/descendant and map it to the applicable STEP/module contributions.
