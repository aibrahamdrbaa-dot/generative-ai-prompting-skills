---
name: gpt-image-2-5
description: Provider-aligned adapter for OpenAI GPT Image 2.5 Flare and Sunburst image generation/editing workflows.
---

# GPT Image 2.5

## Variants

- gpt-image-2.5-flare -> latency-oriented variant
- gpt-image-2.5-sunburst -> quality/detail-oriented variant

Choose the variant from the task constraint, not a global quality score.

## Route here when

- the task is an OpenAI GPT Image 2.5 image workflow
- targeted editing matters
- subject preservation matters
- exact text/layout matters
- the user's workflow already centers on GPT Image

## Prompt anatomy

artifact/purpose -> subject -> composition -> style -> lighting/materials -> literal text -> references -> constraints

## Edits

Use:
Change only [target]. Make it [desired result]. Keep [invariants] unchanged. Do not introduce [specific unwanted change].

After each edit, inspect the result before applying another modification.

## Text/layout

Quote exact copy. State placement, hierarchy, count, alignment, and reading order.

For diagrams/infographics, verify labels and relationships.

## Parameters

Keep model, quality, size, background and similar controls in the settings layer when the provider exposes them as parameters. Do not pretend prompt text changes an API parameter unless documented.

## Reference preservation

When a region must remain exact, prefer a workflow that explicitly preserves that region instead of relying on a vague keep-it-the-same instruction.

## Sources

- https://platform.openai.com/docs/guides/image-generation
- https://openai.com/index/introducing-chatgpt-images-2-5/
