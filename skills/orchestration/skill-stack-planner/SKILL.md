---
name: skill-stack-planner
description: Selects and orders the minimum set of reusable visual skills needed for a generation or editing task.
---

# Skill Stack Planner

Treat Skills as a graph, not a checklist.

## Base graph

Visual Brief -> Model Router -> Prompt Compiler -> Model Adapter -> QA

## Optional branches

- references -> Reference Manager
- repeated identity -> Visual Bible
- video -> Video Storyboard
- typography -> Typography & Layout
- edit -> Visual Editing
- reverse engineering -> Image-to-Prompt
- domain -> Specialty
- aesthetics -> Style
- failed output -> Iteration Controller

## Ordering rules

1. Architecture before style.
2. Reference authority before prompt wording.
3. Domain constraints before decorative style.
4. Model adapter after common intent is stable.
5. QA after generation.
6. Iteration Controller changes one major failure dimension at a time.

Avoid redundant skills that solve the same layer.
