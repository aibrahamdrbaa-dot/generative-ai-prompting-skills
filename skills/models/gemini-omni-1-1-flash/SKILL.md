---
name: gemini-omni-1-1-flash
description: Provider-aligned adapter for Gemini Omni 1.1 Flash video generation and editing.
---

# Gemini Omni 1.1 Flash

Official model ID: gemini-omni-1.1-flash.

## Route here when

- text-to-video
- image-to-video
- reference-guided video
- conversational video editing
- video extension
- first-frame / last-frame transitions

## Prompt anatomy

shot framing -> camera movement -> subject/action -> location/environment -> visual style -> lighting/mood -> timing -> audio -> continuity constraints

## Motion

Prefer one clear camera behavior and one clear subject-motion pattern per short shot.

Name:
- shot size
- camera movement
- subject movement
- environmental motion
- timing when timing is important

## Frames and references

When using first/last-frame or reference-guided workflows:
- label each reference role
- describe what must remain consistent
- define the transition rather than merely describing endpoints

## Conversational editing

For iterative editing, state the intended change and preserve successful properties from the previous state.

Use Visual Bible when identity or scene continuity matters.

## Audio

Separate:
- dialogue
- ambience
- music
- SFX

Do not add audio instructions unless audio is part of the requested deliverable.

## Regional restriction check

Current Google Gemini skills documentation warns that uploading videos for editing or extension is unavailable in the EEA, Switzerland, the United Kingdom, and some US states. Because availability can change, verify the current official provider surface before relying on upload-based video editing or extension.

## Runtime limits

Provider limits on output duration, resolution, input count, aspect ratio and other controls are execution-time facts. Query current provider documentation instead of hard-coding stale limits into prompts.

## Sources

- https://ai.google.dev/gemini-api/docs/models
- https://ai.google.dev/gemini-api/docs/omni
- https://deepmind.google/models/gemini-omni/prompting-guide/
