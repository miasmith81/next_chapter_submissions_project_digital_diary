# Gemini Placeholder-Image Generation Brief

## Purpose

Generate 12 cohesive, non-personal illustrations for the diary's automatic image rotation. The art should support serenity, peace, love, compassion, understanding, hope, comfort, reflection, healing, connection, and resilience.

## Assignment

**AI tool:** Gemini  
**Model:** Gemini 1.5 Flash, as identified in the second supplied report  
**Status:** Second collection received; filenames corrected by Codex; exact sizing pending  
**Human decision-maker:** Mia

Gemini proposes visual assets. Mia reviews, accepts, rejects, revises, and approves files. ChatGPT/Codex independently verifies outputs and handles deterministic project organization.

## Required Output

- 12 separate PNG images
- Exact 1024 x 1280 dimensions
- Portrait 4:5 composition
- Consistent style, palette, and dimensions
- Full-bleed art without a built-in frame
- Names `frame01.png` through `frame12.png`
- Final location `assets/frames/`

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

- No readable text, personal photos, identifiable faces, medical symbols, medication, diagnoses, medical claims, crisis scenes, violence, harmful stereotypes, or copyrighted characters.
- No built-in polaroid border; CSS supplies the frame.
- Gemini's lower-right platform mark is accepted and must be disclosed as AI-generation attribution.

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
- [x] No readable text, unrelated logos, personal content, or unsafe imagery.
- [x] Gemini platform watermark documented and accepted by Mia.
- [x] No built-in polaroid border.
- [ ] Crop test inside the actual CSS frame.
- [ ] Web optimization test.
- [x] Accepted, revised, and rejected results documented.
- [ ] Final integration approval after size verification.

## Iteration History

### First Collection

Gemini returned 12 distinct 1376 x 768 landscape PNG files with an abstract gradient direction, concept filenames, altered scenes, and a non-purple-led palette. Independent audit rejected it for repository integration.

### Second Collection

Gemini 1.5 Flash returned 12 improved portrait PNG files matching the requested concepts and painterly palette. Actual metadata showed 928 x 1152, despite the report claiming 1024 x 1280. Gemini also supplied generated filenames. Codex created byte-identical sequential copies and verified the ZIP.

Mia superseded the original no-watermark requirement and accepted the visible platform mark as AI disclosure. Exact sizing is the only unresolved asset requirement.

See `docs/archive/PLACEHOLDER_IMAGE_AUDIT.md`, `docs/archive/SECOND_COLLECTION_AUDIT.md`, and `docs/archive/prompts/GEMINI_EXACT_SIZE_PROMPT.md`.
