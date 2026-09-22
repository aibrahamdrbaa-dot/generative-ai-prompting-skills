# Roy Visual Generation Architecture — 2026-09-23

## Objective

Build one reusable system that helps Ibrahim create images and videos across four model families without treating them as interchangeable prompt boxes.

## Architecture

User brief
-> Visual Brief
-> Model Router
-> Skill Stack Planner
-> Reference Manager / Visual Bible / Specialty / Style
-> Prompt Compiler
-> Model Adapter
-> Generation
-> Quality Gate
-> Iteration Controller
-> Supermemory lesson

## Why this architecture

The repository already had model-specific skills, general prompting skills, styles, real-estate specialization, examples, and research. The audit found that orchestration between these layers was the missing structural component.

## Three persistent assets

### 1. Common Visual Brief
The provider-neutral representation of user intent.

### 2. Visual Bible
The continuity representation for recurring identities, objects, environments, camera, and light.

### 3. Model Adapter
The provider-specific translation layer.

These assets let the system improve without copying prompts between models.

## Supermemory policy

Supermemory stores durable workflow knowledge, not source-of-truth provider documentation.

Store:
- successful routing patterns
- repeated failure modes
- useful skill combinations
- user-confirmed durable visual preferences
- model-specific prompt lessons
- versioned corrections

Containers:
- agent:roy for system-wide routing and skill lessons
- user:ibrahim only for durable user-specific preferences
- project containers for project-local visual bibles or brand rules

Never mix containers casually.

## Learning promotion rule

A lesson becomes durable when:
- it is explicitly confirmed, or
- it recurs and survives verification, or
- it materially improves the same task class more than once.

One accidental success is not enough.

## Research policy

Official provider documentation outranks community prompt libraries for model behavior. Community skills are used to discover reusable techniques and are synthesized rather than copied wholesale.

## Failure containment

Every write to GitHub is followed by read-back of critical files.
Every meaningful model lesson is independently verified before promotion to durable memory.
