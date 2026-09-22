---
name: generative-ai-prompting
description: Cross-model visual generation router for Gemini Omni 1.1 Flash, Nano Banana 2, Nano Banana Pro, and GPT Image 2.5. Normalizes the brief, chooses the task-fit model, compiles provider-specific instructions, stacks only triggered skills, then runs QA and controlled iteration.
---

# Generative AI Prompting Router

This is the entry point for every visual-generation request.

## Core pipeline

brief -> modality -> operation -> model route -> skill stack -> prompt compilation -> generation -> QA -> surgical iteration -> memory update

Never jump directly from a vague user request to a model prompt when the task is non-trivial.

## 1. Normalize the brief

Capture only what is known or explicitly requested:
- deliverable: image / video / image-to-video / video edit / extension / transition
- operation: generate / edit / inpaint / outpaint / composite / transform / extend
- subject and action
- environment and spatial relationships
- style or visual language
- references and the role of each reference
- literal text that must appear
- composition, framing and aspect ratio
- lighting, materials and color
- continuity constraints
- audio requirements for video
- must-change / must-preserve / must-avoid constraints

Do not invent missing factual details.

## 2. Route by task fit

Use task-fit rules, not an overall quality ranking.

| Need | Route |
| --- | --- |
| Video generation, image-to-video, reference-to-video, conversational video edit, extension, frame transition | Gemini Omni 1.1 Flash |
| General image generation/editing, fast iteration, multi-reference composition, consistency, high-resolution image work | Nano Banana 2 |
| Dense constraints, professional assets, grounding/localization, brand-sensitive or complex layouts | Nano Banana Pro |
| GPT Image 2.5 workflow; choose Flare when latency matters, Sunburst when image quality/detail matters | GPT Image 2.5 |
| Existing image must be preserved while making one targeted change | Add Visual Editing + Reference Manager regardless of model |
| Video with planned shots | Add Video Storyboard + Visual Bible + Cinematic when triggered |

Important: model routing is task-fit, not a global best-model ranking.

## 3. Load the smallest useful skill stack

Core:
- Visual Brief for ambiguous or multi-constraint requests
- Model Router
- Prompt Compiler

Conditional:
- Reference Manager when references exist
- Visual Bible for cross-shot or recurring identity
- Video Storyboard for multi-shot video
- Typography & Layout when text/layout is material
- Visual Editing for edits
- Image-to-Prompt when reverse-engineering a reference
- Specialty when domain correctness changes the output
- Style only when style affects the requested look
- Quality Gate before final delivery
- Iteration Controller after a failed or partial result

Do not load every style or general skill by default.

## 4. Prompt compilation

The common brief is source-of-truth. Each model skill translates it into provider-native language.

Never assume that identical prompts behave identically across providers.

The compiled prompt must preserve:
- exact requested content
- reference roles
- must-preserve constraints
- literal text
- requested composition
- requested motion/timing/audio for video

Provider-specific wording may change; user intent may not.

## 5. Preflight

Before generation, check:
- model compatibility with modality and operation
- current provider limits on reference inputs
- current aspect ratio/resolution support
- literal text integrity
- edit invariants
- grounding needs
- video shot/motion/timing constraints
- regional or feature restrictions that apply to the chosen provider surface

If a restriction blocks the exact operation, explain it and reroute only when the alternate preserves the intended result.

## 6. Final review

Inspect:
- subject identity and count
- composition and spatial relationships
- text spelling and placement
- reference fidelity and role separation
- material/lighting continuity
- motion plausibility and shot continuity
- audio requirements
- domain correctness
- accidental additions
- output settings

Use Iteration Controller for one-dimension-at-a-time correction.

## 7. Memory learning

After meaningful work, record only reusable lessons:
- task pattern
- chosen route
- useful skill stack
- observed failure
- successful correction
- confidence/provenance
- date/version

Store durable workflow lessons in Supermemory under the appropriate container. Do not store transient prompts or private source material by default.

## 8. Hard rule

Provider execution success is not proof of visual correctness.
Aesthetic appeal is not proof of task compliance.
One lucky success is not proof of a reusable rule.
