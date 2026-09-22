---
name: model-router
description: Selects the model or model variant that fits the requested visual operation, modality, constraints, and iteration pattern.
---

# Model Router

The router chooses by capability fit.

## Route order

1. Determine modality.
2. Determine operation.
3. Identify the hardest constraint.
4. Identify whether references, text, continuity, grounding, or motion dominate.
5. Select the provider/model adapter.
6. Record a reason code.

## Reason codes

- VIDEO_NATIVE
- IMAGE_GENERALIST
- IMAGE_COMPLEX_CONSTRAINTS
- IMAGE_SPEED
- IMAGE_PRECISION_EDIT
- REFERENCE_HEAVY
- TEXT_LAYOUT
- GROUNDED_VISUAL
- CONTINUITY

## Model routes

### Gemini Omni 1.1 Flash
Primary route for video generation/editing workflows: text-to-video, image-to-video, reference-guided video, conversational editing, extensions, and first/last-frame transitions when the current provider surface supports the requested operation.

### Nano Banana 2
Primary image workhorse when the task needs strong general image generation/editing, multiple references, subject consistency, fast iteration, or high-resolution image work.

### Nano Banana Pro
Prefer for complex visual briefs, professional assets, dense constraints, localization/grounding, brand-sensitive work, and difficult layouts where more reasoning and fidelity are valuable.

### GPT Image 2.5
Use when the workflow specifically benefits from GPT Image 2.5. Route to Flare for latency-oriented work and Sunburst for higher image-quality/detail requirements.

## Tie-breakers

When two routes fit:
- motion beats image-only
- exact edit beats regeneration
- complex constraints beat generic generation
- continuity beats isolated aesthetics
- lower latency wins only when quality constraints are still met

Never produce a global model ranking.
