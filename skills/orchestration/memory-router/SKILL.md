---
name: memory-router
description: Decides when visual workflow knowledge should be retrieved from or promoted to Supermemory, while preserving container isolation and provenance.
---

# Memory Router

Supermemory is the durable learning layer, not the source of truth for live provider capabilities.

## Retrieve before execution when

- the task resembles a previously solved visual workflow
- a model-specific failure may have a known correction
- a recurring character, brand, room, product, or visual world has a stored Visual Bible
- Ibrahim has a durable preference that changes visual decisions
- the router needs a previously verified skill combination

Use the correct container:
- agent:roy -> Roy-wide workflow rules and model lessons
- user:ibrahim -> durable user-specific preferences
- project container -> project-local visual systems and visual bibles

Never rely on an unscoped search to prove that memory does not exist.

## Promote after execution when

- the same failure recurs
- a correction is independently verified
- the user explicitly confirms a preference or rule
- a skill combination repeatedly improves the same class of task

## Do not store by default

- one-off prompts
- temporary drafts
- raw private source material
- guesses about model behavior
- unverified output quality judgments

## Memory record schema

task_class | model | skill_stack | observed_issue | correction | evidence | confidence | date | source

## Conflict rule

New evidence can supersede older workflow lessons. Preserve provenance and do not silently merge contradictory claims.
