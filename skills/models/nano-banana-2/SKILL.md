---
name: nano-banana-2
description: Provider-aligned adapter for Nano Banana 2 / Gemini 3.1 Flash Image image generation and editing.
---

# Nano Banana 2

Official model ID: gemini-3.1-flash-image.

## Route here when

- general image generation/editing
- fast visual iteration
- multiple references
- subject consistency
- text-rich visual work
- high-resolution image work
- grounded visual tasks where supported

## Position in the system

Treat Nano Banana 2 as the broad image workhorse: it balances speed and capability breadth. Use Nano Banana Pro when the brief is dominated by complex interacting constraints.

## Prompt anatomy

finished visual/purpose -> subject -> composition -> reference roles -> visual treatment -> lighting/materials -> exact text -> preserve/change/exclude

Start with the highest-signal visual constraint.

## References

Give each input one authority:
- identity
- geometry
- pose
- composition
- style
- environment
- layout

If references conflict, resolve the conflict explicitly.

## Editing

Use targeted verbs:
change X; keep Y and Z unchanged.

Do not ask for a broad transformation when only one region should change.

## Text

Quote exact text. State hierarchy and placement. Do not invent factual labels, numbers, signage, or branding.

## Resolution and aspect

Current Google documentation supports multiple output resolutions/aspect choices, including 4K in supported surfaces. Treat these as execution settings, not prompt adjectives.

## Grounding

When current real-world facts matter and supported grounding is available, use it rather than fabricating factual visual details.

## Iteration

Prefer small, isolated refinements. Preserve successful properties from the previous result.

## Sources

- https://ai.google.dev/gemini-api/docs/models/gemini-3.1-flash-image
- https://ai.google.dev/gemini-api/docs/image-generation
