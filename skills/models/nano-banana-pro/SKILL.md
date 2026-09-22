---
name: nano-banana-pro
description: Provider-aligned adapter for Nano Banana Pro / Gemini 3 Pro Image complex image generation and editing.
---

# Nano Banana Pro

Official model ID: gemini-3-pro-image.

## Route here when

- complex visual briefs
- professional visual assets
- dense multi-constraint scenes
- branding-sensitive work
- localization
- factual/world-knowledge visual tasks
- difficult layouts
- high-fidelity reference-driven work

## Prompt anatomy

purpose/artifact -> subject -> reference authority -> composition -> environment -> material/color -> lighting -> typography/data -> preserve/change/exclude

## Complexity

Use this model when the task benefits from deliberate reasoning across many interacting constraints rather than simply adding more descriptive adjectives.

## Grounding

Separate:
- facts that must be correct
- visual interpretation
- stylistic invention

For geographic or factual visual tasks, ground the facts with the supported current tool surface before generation when needed.

## Brand work

Treat supplied brand assets and exact labels as protected inputs.

Do not invent extra logos, product names, signage, or claims.

## Complex layouts

Describe:
- hierarchy
- grid
- alignment
- spacing
- exact copy
- relationships between elements

Then verify the rendered relationships in the output.

## References

Assign authority by property. Do not let a style reference silently override geometry or identity.

## Resolution

Current Google documentation supports high-resolution image output including 4K in supported surfaces. Keep resolution as a provider setting when possible.

## Sources

- https://ai.google.dev/gemini-api/docs/models/gemini-3-pro-image
- https://ai.google.dev/gemini-api/docs/image-generation
