# Prompt History

## Project

**Next Chapter Submissions Project — A Digital Diary**

## Purpose

This file highlights the prompts that best demonstrate how I plan, question, iterate, debug, and verify work with AI. It is a curated project record, not an unfiltered transcript.

Sensitive personal information, credentials, private diary entries, and authentication codes must never be included.

---

## Prompt 1 — Requirements and architecture review

**Stage:** Planning  
**AI tool:** ChatGPT/Codex  
**Model:** Record the exact model shown in the product interface  
**Mode:** Teaching Mode

### Prompt

Review the Next Chapter admissions requirements and my original digital diary handoff. Help me determine what can be preserved, what conflicts with the rubric, how I should document the build and prompt history, and which AI tools should be assigned to each type of task. Do not generate code yet.

### Why this was a strong prompt

- Supplied both the requirements and the previous-project context.
- Defined the desired outcome.
- Established a no-code boundary.
- Asked for architecture, documentation, and AI-tool decisions rather than code generation alone.

### Result and decision

The review identified a conflict between the original React/Express/Neon architecture and the static GitHub Pages requirement. I decided to rebuild the admissions version as a static functional prototype while preserving the diary design and animation.

### Verification

I compared the recommendation against the actual submission checklist and deployment requirement.

---

## Prompt 2 — Challenge the storage recommendation

**Stage:** Security and scope decision  
**AI tool:** ChatGPT/Codex  
**Mode:** Teaching Mode

### Prompt

If I use `localStorage` instead of a cloud database, can I create a username and password model that is enough to keep each user's saved mental-health diary data secure?

### Why this was an important follow-up

The prompt did not automatically accept the first architecture recommendation. It questioned a security assumption before implementation.

### Result and decision

I learned that a JavaScript-only login screen would not provide real authentication because JavaScript on the same website can access the browser storage. I decided not to build cosmetic security or claim that the prototype is production-secure.

### Verification

The answer was checked against authoritative browser-storage security guidance.

---

## Prompt 3 — Interview rubber-ducking

**Stage:** Interview preparation  
**AI tool:** ChatGPT/Codex  
**Mode:** Teaching Mode

### Prompt

Rubber-duck the possible admissions interview questions with me one question at a time. Help me separate the problem, value, and solution, preserve my voice, identify anything missing, and wait for me to explain each idea in my own words before refining the answer.

### Why this was a strong prompt

- Defined a step-by-step learning process.
- Protected my ownership of the answers.
- Asked AI to identify gaps rather than replace my thinking.
- Produced explanations I can genuinely defend in an interview.

### Result

Questions about the problem, user value, solution choice, build order, AI collaboration, and challenging an AI recommendation were developed and refined. Bug and verification answers were intentionally postponed until evidence exists from the build.

---

## Prompt 4 — Generate 12 diary placeholder images

**Stage:** Visual asset planning  
**AI tool:** Gemini  
**Model:** Not identified in the supplied report; record the exact model displayed in Gemini  
**Mode:** Image generation  
**Status:** First iteration returned and independently audited; revision required

### Goal

Generate a cohesive collection of 12 non-personal images for the diary's automatic placeholder rotation.

### Complete prompt

Create a cohesive collection of 12 separate portrait-oriented digital illustrations for a responsive mental-health journaling prototype called “A Digital Diary.” The images should communicate serenity, peace, love, compassion, understanding, hope, emotional warmth, reflection, healing, connection, and gentle resilience.

Use one consistent soft painterly illustration style across the entire collection. Use a harmonious palette built around deep purple, lavender, soft blue, lilac, white, and subtle warm-gold highlights. The mood should feel calm, supportive, inclusive, mature, and emotionally safe—not childish, clinical, gloomy, or overly dramatic.

Create 12 individual images, not a collage, contact sheet, grid, or single combined image. Each image must use a portrait 4:5 composition suitable for cropping inside a CSS-created polaroid frame. Generate full-bleed artwork without a border or built-in frame.

Use these 12 visual themes:

1. Serenity — a still lake at dawn with soft mist and gentle reflections.
2. Peace — a quiet forest path with filtered lavender-blue light.
3. Love — two abstract ribbons of light forming a subtle heart shape.
4. Compassion — gentle hands carefully holding a small warm light, with no identifiable person.
5. Understanding — a softly illuminated bridge connecting two peaceful shores.
6. Calm — moonlight resting across slow ocean waves.
7. Reflection — a lotus and expanding ripples on clear water.
8. Safety — a strong tree creating a protective canopy over a quiet resting place.
9. Hope — birds moving toward light through an open purple-blue sky.
10. Comfort — a warm cup beside a softly lit window with a folded blanket and no readable text.
11. Healing — warm light breaking gently through layered clouds after rain.
12. Connection — a circle of varied wildflowers growing together in harmony.

