# Generative AI Prompting Skills

A production-oriented, provider-aligned skill system for visual generation and editing across:

- Gemini Omni 1.1 Flash
- Nano Banana 2
- Nano Banana Pro
- GPT Image 2.5

These are original project skills, not official Google or OpenAI skill packages. Provider documentation is the source of truth for current model behavior.

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

## Repository layout

skills/
├── generative-ai-prompting/   entry router
├── orchestration/             brief, routing, stacking, compilation, continuity, video planning
├── general/                   reusable task skills
├── models/                    one adapter per supported model
├── styles/                    reusable visual-language adapters
└── specialty/                 domain-specific correctness
examples/                      regression and copy-ready examples
research/                      audits, matrices, sources, architecture

## Design rule

The same user intent may need different prompt construction for different models. The system therefore keeps a common visual brief and compiles it through a provider-specific adapter.

## Memory rule

Supermemory stores durable workflow knowledge and user-confirmed preferences. It does not replace live provider documentation or project source-of-truth files.

## Quality rule

Tool success is not output success. Every meaningful generation gets a compliance and quality check before it becomes a reusable lesson.

## Current routing

- Omni 1.1 Flash -> video-native work
- Nano Banana 2 -> general image work
- Nano Banana Pro -> complex/grounded/brand-sensitive image work
- GPT Image 2.5 Flare -> latency-oriented image work
- GPT Image 2.5 Sunburst -> quality/detail-oriented image work

See SKILLS_INDEX.md and research/MODEL-CAPABILITY-MATRIX.md.
