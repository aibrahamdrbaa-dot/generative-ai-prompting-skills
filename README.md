# Generative AI Prompting Skills

A production-oriented, **provider-aligned** skill system for prompting and curating generative visual work across:

- Gemini Omni 1.1 Flash
- Nano Banana 2
- Nano Banana Pro
- ChatGPT Images 2.5

> **Status:** These repository skills are original skills maintained for this project. They are not official Google/OpenAI Skills. Model behavior is anchored to the providers' current public documentation, with third-party repositories used as research references.

## Architecture

```
skills/
├── generative-ai-prompting/     # cross-model router
├── general/                     # reusable reasoning & editing skills
├── models/                      # one dedicated skill per supported model
├── styles/                      # reusable visual-style skills
└── specialty/                   # domain skills, starting with real estate
examples/                        # original copy-ready prompts
research/                        # sources, audit and curation notes
```

## Dedicated model skills

| Model | ID | Skill |
|---|---|---|
| Gemini Omni 1.1 Flash | `gemini-omni-1.1-flash` | `skills/models/gemini-omni-1-1-flash/SKILL.md` |
| Nano Banana 2 | `gemini-3.1-flash-image` | `skills/models/nano-banana-2/SKILL.md` |
| Nano Banana Pro | `gemini-3-pro-image` | `skills/models/nano-banana-pro/SKILL.md` |
| GPT Image 2.5 Flare | `gpt-image-2.5-flare` | `skills/models/gpt-image-2-5/SKILL.md` |
| GPT Image 2.5 Sunburst | `gpt-image-2.5-sunburst` | same GPT Image 2.5 skill |

## General skills

- prompt-architect
- prompt-curator
- image-to-prompt
- visual-editing
- typography-layout

## Style skills

- photorealism
- cinematic
- editorial
- product-photography
- architectural-visualization
- illustration
- anime
- minimalist-graphic

Style skills are **modular adapters**, not rigid presets. They tell the prompt writer which visual decisions define a style and which generic adjectives to avoid.

## Specialty skills

- real-estate-visuals

## Recommended stacking

```
User brief
   ↓
General Prompt Architect
   ↓
Model Skill
   + Style Skill(s)
   + Specialty Skill(s)
   + Editing / Typography / Image-to-Prompt when relevant
   ↓
Prompt review
   ↓
Copy-ready prompt + settings
```

Examples:
- Real-estate interior image → Prompt Architect + Nano Banana 2 + Real Estate + Architectural Visualization
- Luxury product campaign → Prompt Architect + Nano Banana Pro + Product Photography + Editorial
- Real-estate walkthrough video → Prompt Architect + Omni 1.1 Flash + Real Estate + Cinematic
- Poster → Prompt Architect + target model + Typography & Layout + Minimalist Graphic

## Curation policy

Third-party prompt libraries are treated as research material. We retain source links, model fit, evidence and provenance notes; we do not copy large prompt dumps into this repository.

## License

MIT
