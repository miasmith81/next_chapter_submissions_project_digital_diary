# AI Placeholder-Image Generation Brief

## Purpose

Generate 12 cohesive, non-personal illustrations for the diary's automatic image rotation. The art should support serenity, peace, love, compassion, understanding, hope, comfort, reflection, healing, connection, and resilience.

## Assignment

**AI tools:** Gemini for the completed first and second iterations; OpenAI image generation may be used for a future final collection

**Confirmed model:** Gemini 1.5 Flash, as identified in the second supplied report

**Status:** Second Gemini collection received; filenames corrected by Codex; exact sizing, visible disclosure, final-file provenance verification, and integration pending

**Human decision-maker:** Mia

AI tools propose visual assets. Mia directs the creative requirements, reviews, accepts, rejects, revises, and approves files. ChatGPT/Codex independently verifies outputs and handles deterministic project organization.

## Required Output

- 12 separate PNG images
- Exact 1024 x 1280 dimensions
- Portrait 4:5 composition
- Consistent style, palette, and dimensions
- Full-bleed art without a built-in frame
- Names `frame01.png` through `frame12.png`
- Final location `assets/frames/`
- Visible lower-right disclosure: `AI-generated artwork — Directed by Mia`
- Preserve C2PA and SynthID provenance signals when present and verify the final post-processed export

## Required Themes

1. Serenity - still lake at dawn
2. Peace - quiet forest path
3. Love - ribbons of light forming a heart
4. Compassion - symbolic hands holding warm light
5. Understanding - illuminated bridge
6. Calm - moonlight over slow waves
7. Reflection - lotus and ripples
8. Safety - protective tree canopy
9. Hope - birds moving toward light
10. Comfort - warm cup, window, and folded blanket
11. Healing - warm light through clouds after rain
12. Connection - varied wildflowers growing together

## Content Boundaries

- No readable text except the required AI-generation disclosure; no personal photos, identifiable faces, medical symbols, medication, diagnoses, medical claims, crisis scenes, violence, harmful stereotypes, or copyrighted characters.
- No built-in polaroid border; CSS supplies the frame.
- Gemini's lower-right platform mark is accepted as generator attribution, but it does not replace the project's required visible disclosure.
- Do not copy or imitate Gemini's star or use an OpenAI logo as the project disclosure badge.
- A visible disclosure is transparency, not technical proof. Do not claim C2PA or SynthID survives cropping, resizing, format conversion, or other edits unless the final file is checked.

## Verification Checklist

- [x] Exact Gemini model documented in the supplied second report.
- [x] Exactly 12 separate images.
- [x] No collage or contact sheet.
- [x] PNG format.
- [x] Portrait orientation.
- [ ] Exact 1024 x 1280 dimensions and 4:5 ratio.
- [x] Consistent dimensions within the supplied second collection.
- [x] Sequential names after Codex created renamed copies.
- [x] Cohesive palette and style.
- [x] No unrelated readable text, logos, personal content, or unsafe imagery in the supplied Gemini collection.
- [x] Gemini platform watermark documented and accepted by Mia.
- [x] No built-in polaroid border.
- [ ] Required `AI-generated artwork — Directed by Mia` disclosure added consistently to all final files.
- [ ] Original generated exports preserved separately from final post-processed files.
- [ ] Final files checked for C2PA and SynthID provenance signals.
- [ ] Provenance result recorded honestly for each final file without treating a missing signal as proof that the image was not AI-generated.
- [ ] Crop test inside the actual CSS frame.
- [ ] Web optimization test.
- [x] Accepted, revised, and rejected results documented.
- [ ] Final integration approval after size, disclosure, provenance, and display verification.

## OpenAI Provenance References

- [C2PA and SynthID in OpenAI-generated images](https://help.openai.com/en/articles/8912793-c2pa-in-images) — explains the provenance signals included with supported OpenAI-generated images and their limitations.
- [Verify OpenAI-generated images](https://openai.com/research/verify/) — checks a final PNG, JPG, or WEBP for supported OpenAI provenance signals.

## Iteration History

### First Collection

Gemini returned 12 distinct 1376 x 768 landscape PNG files with an abstract gradient direction, concept filenames, altered scenes, and a non-purple-led palette. Independent audit rejected it for repository integration.

### Second Collection

Gemini 1.5 Flash returned 12 improved portrait PNG files matching the requested concepts and painterly palette. Actual metadata showed 928 x 1152, despite the report claiming 1024 x 1280. Gemini also supplied generated filenames. Codex created byte-identical sequential copies and verified the ZIP.

Mia superseded the original no-watermark requirement and accepted the visible platform mark as AI disclosure. On July 23, 2026, she added a generator-independent rule: every final AI-created image must visibly state `AI-generated artwork — Directed by Mia`. Exact sizing, visible-disclosure application, final-file provenance verification, and integration remain unresolved.

See `docs/archive/PLACEHOLDER_IMAGE_AUDIT.md`, `docs/archive/SECOND_COLLECTION_AUDIT.md`, and `docs/archive/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.