Do not include readable text, letters, numbers, signatures, logos, watermarks, UI elements, medical symbols, medication, diagnoses, crisis scenes, violence, identifiable faces, personal photographs, or copyrighted characters. Avoid stereotypes about mental health. Keep human representation symbolic and non-identifying.

Return or export the images as 12 separate high-quality PNG files. Use the filenames `frame01.png` through `frame12.png` in the same order as the themes above. Keep the dimensions and visual treatment consistent across the collection.

### Why this is a strong prompt

- Defines the purpose and emotional goals.
- Connects the assets to the established project palette.
- Specifies separate files, orientation, cropping behavior, and filenames.
- Gives each image a distinct theme while preserving one visual system.
- Prevents text, personal content, built-in borders, and inappropriate mental-health imagery.
- Establishes objective review criteria before the images enter the repository.

### Result and decision

Gemini returned 12 separate abstract PNG files and a three-page self-audit report. The collection has a cohesive soft-focus style and avoids faces, personal information, medical claims, and crisis imagery. It does not meet the full approved brief: every image is 1376 x 768 landscape instead of portrait 4:5, the filenames do not use the required sequence, the requested scene list was replaced, purple/lavender is not the primary palette, and every image contains a repeated lower-right four-point mark.

ChatGPT/Codex recommends revision before integration. Mausi's final approval decision is pending, so none of the images have been added to the repository.

### Verification

ChatGPT/Codex independently verified the count, distinct hashes, PNG format, dimensions, orientation, filenames, file sizes, visual consistency, and visible prohibited-content requirements. It also rendered and inspected all three pages of Gemini's report. Testing inside the application's CSS polaroid frame remains pending because the component has not been built and the first collection uses the wrong orientation.

### Files affected

Planned location: `assets/frames/frame01.png` through `assets/frames/frame12.png`.

### Related commit

Add after the approved images are committed.

---

## Prompt 5 - Correct the first Gemini image collection

**Stage:** Visual asset revision  
**AI tool:** Gemini  
**Model:** Gemini 1.5 Flash, as identified in Gemini's supplied report  
**Mode:** Image generation  
**Status:** Submitted; second collection returned and independently audited

### Goal

Preserve the strongest visual qualities of the first output while correcting the requirements that failed independent verification.

### Complete prompt

The complete submitted prompt is preserved in `docs/prompts/GEMINI_SECOND_COLLECTION_PROMPT.md`. It specified the project purpose, exact 12-scene sequence, purple/lavender painterly design system, separate PNG output, 4:5 portrait orientation, 1024 x 1280 target dimensions, sequential filenames, prohibited content, and a per-file verification table.

### Why this follow-up is stronger

- Identifies the exact failures instead of asking generally for improvement.
- Preserves the cohesive qualities that worked.
- Restates orientation, filename, palette, scene, and prohibited-mark requirements.
- Requires per-file evidence before Gemini claims completion.
- Leaves final acceptance with Mausi after independent review.

### Result and decision

Gemini returned 12 improved portrait illustrations and a four-page report identifying the model as Gemini 1.5 Flash. The visuals matched the requested scene sequence and design direction. Independent file inspection found that every image measured 928 x 1152 and used a Gemini-generated filename, even though the report claimed 1024 x 1280 and `frame01.png` through `frame12.png`.

Codex created sequentially named, byte-for-byte identical copies. Mausi accepted the lower-right Gemini platform watermark as intentional AI disclosure, superseding the earlier no-watermark requirement. Exact sizing remains pending.

### Files affected

Renamed copies were prepared in a separate downloadable `assets/frames/` folder. No images have been copied into the project repository yet.

### How I will verify the result

ChatGPT/Codex rendered all four report pages, inspected actual PNG metadata, reviewed visual concepts and prohibited content, verified the renamed copies byte-for-byte, and tested the ZIP archive. See `docs/SECOND_COLLECTION_AUDIT.md`.

---

## Prompt 6 - Correct the exact dimensions of all 12 images

