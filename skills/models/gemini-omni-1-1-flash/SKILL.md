---
name: gemini-omni-1-1-flash
description: "Dedicated provider-aligned prompt skill for Gemini Omni Flash (gemini-omni-1.1-flash): text-to-video, image-to-video, reference-to-video, conversational editing, extension and frame interpolation."
---
# Gemini Omni 1.1 Flash

## Provider identity
Official model ID: `gemini-omni-1.1-flash`.

## Use it for
- text-to-video;
- image-to-video;
- reference-guided video;
- conversational editing;
- extensions;
- first/last-frame interpolation.

## Prompt anatomy
Shot framing + camera motion → action → location → style/visual feel → lighting → timing/audio/text → continuity constraints.

## Provider-aligned principles
Google recommends emphasizing scene description, camera movement, lighting and mood. The official prompt guide also identifies shot framing/motion, style, lighting, location and action as core prompt elements. `task` can be used to disambiguate the intended video operation, but Google recommends relying primarily on prompting where possible.

## Conversational editing
When continuing a prior interaction, describe only the intended change and preserve what matters. State continuity constraints when details must remain fixed.

## References
When images/videos are supplied, define what each reference controls: subject, object, pose, environment, motion or style. Do not invent information absent from the references.

## Camera vocabulary
Use real camera intent: wide, medium, close-up, locked-off, push-in, dolly, handheld, over-the-shoulder, continuous shot.

## Timing/audio
Use time ranges only when timing matters. Separate dialogue, sound design and music instructions.

## Source
https://ai.google.dev/gemini-api/docs/omni
https://deepmind.google/models/gemini-omni/prompt-guide/
