# Personality System Audit — 2026-09-23

## Review target

The personality subsystem was reviewed after its first implementation to improve structure, isolation, source discipline, and activation behavior.

## Findings

1. The first version mixed framework analysis skills directly with routing and evidence utilities.
2. There was no explicit framework-selection layer.
3. Assessment administration was mixed into analysis concepts.
4. Evidence labels existed but needed a cleaner shared contract.
5. The subsystem needed a self-contained README and regression tests.

## Repairs

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

## Review result

PASS:
- dormant activation
- framework isolation
- framework selection
- assessment separation
- evidence control
- memory discipline

Remaining limitation:

Psychometric quality depends on the exact instrument used. The Skills architecture itself does not turn a weak instrument into a strong one.
