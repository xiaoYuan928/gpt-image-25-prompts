# Preview images (cached upstream examples)

These files are **local caches** of example / preview images published on the prompt attribution sources
(OpenAI Image prompting docs, fal prompting guide, PixVerse blog, EvoLink GitHub, Image Prompt Gallery /
Toolcentral, docs.jiling.cc, etc.).

## Rules

- Images were **downloaded from the original pages**, not generated with APIs for this pack.
- Each prompt’s `preview.source_image_url` in `data/prompts.jsonl` points at the upstream bytes we cached.
- Full URL inventory: [`SOURCES.md`](./SOURCES.md).
- Prompts without a clear upstream example: [`MISSING.md`](./MISSING.md).

## License / NOTICE

Scaffolding of this repository is MIT; prompt text is CC BY 4.0 with per-record attribution (see root
`LICENSE`, `LICENSE-PROMPTS`, `NOTICE.md`). **Cached preview pixels remain subject to the upstream site’s
terms and copyright.** Prefer linking to the attribution URL for redistribution questions; local copies
are for education, review, and offline browsing of this catalog.

If you redistribute this pack commercially, re-check each upstream license and remove or replace
previews as needed.
