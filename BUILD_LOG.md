# Build Log

This chronological log records significant project decisions, changes, verification results, and next steps. Dates should be expanded with exact dates from Git history when the repository is connected.

## 1. Original concept and reset decision

- Began with a personal digital diary implemented with React, Express, and Neon.
- Completed the admissions prework and reviewed the submission requirements.
- Decided to restart the admissions build as static HTML, CSS, and JavaScript for GitHub Pages compatibility.
- Preserved the core diary idea, visual direction, color palette, animation concept, and ability for users to personalize the diary.
- Removed Mausi's personal diary entries from the submission concept.

## 2. Minimum viable product defined

- Defined the first proof of value as the ability to write an entry, save it, and revisit it later.
- Prioritized working functionality before personalization, images, styling polish, and animation.
- Chose localStorage for prototype persistence.
- Documented that client-side localStorage is not secure storage for sensitive mental-health information and that a client-side username/password screen would not solve that limitation.

## 3. Interview preparation started

- Rubber-ducked the intended user, the problem, the value proposition, the digital-diary choice, and the minimum viable experience.
- Refined answers while preserving Mausi's meaning and voice.
- Deferred implementation-dependent interview questions until real build evidence exists.

## 4. First Gemini image collection

- Prompted Gemini to create 12 calming placeholder images.
- Received 12 landscape images using soft blue, green, peach, and neutral colors.
- Independently inspected the files and retained the audit evidence.
- Determined that the collection did not meet the later portrait 4:5 requirement.

## 5. Second Gemini image collection

- Revised the image prompt to make composition and collection consistency more explicit.
- Received 12 portrait images with generic Gemini filenames.
- Independently verified that the downloaded files were 928 x 1152 RGBA PNGs, not the 1024 x 1280 pixels stated in Gemini's report.
- Defined deterministic filenames `frame01.png` through `frame12.png`.
- Accepted the lower-right Gemini mark as intentional AI-generation disclosure.
- Created a final correction prompt requiring exactly 1024 x 1280 pixels.

## 6. Live documentation rule adopted

- Established a standing project rule: every material prompt, decision, implementation change, verification result, and limitation must be captured as the project progresses.
- Added `AGENTS.md` so Codex working inside the repository follows this documentation workflow.
- Confirmed that `prompt-history.md` belongs in the repository root so Codex can update it alongside the code.

## 7. Documentation folder restored

- The previously generated documentation output was no longer present in the working folder.
- Reconstructed the latest documentation set from the current project record and available source evidence.
- Included planning, requirements, privacy, interview preparation, AI usage, asset briefs, both image audits, exact prompts, source requirements, and workflow instructions.
- Packaged the reconstructed folder as a fresh ZIP and tested the archive before delivery.

## Next Build Actions

1. Add the restored documentation to the repository.
2. Generate or resize the 12 images to exactly 1024 x 1280 pixels and verify every output.
3. Build the functional diary flow: create, save, list, open, and revisit an entry.
4. Test the core behavior before adding styling, personalization, imagery, or animation.
5. Record real implementation decisions and use them to complete interview questions 7 and 8.
