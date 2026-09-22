---
name: generative-ai-prompting
description: "Cross-model visual prompt router for Gemini Omni 1.1 Flash, Nano Banana 2, Nano Banana Pro and GPT Image 2.5. Selects model, general, style and specialty skills, then produces a reviewed copy-ready prompt."
---
# Generative AI Prompting

## Route every request
1. Identify modality: image or video.
2. Identify operation: generate, edit, inpaint, composite, transform, extend or transition.
3. Resolve exact model/variant.
4. Apply the relevant model skill.
5. Add general skills only when triggered.
6. Add style skill(s) when style is a real requirement.
7. Add specialty skill(s) when domain constraints matter.
8. Review prompt for contradictions, missing invariants and filler.
9. Return final prompt + settings + reference roles.

## Model routing
- Video → Gemini Omni 1.1 Flash.
- General image + multi-reference → Nano Banana 2.
- Complex/professional/grounded/brand-sensitive image → Nano Banana Pro.
- GPT Image 2.5 draft/speed → Flare.
- GPT Image 2.5 precision/editing → Sunburst.

These are task-fit rules, not an overall quality ranking.

## Skill stacking
Do not load every skill. Retrieve the smallest useful set.

Common stacks:
- image generation → Prompt Architect + model skill
- reference recreation → Image-to-Prompt + model skill
- precise edit → Visual Editing + model skill
- poster/infographic → Typography & Layout + model skill
- real estate → Real Estate + model skill
- style-driven work → relevant Style skill + model skill
- library research → Prompt Curator + model skill

## Final review
Check subject, composition, spatial relationships, reference roles, text, preservation constraints, medium and visible style mechanisms. Remove generic adjective chains.
