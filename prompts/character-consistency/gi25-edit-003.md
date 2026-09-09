# Virtual try-on preserve identity

**中文标题：** 虚拟试穿：仅换衣保留身份  
**ID:** `gi25-edit-003` · **Mode:** `multi_ref`  
**Categories:** `edit-change-preserve`, `character-consistency`  
**Tags:** `try-on`, `identity-lock`, `openai-official`  

### Virtual try-on preserve identity

```text
Edit the image to dress the woman using the provided clothing images. Do not change her face, facial features, skin tone, body shape, pose, or identity in any way. Preserve her exact likeness, expression, hairstyle, and proportions. Replace only the clothing, fitting the garments naturally to her existing pose and body geometry with realistic fabric behavior. Match lighting, shadows, and color temperature to the original photo so the outfit integrates photorealistically, without looking pasted on. Do not change the background, camera angle, framing, or image quality, and do not add accessories, text, logos, or watermarks.
```

- **Recommended model:** `gpt-image-2.5-sunburst`
- **Settings:** `quality=medium`, `size=1024x1536`
- **Source:** [OpenAI Image prompting](https://developers.openai.com/api/docs/guides/image-prompting) — OpenAI
- **License note:** OpenAI docs examples
- **Notes:** Multi-image edit; Sunburst preferred for identity-sensitive try-on.
