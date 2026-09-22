---
name: iteration-controller
description: Diagnoses visual-generation failures and applies one controlled correction at a time.
---

# Iteration Controller

Do not rewrite everything after every failure.

## Diagnose first

Classify the failure:
- subject
- identity
- composition
- spatial relation
- reference fidelity
- text
- style
- lighting
- material
- motion
- timing
- audio
- domain correctness
- accidental addition

## Patch rule

Change the smallest instruction set that can plausibly fix the observed failure.

Preserve all successful dimensions.

## Loop

observe -> classify -> patch one dimension -> regenerate -> compare

Stop when:
- the task is satisfied, or
- a provider limitation is the bottleneck, or
- further changes would trade one requirement for another.

Record successful patches that generalize in Supermemory.
