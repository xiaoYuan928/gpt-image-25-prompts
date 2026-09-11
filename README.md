# hiAPI GPT Image 2.5 Prompt Collection

Sourced, attributed prompts for **GPT Image 2.5** (`gpt-image-2.5-flare` / `gpt-image-2.5-sunburst`), organized for copy-paste use and API experiments.

**159** entries · collected **2026-09-11** · every record has an `attribution.url`

> Soft note: try the same prompts on hiAPI — [GPT Image 2.5 Flare](https://www.hiapi.ai/en/models/gpt-image-2.5-flare?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-en-flare) · [Sunburst](https://www.hiapi.ai/en/models/gpt-image-2.5-sunburst?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-en-sunburst) · [API](https://api.hiapi.ai?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-en-api). Limited launch offer (check dates): [30% off promo](https://www.hiapi.ai/en/promotions?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-en-promo). This repo is **not affiliated with OpenAI**.

[简体中文](./README.zh-CN.md) · [NOTICE](./NOTICE.md) · [Schema](./schema/prompt.schema.json) · [Skill](./skills/hiapi-gpt-image-25/SKILL.md)

---

## Purpose

- Give developers and creators a **git-ready** seed library aligned with OpenAI’s Image 2.5 prompting guide.
- Keep **source links** so remixes stay attributable (CC BY 4.0 for prompt text).
- Highlight **Flare vs Sunburst** so you pick speed vs quality deliberately.

## Flare vs Sunburst

| Model | Role | When to use |
|---|---|---|
| `gpt-image-2.5-flare` | Fast / default path | Latency matters; quality already looks good on a dry run |
| `gpt-image-2.5-sunburst` | Higher quality / cost | Dense text, fine packaging, UI chrome, or quality still short |
| `either` | A/B the same prompt | Compare with identical `quality` / `size` / settings |

Practical rule (from OpenAI docs): if quality is already OK → try **Flare** to cut latency; if not → establish **Sunburst**, then A/B Flare with the same prompt and settings.

See [examples/flare-vs-sunburst.md](./examples/flare-vs-sunburst.md).

## Quick start

```bash
# browse machine-readable data
head -n 1 data/prompts.jsonl | jq .

# filter by category
jq -c 'select(.categories | index("xiaohongshu"))' data/prompts.jsonl

# list categories
jq '.categories[] | {id, count}' data/categories.json
```

Human-readable copies live under `prompts/<category>/`.

## Category index

| Category | Folder | Focus |
|---|---|---|
| Ecommerce | [prompts/ecommerce](./prompts/ecommerce/) | Hero shots, campaign ads |
| Xiaohongshu | [prompts/xiaohongshu](./prompts/xiaohongshu/) | 3:4 covers, Chinese text |
| Poster / typography | [prompts/poster-typography](./prompts/poster-typography/) | Exact on-image text |
| Product cutout | [prompts/product-cutout](./prompts/product-cutout/) | Transparent / isolated product |
| UI mockup | [prompts/ui-mockup](./prompts/ui-mockup/) | App / web chrome |
| Character consistency | [prompts/character-consistency](./prompts/character-consistency/) | Identity across scenes |
| Edit (Change + Preserve) | [prompts/edit-change-preserve](./prompts/edit-change-preserve/) | Surgical edits |
| Flare vs Sunburst | [prompts/flare-vs-sunburst](./prompts/flare-vs-sunburst/) | Comparison pairs |
| General | [prompts/general](./prompts/general/) | Photoreal / documentary |

## Prompt shape (official-aligned)

1. **Scene** — where / lighting / mood  
2. **Subject** — who or what  
3. **Details** — materials, text (quoted), composition  
4. **Use case** — ad, cover, mockup, packshot…  
5. **Constraints** — no extra text, no watermark, preserve identity…

Edits: **Change only X** + **Preserve** geometry / lighting / typography / layout.

More: [examples/openai-aligned.md](./examples/openai-aligned.md) · [skills/hiapi-gpt-image-25/SKILL.md](./skills/hiapi-gpt-image-25/SKILL.md)

## Record fields

Normalized into `data/prompts.jsonl`:

`id`, `title.{en,zh}`, `prompt`, `mode`, `categories`, `tags`, `recommended_model`, `settings`, `attribution.{source,author,url,license}`, `remix_allowed`, `collected_at`

## License

| Asset | License |
|---|---|
| Code, schema, docs scaffolding | [MIT](./LICENSE) |
| Prompt text | [CC BY 4.0](./LICENSE-PROMPTS) — credit upstream + this collection |
| Upstream authors | See [NOTICE.md](./NOTICE.md) |

## Disclaimer

Not affiliated with, endorsed by, or sponsored by OpenAI. Model names and docs examples are used for interoperability and education. Follow [OpenAI Usage Policies](https://openai.com/policies/usage-policies) when generating images.

---

*Maintained for hiAPI content experiments — restrained CTAs only; the prompts themselves stay free to copy.*
