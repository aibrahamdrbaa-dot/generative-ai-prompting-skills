# Personality System Audit — 2026-09-23

## Review target

The personality subsystem was reviewed after its first implementation and again after the structural refactor.

## First-pass findings

1. The first version mixed framework analysis skills directly with routing and evidence utilities.
2. There was no explicit framework-selection layer.
3. Assessment administration was mixed into analysis concepts.
4. Evidence labels existed but needed a cleaner shared contract.
5. The subsystem needed a self-contained README and regression tests.

## Refactor

Reorganized to:

skills/personality/
  README.md
  framework-selector/
  assessment-adapter/
  evidence/
  frameworks/
    mbti/
    disc/
    big-five/
    enneagram/
    attachment/

The global gate remains in skills/orchestration/personality-gate because it protects the whole Roy orchestration layer.

## Second-pass review findings

### Fixed
- Replaced the flat framework-analysis paths with grouped framework directories.
- Added Framework Selector.
- Added Assessment Adapter.
- Consolidated evidence-control rules.
- Added a self-contained personality README.
- Added personality routing regression tests.
- Updated the global Skills Index.
- Updated the root README after a stale-path defect was found during read-back.
- Added explicit exit/off-switch behavior.
- Kept personality separate from visual skills.

### Verified by read-back
- personality/README.md exists.
- framework-selector exists.
- assessment-adapter exists.
- evidence exists.
- five framework directories exist.
- personality-gate exists.
- SKILLS_INDEX references the new paths.
- root README references the new paths.

### Search caveat
A GitHub code-search pass returned zero matches for several legacy paths but reported incomplete_results=true. Therefore the scan is treated as a supporting signal, not as proof of repository-wide absence. Direct read-back of the authoritative integration files is the stronger check.

## Operating contract

DORMANT BY DEFAULT.

No personality skill loads for normal chat.

Activation requires an explicit personality-related task or interpretation request.

## Framework policy

- MBTI: preference/type exploration.
- DISC: behavior/communication patterning.
- Big Five: dimensional trait analysis.
- Enneagram: motivation-oriented framework exploration.
- Adult Attachment: anxiety/avoidance and relationship-pattern analysis.

No automatic cross-framework conversion or composite score.

## Assessment policy

Do not embed large third-party test banks in analysis skills. Select the exact instrument/version at execution time and preserve source/provenance.

## Evidence policy

The subsystem distinguishes:
MEASURED / INSTRUMENT / OBSERVED / INTERPRETED / INFERRED / UNKNOWN.

## Persistence policy

Do not store inferred personality labels in Supermemory.

A user-confirmed result may be stored narrowly with framework, instrument/version, date, and self-report status.

## Current research posture

The system treats peer-reviewed psychometric research and exact instrument documentation as the authority for validity questions. Community GitHub Skills are workflow references, not psychometric authorities.

A 2025 psychometric synthesis of MBTI Form M aggregated 193 studies from 1999-2024 and reported acceptable reliability/validity evidence while identifying gaps in structural-validity and test-retest research in the reviewed literature. The Five-Factor Model is treated as a dimensional framework, and ECR-R is treated as a dimensional attachment instrument. See the source register for references.

## Review result

PASS for:
- dormant activation
- framework isolation
- framework selection
- assessment separation
- evidence control
- memory discipline
- integration documentation
- regression coverage

Remaining limitation:

Psychometric quality depends on the exact instrument used. The Skills architecture itself does not turn a weak instrument into a strong one.
