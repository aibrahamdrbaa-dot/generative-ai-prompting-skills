# Generative AI Prompting Skills

A practical, model-aware prompt-engineering toolkit for:

- Gemini Omni 1.1 Flash
- Nano Banana 2
- Nano Banana Pro
- ChatGPT Images 2.5

## Architecture

```
general-prompting/
├── router/
├── general/
│   ├── prompt-architect
│   ├── prompt-curator
│   ├── image-to-prompt
│   ├── visual-editing
│   └── typography-layout
├── models/
│   ├── gemini-omni-1-1-flash
│   ├── nano-banana-2
│   ├── nano-banana-pro
│   └── gpt-image-2-5
├── specialty/
│   └── real-estate-visuals
└── examples/
```

The router decides which specialized skill(s) should be applied. The model skills contain model-specific behavior. General skills handle cross-model reasoning.

## Current model IDs

| Product | API/model ID |
|---|---|
| Gemini Omni 1.1 Flash | `gemini-omni-1.1-flash` |
| Nano Banana 2 | `gemini-3.1-flash-image` |
| Nano Banana Pro | `gemini-3-pro-image` |
| ChatGPT Images 2.5 Flare | `gpt-image-2.5-flare` |
| ChatGPT Images 2.5 Sunburst | `gpt-image-2.5-sunburst` |

## Design principle

One universal prompt style is a bad abstraction. The shared layer handles visual reasoning, while each model skill adapts the prompt to its own strengths, interfaces, and workflows.

## Curation policy

Third-party prompt collections are research sources, not content to copy wholesale. The package records provenance and synthesizes original ready-to-use prompts.

## Examples

See `examples/` for copy-ready original prompts across real estate, product visuals, editing, posters, portraits, architecture and video.

## License

MIT
