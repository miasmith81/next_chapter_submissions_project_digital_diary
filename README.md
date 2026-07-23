# Next Chapter Submissions Project - A Digital Diary

A responsive digital diary prototype that helps users record feelings and possible triggers while experiences are fresh, then revisit entries for personal reflection or optional discussion with a therapist. Built with HTML, CSS, JavaScript, animated page turns, and browser-based storage.

## Live Demo

**Deployment pending.** The GitHub Pages link will be added after the application is built, deployed, and verified.

## Mission Brief

The project provides a familiar digital space where someone experiencing a difficult emotional moment can record what they are feeling and what may have contributed to it. The user can revisit the entry later for personal reflection or choose to discuss it with a therapist.

This admissions project is a functional prototype. It is not therapy, medical advice, diagnosis, emergency monitoring, or a crisis-response service.

## Problem

After a difficult emotional experience, someone may not remember exactly how they felt or what may have triggered the moment. Without those details, it can be harder to process the experience and explain it later during a conversation with a therapist.

## Value

The application gives users a place to record personal feelings while an experience is still fresh. Later, they can revisit what they wrote. If they choose to share the information with a therapist, it may help them discuss what happened, recognize possible patterns, and explore helpful coping strategies together.

## Smallest Demonstration of Value

The application first proves its value when a user can:

1. Write a diary entry.
2. Save the entry.
3. Revisit the entry later.

## Project Plan

1. Establish the repository and documentation foundation.
2. Build and verify the write-save-revisit data flow.
3. Add the empty state, diary name, and responsible deletion controls.
4. Render saved entries dynamically as diary pages.
5. Add the animated book and page-turn interactions.
6. Apply the approved visual identity and decorative images.
7. Verify desktop, mobile, keyboard, storage, and accessibility behavior.
8. Deploy through GitHub Pages and complete the submission audit.

See [Project Plan](./docs/PROJECT_PLAN.md).

## Completed Foundation

- Initial project structure
- Requirements and scope review
- Static-site architecture decision
- Documentation foundation and standing `AGENTS.md` workflow
- Interview preparation for Questions 1-6
- Privacy and browser-storage limitation analysis
- Gemini image prompts and two visual iterations
- Independent audits of both Gemini collections
- Verified sequential filename correction by Codex
- Documented acceptance of Gemini's visible AI-generation watermark

## MVP Features Being Built

- Write and validate a diary entry
- Save entries in the current browser
- Revisit entries after refresh or reopening
- Display entries chronologically
- Show an empty state
- Personalize the diary with a user-entered name
- Delete prototype entries with confirmation
- Responsive desktop and mobile layouts
- Accessible controls and keyboard navigation

## Visual Features Planned

- Closed front and back covers
- Animated opening, closing, and page turns
- Purple, blue, and white palette
- Glassmorphism interface styling
- Handwritten diary typography
- Decorative polaroid-style images
- Mobile swipe navigation that does not interfere with scrolling

## Technologies

- HTML5
- CSS3
- JavaScript
- Web Storage API (`localStorage`) for prototype persistence
- Git and GitHub
- GitHub Pages
- Visual Studio Code

## AI Tools Used

### Claude

Claude supported the original diary and produced a handoff describing its design, animation, architecture, known bugs, and reusable decisions.

### ChatGPT and Codex

ChatGPT/Codex is the lead planning, implementation, documentation, and verification collaborator for the admissions rebuild. It compared the original architecture with the rubric, organized the work, rubber-ducked interview answers, investigated storage limitations, independently audited AI outputs, corrected deterministic filenames, and established the live documentation workflow.

### Gemini

Gemini 1.5 Flash completed two visual iterations. The second collection follows the requested scenes and purple/lavender painterly direction. Independent inspection found that its report overstated the technical results: actual files were 928 x 1152 and used Gemini-generated names rather than the claimed 1024 x 1280 sequential files. Codex created and verified correctly named copies. Mausi accepted Gemini's lower-right mark as AI-generation disclosure. Exact sizing remains pending.

Mausi preserves her own voice, challenges recommendations, makes the final decisions, and verifies important claims before including AI-assisted work.

## Running Locally

This static project requires no package installation or build command.

1. Clone the repository.
2. Open the repository folder in Visual Studio Code.
3. Open `index.html` with Live Server.
4. Use the address displayed by Live Server.

## Project Structure

```text
next_chapter_submission_digital_diary/
├── AGENTS.md
├── assets/
├── css/
├── docs/
│   ├── AI_USAGE_LOG.md
│   ├── ASSET_GENERATION_BRIEF.md
│   ├── DOCUMENTATION_WORKFLOW.md
│   ├── INTERVIEW_PREP.md
│   ├── PLACEHOLDER_IMAGE_AUDIT.md
│   ├── PRIVACY_AND_LIMITATIONS.md
│   ├── PROJECT_PLAN.md
│   ├── PROJECT_REQUIREMENTS_AND_SCOPE.md
│   ├── SECOND_COLLECTION_AUDIT.md
│   ├── evidence/
│   └── prompts/
├── js/
├── BUILD_LOG.md
├── index.html
├── LICENSE
├── prompt-history.md
└── README.md
```

## Storage and Privacy Limitations

Entries in this admissions prototype are stored in the current browser using `localStorage`.

- Entries remain after an ordinary refresh or browser restart.
- Entries are tied to the current browser profile and device.
- Entries do not synchronize across devices.
- Clearing browser site data can remove entries.
- Browser storage must not be described as production-secure storage for sensitive mental-health information.
- Users should enter only non-sensitive demonstration content.

A username and password screen written entirely in client-side JavaScript would not provide real authentication. Secure authentication and per-user backend storage are future production features.

## Documentation

- [Build Log](./BUILD_LOG.md)
- [Prompt History](./prompt-history.md)
- [AI Usage Log](./docs/AI_USAGE_LOG.md)
- [Asset Generation Brief](./docs/ASSET_GENERATION_BRIEF.md)
- [Live Documentation Workflow](./docs/DOCUMENTATION_WORKFLOW.md)
- [Interview Preparation](./docs/INTERVIEW_PREP.md)
- [First Image Audit](./docs/PLACEHOLDER_IMAGE_AUDIT.md)
- [Second Image Audit](./docs/SECOND_COLLECTION_AUDIT.md)
- [Privacy and Limitations](./docs/PRIVACY_AND_LIMITATIONS.md)
- [Project Plan](./docs/PROJECT_PLAN.md)
- [Requirements and Scope](./docs/PROJECT_REQUIREMENTS_AND_SCOPE.md)
- [Documentation Index](./docs/README.md)

## Development Status

The project is in the documentation and MVP-foundation stage. The second image collection is visually accepted and sequential filenames were corrected. Exact 1024 x 1280 sizing remains pending. Documentation will be updated as prompts, decisions, tests, and verified functionality change.

## Author

Mia Smith-Petross - [miasmith81](https://github.com/miasmith81)

## License

See `LICENSE` for license information.
