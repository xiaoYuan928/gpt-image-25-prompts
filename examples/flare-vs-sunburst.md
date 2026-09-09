# Flare vs Sunburst

OpenAI’s GPT Image 2.5 exposes two generation paths:

| | **Flare** | **Sunburst** |
|---|---|---|
| ID | `gpt-image-2.5-flare` | `gpt-image-2.5-sunburst` |
| Bias | Lower latency | Higher fidelity |
| Good for | Iteration, drafts, social volume | Exact text, packaging, UI, hero finals |

## How to compare fairly

1. Lock the **same prompt** string.
2. Lock **quality**, **size**, and other settings.
3. Run Flare and Sunburst back-to-back.
4. Prefer Flare when the Sunburst result is not meaningfully better.

## Seed prompts tagged for comparison

Browse `prompts/flare-vs-sunburst/` or filter:

```bash
jq -c 'select(.categories | index("flare-vs-sunburst"))' data/prompts.jsonl
```

Official-style photoreal and infographic pairs in this collection often mark `recommended_model` as `either` or call out both models in `notes`.

## hiAPI note

If you route through an OpenAI-compatible gateway such as [hiAPI](https://hiapi.ai), pass the model id explicitly (`gpt-image-2.5-flare` or `gpt-image-2.5-sunburst`) rather than burying the choice inside the natural-language prompt.
