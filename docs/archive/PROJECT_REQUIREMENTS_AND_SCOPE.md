# Project Requirements and Scope

## Project

**Next Chapter Submissions Project - A Digital Diary**

**Applicant:** Mia Smith

Project documentation should refer to the applicant as `Mia`, using `Mia Smith` only when a full name is needed.

## Product Purpose

Build a responsive digital diary prototype for people dealing with mental-health challenges. It allows a user to record feelings and possible triggers while an experience is fresh, then revisit the entry later for personal reflection or optional discussion with a therapist.

## Admissions Architecture

- Static HTML, CSS, and JavaScript
- Deployable through GitHub Pages
- No required build system or backend server
- Browser-based prototype persistence using `localStorage`
- Non-sensitive demonstration data only

## Core Value Requirement

The first working milestone must allow a user to:

1. Write an entry.
2. Save the entry.
3. Revisit the entry later.

Functionality must be verified before adding personalization, complex styling, images, or animation.

## Submission Documentation Requirements

- Keep one project `README.md` with the required project story, live demo when deployed, problem, value, plan, features, technologies, AI tools, and local-running instructions.
- Maintain `docs/prompt_history.md` as a curated record of the prompts that best demonstrate how Mia collaborates with AI.
- Prioritize evidence of planning, curiosity, iteration, debugging, verification, questions, follow-ups, and requests for code explanation.
- Preserve actual prompt wording when it is important evidence, or link to the complete prompt when it is maintained separately.
- Maintain meaningful commit history and keep reviewer-facing documentation synchronized with the actual repository.
- Do not include secrets, private diary content, or unsupported claims about AI outputs or completed functionality.

## Privacy Boundary

- This is a functional admissions prototype, not a production-secure mental-health platform.
- `localStorage` is readable by JavaScript running on the same site.
- A client-side username/password screen is not real authentication.
- Do not claim secure accounts, per-user authorization, encrypted cloud storage, therapy, diagnosis, monitoring, or crisis support.
- Users should enter only non-sensitive demonstration content.

## Preserved Visual Direction

- Purple, blue, and white gradient palette
- Inter for interface text
- Caveat for handwritten diary text
- Glassmorphism styling
- Floating background and entrance animations
- Animated diary beginning closed and opening into pages
- Page-turn interaction
- Taped polaroid-style decorative frames
- Twelve non-personal illustrations rotating automatically
- Responsive desktop and mobile experience

## MVP Features

- Editable diary name stored in the current browser
- New-entry form
- Optional entry title and mood
- Save to browser storage
- Chronological saved-entry rendering
- Revisit after refreshing or reopening
- Empty state
- Delete-my-entries control with confirmation
- Responsive layouts
- Clear prototype and storage notices

## Placeholder-Image Requirements

- Store approved images in `assets/frames/`.
- Use `frame01.png` through `frame12.png`.
- Use exact 1024 x 1280 dimensions and portrait 4:5 composition.
- Use a cohesive purple, blue, lilac, white, and warm-gold painterly system.
- Do not include personal photos, identifiable people, unrelated readable text, logos, medical claims, diagnoses, crisis scenes, or copyrighted characters.
- Every final AI-created image must visibly state `AI-generated artwork — Directed by Mia`; this disclosure is the only approved readable text inside the final asset.
- Preserve a generator's platform watermark when Mia approves it, but do not depend on a generator-specific mark as the project's only disclosure.
- Preserve C2PA and SynthID provenance when available. Verify the final post-processed file before claiming either signal remains.
- If provenance metadata or an invisible watermark cannot be verified after cropping, resizing, or conversion, keep the visible disclosure and record the technical result honestly.
- Preserve original generated exports separately from final project-ready files.
- Do not include a built-in polaroid border; CSS supplies the frame.
- Rotate through all 12 and wrap to the first.
- Verify dimensions, filename, visible disclosure, display crop, safety, and available provenance signals for every final asset before repository integration.

## Postponed Features

- Cloud database
- Express backend
- User accounts
- Real authentication and authorization
- Cross-device synchronization
- Custom uploads
- Therapist accounts or automatic sharing
- Social or shared diaries

## Future Production Direction

A production version would require authenticated per-user authorization, secure backend storage, appropriate encryption and retention controls, cross-device synchronization, and professional privacy and security review.
