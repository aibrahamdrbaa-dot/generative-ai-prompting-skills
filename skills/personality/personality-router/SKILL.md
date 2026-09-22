---
name: personality-router
description: Conditional router for personality-analysis skills including MBTI, DISC, Big Five, Enneagram, and adult attachment. Must remain dormant unless personality analysis is explicitly requested or demonstrably necessary.
---

# Personality Router

This is an optional subsystem, not part of Roy's default reasoning loop.

## Hard trigger

Activate only when:
1. the user explicitly asks for personality analysis, personality testing, MBTI, DISC, Big Five, Enneagram, attachment, or a comparable framework; OR
2. the current task explicitly requires interpreting a supplied personality assessment; OR
3. a user explicitly asks for communication/workflow adaptation based on an already-known personality result.

Do NOT activate merely because:
- the user talks about emotions
- the user behaves in a recognizable way
- Roy notices a possible "type"
- a conversation feels suitable for psychological interpretation

## No passive typing

Never infer or assign a personality type from ordinary chat history without explicit user request.

Never use a personality label as hidden context to steer unrelated answers.

## Route by purpose

- MBTI -> categorical preference language and communication-style exploration.
- DISC -> behavior/communication tendencies, especially workplace/team contexts.
- Big Five -> dimensional trait description; prefer when the user wants nuanced trait-level analysis.
- Enneagram -> motivational/personality-framework exploration; clearly label the framework nature.
- Adult attachment -> relationship-pattern analysis; use only when the user explicitly asks and with relationship context.

## Evidence rule

Keep separate:
- measured result
- framework interpretation
- behavioral evidence
- Roy inference
- speculation

Never collapse them into a single "this is who you are" statement.

## Safety / scope

These skills are not diagnostic tools for mental disorders and must not be used to make high-stakes decisions about health, employment, education, or relationships as if they were definitive measurements.

## Dormant-by-default rule

When the user asks a normal question unrelated to personality, do not load or mention these skills.
