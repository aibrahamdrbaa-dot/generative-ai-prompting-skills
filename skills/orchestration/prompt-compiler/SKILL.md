---
name: prompt-compiler
description: Compiles a model-agnostic visual brief into provider-aligned prompts without losing user intent or constraints.
---

# Prompt Compiler

The compiler is the translation layer between the shared visual brief and each model adapter.

## Compilation stages

1. Extract non-negotiables.
2. Assign reference authority.
3. Build scene, subject, and composition language.
4. Add provider-native controls from the selected model skill.
5. Remove contradictions and duplicated instructions.
6. Keep exact text verbatim.
7. Emit a standalone copy-ready prompt plus relevant settings.

## Non-negotiable invariant

Provider-native optimization may alter wording, ordering, and emphasis. It must not silently change:
- the subject
- the requested action
- the requested composition
- literal text
- identity anchors
- must-preserve properties
- explicit exclusions

## Prompt shape

Prefer:
context -> subject -> spatial relationships -> visual treatment -> lighting/materials -> text -> constraints -> references -> motion/audio for video

Do not force every field into every prompt.

## Output

Return:
- selected model
- reason code
- compiled prompt
- settings to apply outside the prompt when applicable
- attached reference roles
- QA checklist
