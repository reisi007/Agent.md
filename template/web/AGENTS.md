# AI Agent Guidelines (AGENTS.md) - Web Environment

This document contains repository-specific context, architectural decisions, and strict rules for AI agents working on this project via Web UI.

## 1. AI Interaction & Output Formatting
* **Complete Code Output:** When proposing code changes or updating a file, ALWAYS output the entire, complete code of that file. Do not use snippets, diffs, or omit sections with comments like `// ... existing code ...`.
* **Rule Update Exception:** When updating this `AGENTS.md` file, only provide the specific new rules or sections to be added, not the entire document.
* **Proactive Rule Suggestion & Placement:** Proactively suggest new rules if you identify recurring patterns or pitfalls. You must critically weigh whether a learning is a general, project-wide rule (add to `AGENTS.md`) or a localized implementation detail. Localized details MUST be written directly as code comments.

## 2. Language & Documentation Policy
* **Language Requirements:** All code, underlying architecture, variable names, and comments MUST be in English. User interface strings (dialogs, labels, frontend content) MUST be in German.
* **Mandatory Method Comments:** Every method and function MUST have complete documentation blocks (including params and return types). Comments must explain the *why* behind the logic, not just parrot the syntax. Do not write comments that merely describe your latest modifications (e.g., `// Added feature X`); comments must describe the system's timeless state.

## 3. Code Quality & Maintenance
* **Code Cleanliness:** Do not leave empty functions, obsolete code blocks, or placeholder comments.
* **Dead Code Removal:** Remove unused functions and styles entirely to keep the codebase clean and maintainable.

## 4. Security & Architecture
* **Environment Variables:** Never hardcode sensitive data. Pass keys, tokens, and credentials via environment variables.
* **Proactive Security Evaluation:** Point out potential security vulnerabilities (e.g., in routing or authentication) and offer robust solutions before executing the primary task.
* **Destructive Actions:** Any UI action that mutates or deletes data MUST be protected by explicit confirmation mechanisms (e.g., dialogs or checkboxes).
* **Statelessness:** The application backend should remain stateless where applicable; avoid relying on server-side session variables for critical state.