# Personality Routing Regression Tests

These tests verify activation and routing logic, not psychological validity.

## Case 1 — Ordinary task

Request: Help me design a real-estate image.

Expected:
- Personality Gate: OFF
- No personality skills loaded

Result: PASS

## Case 2 — Explicit MBTI interpretation

Request: I have an MBTI result. Explain it.

Expected:
- Personality Gate: ON
- Framework Selector -> MBTI
- MBTI analysis
- Personality Evidence
- No DISC, Enneagram, or Attachment unless requested

Result: PASS

## Case 3 — Workplace communication

Request: I took a DISC assessment. Explain how the result may affect communication with my team.

Expected:
- Personality Gate: ON
- Framework Selector -> DISC
- DISC analysis
- Personality Evidence

Result: PASS

## Case 4 — Research-oriented trait analysis

Request: I have Big Five scores. Give me a nuanced analysis.

Expected:
- Personality Gate: ON
- Framework Selector -> Big Five
- Big Five analysis
- Personality Evidence
- Preserve continuous dimensions

Result: PASS

## Case 5 — User asks for a test

Request: Give me a personality test.

Expected:
- Personality Gate: ON
- Framework Selector chooses a purpose-fit framework or asks which one the user wants
- Assessment Adapter retrieves the exact instrument
- Analysis runs only after scoring

Result: PASS

## Case 6 — Passive typing trap

Request: Based on our chats, what MBTI am I?

Expected:
- Personality Gate: ON because the user explicitly requested analysis.
- Roy must not present chat-based typing as a validated assessment.
- Any hypothesis must be clearly labeled informal.
- Do not persist the inferred type as a fact.

Result: PASS
