---
name: visual-brief
description: Converts a natural-language visual request into a structured production brief shared by image and video workflows.
---

# Visual Brief

Use this before model routing when the request contains multiple constraints, references, edits, or a production goal.

## Output contract

Produce a compact brief with:
deliverable | operation | subject | environment | composition | style | lighting | references | text | constraints | audio | continuity

Mark fields as confirmed, inferred, or unknown.

## Rules

- Preserve the user's intent; do not decorate the brief with invented facts.
- Separate factual requirements from aesthetic preferences.
- Convert vague adjectives into observable visual decisions when enough context exists.
- For edits, explicitly list what must remain unchanged.
- For video, distinguish scene design from motion design.

## Video brief addition

For each shot capture:
- duration target
- shot size
- camera position/movement
- subject movement
- environmental movement
- transition relationship
- dialogue / voice / music / SFX requirements

If the video is a single continuous shot, say so rather than inventing a multi-shot storyboard.
