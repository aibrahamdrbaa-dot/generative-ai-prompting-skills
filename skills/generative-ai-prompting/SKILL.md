---
name: generative-ai-prompting
description: "Router skill for visual generative-AI prompts. Detects task type, selects the appropriate general/model/specialty skills, retrieves only relevant guidance, and returns a copy-ready prompt."
---
# Generative AI Prompting Router
## Route
1. Classify image vs video.
2. Classify generate/edit/inpaint/composite/transform/extend.
3. Detect references and assign their roles.
4. Detect exact text and layout requirements.
5. Detect preservation constraints.
6. Pick the model-specific skill.
7. Add relevant general/specialty skills.
8. Run contradiction, omission and prompt-bloat checks.
9. Return a copy-ready prompt plus settings.
## Routing
Video → gemini-omni-1-1-flash.
Image general/multi-reference → nano-banana-2.
Image complex/professional/localized/brand-sensitive → nano-banana-pro.
GPT Image 2.5 fast → gpt-image-2-5 / Flare.
GPT Image 2.5 precision edit → gpt-image-2-5 / Sunburst.
Add real-estate-visuals for property work.
Add image-to-prompt when a reference image must be reverse-engineered.
Add visual-editing for controlled changes.
Add typography-layout when literal text or layout is central.
Add prompt-curator when the user asks for examples/library research.
## Output
Model/variant; recommended settings; final prompt; reference roles; one-line routing rationale.
