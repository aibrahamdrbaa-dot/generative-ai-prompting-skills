---
name: video-storyboard
description: Plans multi-shot AI video as a sequence of controlled shots, frames, motion, timing, continuity, and audio instructions.
---

# Video Storyboard

Use for multi-shot video, ads, reels, cinematic sequences, or any task where shot continuity matters.

## Storyboard schema

shot_id | duration | framing | camera_move | subject_action | environment_motion | lighting | transition | audio | continuity_anchors

## Frame strategy

When useful, generate or define:
- establishing frame
- hero/identity frame
- detail frame
- transition endpoint

For first/last-frame workflows, treat the endpoints as continuity contracts.

## Motion rules

Describe:
- what starts still
- what moves first
- what moves continuously
- what stops
- what the camera does relative to the subject

Avoid piling multiple unrelated camera moves into a short shot.

## Audio rules

Separate:
- dialogue
- ambience
- music
- sound effects

Do not assume audio is wanted merely because the provider can generate it.

## QA

Check shot-to-shot:
- identity
- wardrobe
- geometry
- spatial direction
- light
- color
- camera logic
- motion continuity
- audio continuity
