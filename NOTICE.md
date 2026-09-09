# NOTICE — Third-party prompt sources

Collected: **2026-09-09** (Asia/Shanghai).

This repository aggregates publicly published prompt examples for GPT Image 2.5
(Flare / Sunburst) education and API testing. Scaffolding is MIT; prompt text is
CC BY 4.0 with per-record attribution. **Not affiliated with OpenAI.**

## Unique sources

| URL | source | authors | prompts | license note |
|---|---|---|---:|---|
| https://developers.openai.com/api/docs/guides/image-prompting | openai-docs | OpenAI | 23 | OpenAI docs examples |
| https://fal.ai/learn/tools/prompting-gpt-image-2 | vendor-blog | Ilker Izgi / fal | 13 | fal blog examples; adapt for 2.5 |
| https://pixverse.ai/zh/blog/gpt-image-2-review-and-prompt-guide | vendor-blog | PixVerse | 10 | PixVerse blog copy-ready examples |
| https://help.apiyi.com/gpt-image-2-xiaohongshu-infographic-content-creation-guide.html | vendor-blog | APIYI 技术团队 | 6 | blog template; replace bracketed fields |
| https://github.com/EvoLinkAI/awesome-gpt-image-2-API-and-Prompts | github | @Gdgtify (via EvoLinkAI); @Strength04_X (via EvoLinkAI); @iamaiistudio (via EvoLinkAI) | 4 | CC0-1.0 (repo badge) |
| https://docs.jiling.cc/templates/xiaohongshu-saveable-cover.html | community | 机灵助手 / docs.jiling.cc | 1 | template page; reuse with attribution |
| https://github.com/Toolcentral-ai/awesome-gpt-image-2-prompts | github | かみいずみさω (via Toolcentral-ai) | 1 | source-attributed catalog |

## Mapping notes

- Collected fields `title_en` / `title_zh` → `title.en` / `title.zh`.
- Collected `attribution.source_type` → `attribution.source`.
- Collected `attribution.license_guess` → `attribution.license`.
- Every record sets `remix_allowed: true` and `collected_at: "2026-09-09"`.
- Prefer official OpenAI Image prompting examples as canonical for structure.
- fal / PixVerse / EvoLink / Toolcentral / Apiyi / jiling rows are largely GPT Image 2–era;
  structure is compatible with 2.5; see per-record `notes` where present.

## Disclaimer

Prompt strings remain the creative work of their listed authors. This pack does not
claim ownership of upstream examples. Always follow the upstream site terms and
OpenAI Usage Policy when generating images.
