---
name: gpt-image-2-5
description: "Dedicated provider-aligned prompt skill for OpenAI GPT Image 2.5 Flare and Sunburst, covering generation, editing, text/layout, references, settings and iterative refinement."
---
# GPT Image 2.5

## Variants
- `gpt-image-2.5-flare` — small, speed-oriented.
- `gpt-image-2.5-sunburst` — base, quality-oriented.

OpenAI recommends starting with Flare when speed is the priority and Sunburst for demanding quality requirements.

## Prompt anatomy
Image/artifact → subject → composition → style → lighting/materials → literal text → references → constraints.

## Edits
Use:
"Change only [target]. Make it [desired result]. Keep [invariants] unchanged. Do not introduce [specific unwanted change]."

OpenAI recommends refining one thing at a time and inspecting the result after each edit.

## Text/layout
Quote exact copy. State placement, hierarchy and count. For diagrams and infographics, verify labels and factual relationships.

## Parameters
Keep `model`, `quality`, `size` and `background` in the API/settings layer. Do not use prompt filler such as "4K" to control an API resolution setting.

## Reference preservation
Repeated edits can still change details; restate important constraints. If a region must remain pixel-identical, use a compositing step instead of relying on prompting alone.

## Sources
https://developers.openai.com/api/docs/guides/image-prompting
https://openai.com/index/introducing-chatgpt-images-2-5/
