# Admissions Interview Preparation

## 1. What problem does your application solve?

This application is built for anyone dealing with mental-health challenges. After a difficult moment, they may not remember exactly how they felt or what may have triggered it. Without those details, it can be harder to process the experience and work through it with a therapist.

## 2. What value does your application create?

The application gives users a place to record personal feelings and what has upset them while the experience is still fresh. Later, they can revisit that emotional experience. If they choose to share it with their therapist, it may help them discuss what happened, recognize possible patterns, and explore helpful coping strategies together.

## 3. Why did you choose this solution?

I chose a digital diary because journaling gives people a space for personal reflection. Making it digital allows users to record an experience while it is still fresh and revisit it later. I designed it to look and feel like a personal diary because that familiarity can create comfort and ownership, while recognizing that the visual design is separate from how information is stored and protected.

## 4. How did you decide what to build first?

I identified the smallest version that proves the application's value: a user must be able to write an entry, save it, and revisit it later. I decided to build and test that core functionality before personalization, styling, images, and animation. This makes the code easier to understand and lets me debug essential features before introducing visual complexity.

**Update after development:** Confirm the actual build order and add commit references.

## 5. How did AI help during development?

My AI tools helped me break the project into manageable pieces so I could address every submission requirement. I preserve my own tone and ideas while reviewing refined options, but I make the final decisions. I act as the orchestrator by using Teaching Mode when I need to rubber-duck and Execution Mode when a defined task is ready.

A specific example is the visual-asset workflow. The first Gemini collection failed several requirements, so I requested a stronger second iteration from Gemini 1.5 Flash. The second collection matched my visual direction, but its report claimed the files were 1024 x 1280 and correctly named when actual files were 928 x 1152 with Gemini-generated names. I assigned deterministic naming to Codex, which created and verified `frame01.png` through `frame12.png`, and used a focused prompt for the remaining size issue. I also made the human decision to keep Gemini's visible mark because I want users to know the images were AI-generated. This shows that I can assign tasks to appropriate tools, verify claims, revise requirements intentionally, and keep final control.

**Update after development:** Add exact-size results, coding examples, repository integration, verification, and commits.

## 6. Was there a time you challenged an AI suggestion?

I originally planned to build with React, Express, and Neon, but an AI review showed that this conflicted with the requirement to deploy a static HTML, CSS, and JavaScript application through GitHub Pages. The static recommendation made sense, but I questioned whether `localStorage` could protect personal entries by adding a username and password.

I asked AI to verify the security claim and learned that a JavaScript login screen would not provide real authentication because JavaScript running on the website can still access stored data. I decided to treat the submission as a functional prototype using non-sensitive demonstration entries, document its limitations clearly, and identify authenticated per-user storage as a future feature.

This showed me that I should challenge AI recommendations, verify important claims, and make the final decision myself.

## 7. What was the most interesting bug?

**Pending:** Complete with a real bug, investigation steps, AI collaboration, solution, verification, and commit.

## 8. How did you verify the application?

**Pending:** Complete with actual manual tests, responsive checks, accessibility checks, browser checks, persistence tests, and deployment verification.

## 9. What would you improve with another weekend?

A production version would add real authentication, per-user authorization, secure backend storage, cross-device access, and appropriate privacy and security review. Refine after final prototype scope is known.

## 10. What are you most proud of?

**Pending:** Answer after completion using genuine work and evidence.
