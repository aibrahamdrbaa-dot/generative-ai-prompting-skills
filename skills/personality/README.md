# Roy Personality & Behavioral Analysis Skills

This directory is an optional subsystem for personality and behavioral frameworks.

## Activation policy

DORMANT BY DEFAULT.

Nothing in this directory should load during ordinary conversations.

Activation requires:
1. an explicit request for personality or behavioral analysis/testing;
2. interpretation of a supplied assessment result; or
3. explicit adaptation of communication/workflow based on an already-known result.

A recognizable conversational pattern is not an activation trigger.

## Architecture

personality gate
-> framework selector
-> assessment adapter OR result interpreter
-> evidence control
-> contextual interpretation
-> optional user-requested adaptation
-> off-switch

## Frameworks

| Framework | Primary use | Representation |
|---|---|---|
| MBTI | preference/type exploration | four preference axes + type |
| DISC | behavior/communication | D/I/S/C profile |
| Big Five | trait-level personality description | continuous dimensions |
| Enneagram | motivation-oriented reflection | type + supporting pattern |
| Adult Attachment | relationship-pattern analysis | anxiety/avoidance dimensions |

## Non-equivalence

These frameworks are not interchangeable.

Do not automatically translate:
MBTI <-> DISC <-> Big Five <-> Enneagram <-> Attachment.

A conceptual similarity is not psychometric equivalence.

## Evidence hierarchy

1. Exact instrument documentation
2. Peer-reviewed psychometric evidence
3. Primary institutional/academic sources
4. Reputable secondary research
5. Community skills and prompt collections

Community repositories are useful for workflow ideas, not for establishing psychological validity.

## Output discipline

Always separate:
- measured result
- instrument facts
- user-provided examples
- framework interpretation
- Roy inference
- unknown/uncertain points

Do not turn a framework result into a fixed identity, diagnosis, or deterministic prediction.

## Persistence

Do not store inferred personality labels.

A user-confirmed result may be stored only with the framework/instrument and narrow scope.

Example:
User-reported MBTI result: [type], instrument/version: [source], date: [date].

Never store a causal personality claim such as:
User is X, therefore user thinks or acts Y.
