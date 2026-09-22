---
name: visual-bible
description: Maintains recurring visual identity across scenes, images, and video shots.
---

# Visual Bible

Use when the same person, character, room, product, vehicle, brand asset, or visual world appears more than once.

## Lock fields

### Identity
- face/character identity
- body proportions
- age presentation
- distinctive features
- wardrobe

### Object/world
- product geometry
- architecture
- props
- environment
- palette
- materials
- typography rules

### Camera language
- lens tendency
- camera height
- framing
- depth of field
- movement style

### Lighting language
- key/fill direction
- softness
- contrast
- time of day
- atmosphere

## Continuity policy

Each new shot must explicitly reference what is locked and what is allowed to change.

Do not restate the entire bible unless needed. Inject only the relevant locked anchors.

## Drift detection

After each generation compare:
- identity
- wardrobe
- geometry
- scale
- environment
- camera
- light
- palette

When drift occurs, diagnose the changed dimension before rewriting the whole prompt.
