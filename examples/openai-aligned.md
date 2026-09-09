# OpenAI-aligned prompt structure

Canonical references:

- [Image prompting (GPT Image 2.5)](https://developers.openai.com/api/docs/guides/image-prompting)
- [Cookbook: image generation prompting guide](https://developers.openai.com/cookbook/examples/multimodal/image-gen-models-prompting-guide)

## Generate skeleton

```text
Scene: …
Subject: …
Important details: … (quote exact text; materials; camera)
Use case: …
Constraints: no extra text; no watermark; …
```

## Edit skeleton

```text
Change only: …
Preserve: identity / geometry / lighting / typography / layout
Keep physical plausibility: shadows, scale, contact points
```

## Text on image

- Put the string in **quotes** or ALL CAPS.
- Specify size, weight, and placement once.
- Add “no extra / no duplicate text”.
- Spell difficult words explicitly.

## Parameters stay outside the prose

Put `model`, `quality`, `size`, `background` in the API / `settings` object — not as keyword stuffing inside the prompt.

## In this repo

Records under `attribution.source = "openai-docs"` are adapted from the official Image prompting guide. See `NOTICE.md` and each file in `prompts/`.
