# Missing previews

Prompts where the attribution source page did **not** provide a clearly corresponding example/output image
(or download failed). `preview` remains `null` in `data/prompts.jsonl`.

Count: **18** / 58

- `gi25-ui-002` — DAYBREAK minimalist to-do app screenshot: fal page shows DAYBREAK prompt text but adjacent example image is a different mobile weather-app render, not DAYBREAK.
- `gi25-gen-007` — Istanbul florist blue hour structured template: fal copy-paste Istanbul florist prompt; page only shows a “closest analogue” winter street portrait, not this prompt’s output.
- `gi25-flare-001` — Museum woman editorial structured: fal “vague vs visual” museum woman structured prompt has no dedicated example output image (museum photo is a try-on input).
- `gi25-edit-015` — Change-only clothing olive jacket preserve face: fal olive-jacket “change only clothing” text example has no dedicated result image (try-on visuals belong to multi-ref case).
- `gi25-eco-004` — Matte black speaker ecommerce hero: PixVerse lists the matte-black speaker ecommerce hero as copy-ready text; no dedicated output image (product-ad image is the tagged “SOUND YOU CAN FEEL” ad = eco-006).
- `gi25-typ-006` — Create Faster vertical launch poster: PixVerse “Create Faster” poster prompt has no matching example image (nearby city poster is Spring 2026 New York, different prompt).
- `gi25-char-003` — NOVA sci-fi courier character sheet: PixVerse NOVA courier sheet prompt; section image is the Lysandra fantasy mage sheet (prompt 41), not NOVA.
- `gi25-eco-005` — White earbuds pure ecommerce cutout: PixVerse white earbuds ecommerce prompt has no example output on the page.
- `gi25-ui-005` — LUMA habit app onboarding: PixVerse LUMA onboarding prompt; section image is Leonardo Instagram UI mockup (different prompt).
- `gi25-edit-013` — Multi-ref product into style scene: PixVerse multi-ref product-into-scene edit prompt; section image is astronaut first-frame (prompt 71), not this edit.
- `gi25-edit-014` — Change weather only light snowfall: PixVerse weather/snowfall edit prompt has no example output image on the page.
- `gi25-typ-008` — FRAME 2026 design conference poster: PixVerse FRAME 2026 poster prompt; nearby poster image is Spring 2026 New York, not FRAME 2026.
- `gi25-xhs-001` — Xiaohongshu knowledge card template: Apiyi article images are guide/process/comparison graphics, not outputs of the knowledge-card template.
- `gi25-xhs-002` — Xiaohongshu product comparison card: Apiyi page has no example output for the product-comparison card template.
- `gi25-xhs-003` — Xiaohongshu tutorial 3-step card: Apiyi page has no example output for the 3-step tutorial card template.
- `gi25-xhs-004` — Xiaohongshu data visualization card: Apiyi page has no example output for the data visualization card template.
- `gi25-xhs-005` — Xiaohongshu checklist cover: Apiyi page has no example output for the checklist cover template.
- `gi25-xhs-006` — Xiaohongshu AI drawing tools cover example: Apiyi page has no example output for the AI drawing tools TOP 5 cover (only guide chrome images).
