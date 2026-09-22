# Generative AI Prompting Skills

A production-oriented, provider-aligned skill system for visual generation and editing across:

- Gemini Omni 1.1 Flash
- Nano Banana 2
- Nano Banana Pro
- GPT Image 2.5

The repository also contains dormant optional skill families that are not part of normal execution.

## Architecture

User Brief
-> Visual Brief
-> Model Router
-> Skill Stack Planner
-> Reference Manager / Visual Bible / Specialty / Style
-> Prompt Compiler
-> Model Adapter
-> Generation
-> Quality Gate
-> Iteration Controller
-> Supermemory

Optional subsystems are activated only by their own trigger rules.

## Personality subsystem

A separate on-demand personality and behavioral-analysis family exists under:
skills/personality/

Structure:
- framework-selector
- assessment-adapter
- evidence
- frameworks/mbti
- frameworks/disc
- frameworks/big-five
- frameworks/enneagram
- frameworks/attachment

The global protection layer is:
skills/orchestration/personality-gate/

Personality skills must never be loaded merely because Roy notices a behavioral pattern in conversation.

## Personality activation

DORMANT BY DEFAULT.

Activate only for:
- explicit personality testing
- explicit personality analysis
- interpretation of a supplied personality assessment
- explicit communication/workflow adaptation based on a known result

Do not infer or persist personality types from casual conversation.

## Memory rule

Supermemory stores durable workflow knowledge and explicitly confirmed preferences. It does not replace live source-of-truth documentation.

## Quality rule

Tool success is not output success. Every meaningful generation or analysis gets a compliance/reasoning check before it becomes a reusable lesson.

## Current visual routing

- Omni 1.1 Flash -> video-native work
- Nano Banana 2 -> general image work
- Nano Banana Pro -> complex/grounded/brand-sensitive image work
- GPT Image 2.5 Flare -> latency-oriented image work
- GPT Image 2.5 Sunburst -> quality/detail-oriented image work

See SKILLS_INDEX.md.
