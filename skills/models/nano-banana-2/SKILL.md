---
name: nano-banana-2
description: "Dedicated provider-aligned prompt skill for Nano Banana 2 / Gemini 3.1 Flash Image: generation, editing, multi-reference composition, text-heavy layouts and grounded visual tasks."
---
# Nano Banana 2

## Provider identity
Official model ID: `gemini-3.1-flash-image`.

## Use it for
General image generation/editing, multi-reference compositions, consistency workflows, text-rich visuals, fast iteration and search-grounded visual tasks.

## Prompt anatomy
Finished artifact + purpose → subject → composition → references and their roles → visual treatment → lighting/materials → text/layout → preserve/change → exclusions.

## References
Assign each input a specific authority:
- architecture;
- product geometry;
- person/character identity;
- pose;
- style;
- environment;
- layout.

When roles conflict, specify which reference wins for each property.

## Text
Give exact text in quotation marks and define placement/hierarchy. Avoid inventing factual labels, statistics or signage.

## Editing
Use targeted changes and protect established geometry, subject identity and composition.

## Resolution/aspect
Nano Banana 2 supports 0.5K, 1K, 2K and 4K outputs and additional extreme aspect ratios. Put these choices in the request settings, not in decorative prompt prose.

## Grounding
When current real-world content matters, use supported Search Grounding rather than fabricating facts.

## Sources
https://ai.google.dev/gemini-api/docs/models/gemini-3.1-flash-image
https://ai.google.dev/gemini-api/docs/image-generation