**Stage:** Visual asset correction  
**AI tool:** Gemini  
**Intended model:** Gemini 1.5 Flash  
**Mode:** Image editing and verification  
**Status:** Prepared; result pending

### Goal

Correct only the technical dimensions while preserving the accepted artwork and visible AI watermark.

### Complete prompt

The complete prompt is preserved in `docs/prompts/GEMINI_EXACT_SIZE_PROMPT.md`. It instructs Gemini to extend each 928 x 1152 canvas to 928 x 1160 by naturally adding four pixels at the top and bottom, then resize to exactly 1024 x 1280. It prohibits regeneration, redesign, meaningful cropping, distortion, removal of the accepted watermark, format changes, or unsupported success claims.

### Why this prompt is strong

- Focuses on one remaining problem instead of regenerating approved artwork.
- States the exact width, height, orientation, ratio, and PNG format repeatedly.
- Provides a mathematically exact canvas-correction method.
- Preserves the original composition and accepted AI disclosure mark.
- Requires verification from actual exported-file properties.
- Requires Gemini to report a limitation honestly if its platform cannot export the requested dimensions.

### Result and decision

Pending submission and independent inspection of the returned files.

### Files affected

No repository files yet. Final candidates will be `assets/frames/frame01.png` through `assets/frames/frame12.png` only after exact metadata verification.

### How I will verify the result

Inspect all 12 actual PNG files and require exactly 1024 pixels wide by 1280 pixels high before marking the asset collection complete.

---

## Prompt 7 - Establish live project documentation

**Date:** July 22, 2026  
**Development stage:** Project-process definition  
**AI tool:** ChatGPT/Codex  
**Mode:** Execution  
**Status:** Implemented in the documentation bundle

### Complete prompt

Chat every new prompt and update that we do must be captured and all applied docs be updated with every new change and update that I need you to make sure you are doing as we keep building. Question Chat am I going to have to prompt you to update all docs as we keep working or will you put in your memory while working on this project update all docs as new changes happen in live time?

### Result and decision

Mausi will not need to request documentation updates after every material change. ChatGPT/Codex added a project-level `AGENTS.md` and `docs/DOCUMENTATION_WORKFLOW.md` so the rule travels with the repository and is more reliable than conversational memory alone.

Every relevant document will be updated as prompts, decisions, requirements, tests, AI outputs, bugs, commits, and deployment status change. Unrelated documents will not be edited artificially.

### Files affected

- `AGENTS.md`
- `docs/DOCUMENTATION_WORKFLOW.md`
- All documentation affected by the second Gemini image iteration

### How I verified the result

Reviewed the documentation set for current asset status, preserved the new prompts and evidence, and rebuilt the downloadable documentation bundle.

---

## Prompt 8 - Connect Codex directly to the VSCode repository workflow

**Date:** July 22, 2026  
**Development stage:** Local development setup  
**AI tool:** ChatGPT/Codex  
**Mode:** Teaching and setup guidance  
**Status:** Instructions prepared; repository connection pending

### Complete prompt

Chat how do we get Codex the ability to update all my docs workflow working with me directly alongside my code?

### Result and decision

The recommended setup is to open the actual Git repository as the VSCode workspace, use the Codex IDE extension from that workspace, place the project `AGENTS.md` at the repository root, and keep the documentation files in the same repository. Codex can then edit code and affected documentation during the same active task.

The setup must be verified before implementation by asking Codex to report the repository root and summarize the active `AGENTS.md` instructions without changing files. Codex does not silently monitor unrelated manual edits in the background; after Mausi edits files manually, she can ask Codex to review the current diff and synchronize affected documentation.

### Verification source

Checked the current official OpenAI Codex IDE-extension and `AGENTS.md` documentation. The IDE extension uses open editor context and supports reviewing edits in place. Codex discovers project instructions from the Git root down to the active working directory.

### Remaining action

Open `next_chapter_submission_digital_diary` as the VSCode workspace, copy the documentation bundle into that repository, confirm `AGENTS.md` is at the root, start a fresh Codex IDE chat, and run the read-only verification prompt.

---

## Prompt-entry template

**Prompt number and title:**  
**Date:**  
**Development stage:**  
**AI tool:**  
**Model:**  
**Mode:** Teaching or Execution  

### Goal

### Complete prompt

### Why I wrote the prompt this way

### AI response summary

### Follow-up prompt

### What I accepted

### What I changed or rejected

### Files affected

### How I verified the result

### Related commit
