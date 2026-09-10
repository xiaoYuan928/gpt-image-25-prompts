# hiAPI GPT Image 2.5 提示词合集

面向 **GPT Image 2.5**（`gpt-image-2.5-flare` / `gpt-image-2.5-sunburst`）的**有出处**提示词库，适合复制使用与 API 试验。

**131** 条 · 采集于 **2026-09-10** · 每条均含 `attribution.url`

> 轻量说明：同一批 Prompt 可在 hiAPI 试跑 — [Flare](https://www.hiapi.ai/zh/models/gpt-image-2.5-flare?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-zh-flare) · [Sunburst](https://www.hiapi.ai/zh/models/gpt-image-2.5-sunburst?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-zh-sunburst) · [API](https://api.hiapi.ai?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-zh-api)。上新限时活动（以页面日期为准）：[双模型限时 7 折](https://www.hiapi.ai/zh/promotions?utm_source=github&utm_medium=referral&utm_campaign=gpt-image-25-prompts&utm_content=readme-zh-promo)。本仓库**与 OpenAI 无隶属关系**。

[English](./README.md) · [NOTICE](./NOTICE.md) · [Schema](./schema/prompt.schema.json) · [Skill](./skills/hiapi-gpt-image-25/SKILL.md)

---

## 目的

- 提供与 OpenAI Image 2.5 提示规范对齐的 **git 就绪**种子库。
- 保留 **来源链接**，方便按 CC BY 4.0 署名 remix。
- 讲清 **Flare vs Sunburst**，按延迟与质量选型。

## Flare vs Sunburst

| 模型 | 角色 | 何时选用 |
|---|---|---|
| `gpt-image-2.5-flare` | 快 / 默认路径 | 在意延迟；试跑质量已够 |
| `gpt-image-2.5-sunburst` | 更高质量 / 成本 | 密字、包装细节、UI 控件，或质量仍不够 |
| `either` | 同 Prompt 对照 | 固定 `quality` / `size` / 参数做 A/B |

实务（对齐官方文档）：质量已够 → 测 **Flare** 降延迟；不够 → 先用 **Sunburst** 定调，再用相同 Prompt/参数回测 Flare。

详见 [examples/flare-vs-sunburst.md](./examples/flare-vs-sunburst.md)。

## 快速开始

```bash
head -n 1 data/prompts.jsonl | jq .

jq -c 'select(.categories | index("xiaohongshu"))' data/prompts.jsonl

jq '.categories[] | {id, count}' data/categories.json
```

可读版在 `prompts/<category>/`。

## 分类索引

| 分类 | 目录 | 侧重 |
|---|---|---|
| 电商 | [prompts/ecommerce](./prompts/ecommerce/) | 主图、营销广告 |
| 小红书 | [prompts/xiaohongshu](./prompts/xiaohongshu/) | 3:4 封面、中文出字 |
| 海报文字 | [prompts/poster-typography](./prompts/poster-typography/) | 精确屏幕文字 |
| 产品抠图 | [prompts/product-cutout](./prompts/product-cutout/) | 透明底 / 孤立产品 |
| UI 稿 | [prompts/ui-mockup](./prompts/ui-mockup/) | App / Web 界面 |
| 角色一致 | [prompts/character-consistency](./prompts/character-consistency/) | 跨场景身份 |
| 编辑 | [prompts/edit-change-preserve](./prompts/edit-change-preserve/) | Change + Preserve |
| Flare 对照 | [prompts/flare-vs-sunburst](./prompts/flare-vs-sunburst/) | 双模型对比 |
| 通用 | [prompts/general](./prompts/general/) | 写实 / 纪实 |

## 官方对齐写法

1. **Scene（场景）**  
2. **Subject（主体）**  
3. **Details（细节）** — 材质、引号内精确文字、构图  
4. **Use case（用途）**  
5. **Constraints（约束）**

编辑：**只改 X** + **保持**几何 / 光影 / 文字 / 版式。

更多：[examples/openai-aligned.md](./examples/openai-aligned.md) · [SKILL.md](./skills/hiapi-gpt-image-25/SKILL.md)

## 字段

`data/prompts.jsonl` 已规范化为：

`id`、`title.{en,zh}`、`prompt`、`mode`、`categories`、`tags`、`recommended_model`、`settings`、`attribution.{source,author,url,license}`、`remix_allowed`、`collected_at`

## 许可

| 资产 | 许可 |
|---|---|
| 代码、Schema、文档脚手架 | [MIT](./LICENSE) |
| 提示词文本 | [CC BY 4.0](./LICENSE-PROMPTS) — 请同时署名上游与本合集 |
| 上游作者 | 见 [NOTICE.md](./NOTICE.md) |

## 声明

本项目与 OpenAI **无官方隶属或背书关系**。模型名与文档示例仅用于互操作与教学。出图时请遵守 [OpenAI 使用政策](https://openai.com/policies/usage-policies)。

---

*服务 hiAPI 内容实验 — 仅克制 CTA；提示词本身可自由复制。*
