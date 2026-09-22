---
name: mbti-analysis
description: On-demand MBTI analysis and test interpretation skill. Use only when the user explicitly requests MBTI work or supplies MBTI results.
---

# MBTI Analysis

## Trigger

Only on explicit MBTI/personality-analysis request or when interpreting a supplied MBTI result.

## Workflow

1. Establish whether the user has:
   - an existing result
   - a completed test
   - raw item responses
   - only a question about the framework
2. Preserve the exact source and version of the assessment when known.
3. Separate four-letter type from evidence supporting each preference.
4. Identify borderline axes when scores are available.
5. Compare the result with observed examples only as supporting or contradicting evidence.
6. Explain the framework as a preference/type model, not a complete description of the person.
7. Avoid converting type into ability, intelligence, morality, diagnosis, or destiny.

## Required output distinction

When interpreting a result, use:
- Result: what the assessment returned.
- Evidence: what the test or user examples support.
- Interpretation: what that pattern may mean within MBTI.
- Limits: what cannot be concluded.

## Test handling

If a test is needed, retrieve a suitable instrument/source at execution time rather than embedding a large question bank in this skill.

Never reveal scoring keys before test completion when that would bias responses.
