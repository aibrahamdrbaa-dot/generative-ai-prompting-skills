---
name: assessment-adapter
description: Handles personality test administration as a source-aware execution layer, retrieving the exact instrument and scoring rules instead of embedding large or uncertain test banks in analysis skills.
---

# Assessment Adapter

Use only when the user explicitly asks to take a personality assessment.

## Workflow

1. Identify the requested construct/framework.
2. Identify the exact instrument and version.
3. Check source, license/usage conditions, scoring instructions, and intended population.
4. Retrieve the test material from a suitable authoritative source when available.
5. Keep administration separate from interpretation.
6. Do not reveal scoring keys before completion when that could bias responses.
7. Validate response count, scale range, reverse-scored items, and missing values.
8. Compute scores using the instrument's own scoring rules.
9. Preserve raw scores and instrument metadata with the result.
10. Pass the result to the relevant framework analysis skill.

## Important

Never assume that:
- all MBTI tests are equivalent;
- all DISC tests are equivalent;
- a short online quiz has the same validity as the named instrument;
- categorical cutoffs transfer between instruments.

## Copyright and licensing

Do not embed or redistribute large third-party item banks in this skill merely for convenience. Retrieve or reference the legitimate instrument/source when needed.
