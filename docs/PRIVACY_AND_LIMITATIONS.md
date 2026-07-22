# Prototype Privacy and Limitations

## What this application is

This project is an admissions-level functional prototype demonstrating how a user can write, save, and revisit diary entries in a responsive web application.

## What this application is not

- It is not a production-secure mental-health record system.
- It is not therapy, diagnosis, medical advice, or crisis support.
- It does not create therapist accounts or automatically share entries.
- It does not provide real user authentication.

## Browser-storage behavior

Entries are stored in the current browser using `localStorage`.

This means:

- Entries remain after an ordinary refresh or browser restart.
- Entries are tied to the current browser profile and device.
- Entries do not synchronize across devices.
- Clearing site data can remove the entries.
- Someone with access to the same browser profile may be able to inspect the stored information.
- JavaScript running on the same website can access the stored information.

Users should enter only non-sensitive demonstration content in this prototype.

## Why the prototype does not include a password screen

A username and password interface written entirely in client-side JavaScript would hide the interface but would not create trusted authentication or authorization. Presenting that screen as security would be misleading.

## Responsible prototype controls

- Display a clear prototype limitation notice.
- Provide a delete-my-entries control with confirmation.
- Do not include personal diary entries in the repository or live demo.
- Do not collect names, email addresses, diagnoses, therapy information, or other unnecessary personal data.
- Do not include passwords, tokens, credentials, or private information in code, commits, prompts, screenshots, or documentation.

## Future production requirements

A production version would require professional architecture and review, including:

- Secure server-side authentication
- Proper password hashing or trusted identity-provider integration
- Per-user authorization
- Protected session management
- Secure backend storage
- Encryption and key-management decisions
- Privacy policy and data-retention policy
- Threat modeling and security testing
- Legal and professional review appropriate to sensitive mental-health information

