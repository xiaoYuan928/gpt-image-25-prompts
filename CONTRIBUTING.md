# Contributing

Thanks for helping grow a sourced GPT Image 2.5 prompt library.

## Rules

1. **Do not invent prompts.** Every entry needs a public `attribution.url`.
2. Match `schema/prompt.schema.json`.
3. Prefer OpenAI's structure: Scene → Subject → Details → Use case → Constraints.
4. For edits, use Change + Preserve language.
5. Set `recommended_model` to `gpt-image-2.5-flare`, `gpt-image-2.5-sunburst`, or `either`.
6. Keep EN + ZH titles when possible.
7. One logical change per PR.

## Add a prompt

1. Append one JSON object line to `data/prompts.jsonl`.
2. Add or update the matching file under `prompts/<category>/<id>.md`.
3. Update `data/categories.json` counts if you introduce a new category.
4. If the URL is new, add a row to `NOTICE.md`.

## ID convention

`gi25-<short>-NNN` — e.g. `gi25-eco-010`, `gi25-xhs-008`.

## License

- Repo scaffolding: MIT (`LICENSE`)
- Prompt text you contribute: CC BY 4.0 (`LICENSE-PROMPTS`) with attribution retained
