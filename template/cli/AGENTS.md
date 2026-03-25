# AI Agent Guidelines (AGENTS.md) - CLI Environment

This document contains repository-specific context, architectural decisions, and strict rules for AI agents operating in this project via CLI.

## 1. AI Interaction & Workflow Constraints (Strict)
* **Minimize Token Usage:** Optimize all outputs for brevity. Do not explain standard programming concepts unless explicitly asked.
* **Native File Operations:** Use native shell commands (e.g., `cp`, `mv`, `rename`, `sed`, `awk`, or `patch`) for file manipulations instead of rewriting files from scratch.
* **NO FULL FILE OUTPUTS:** It is strictly forbidden to output the entire content of a file. Only output the necessary diffs, precise search/replace blocks, or targeted modifications.
* **Proactive Rule Suggestion & Placement:** Proactively suggest new rules if you identify recurring issues. Critically evaluate whether a new learning is a general architectural rule (which belongs in this `AGENTS.md`) or a specific implementation detail. If it is specific, implement it as a code comment instead.

## 2. Language & Documentation Policy
* **Language Requirements:** All code, inline code comments, and documentation MUST be written in English. User-facing UI strings (menus, dialogs, texts) MUST be implemented in German.
* **Mandatory Method Comments:** All methods and functions MUST be documented correctly using standard block comments (e.g., PHPDoc, JSDoc). These comments must describe the parameters, return types, and most importantly, the *why* behind complex or non-obvious logic, not just the *what*.

## 3. Code Quality & Maintenance
* **Code Cleanliness:** Do not leave empty functions, obsolete code blocks, or placeholder comments.
* **Dead Code Removal:** Remove unused functions and all their corresponding calls entirely to keep the codebase clean.

## 4. Security & Architecture
* **Environment Variables:** Never hardcode sensitive data (API tokens, passwords, webhooks). Always use environment variables.
* **Proactive Security Evaluation:** Always evaluate routing, authentication, and state management for potential vulnerabilities or bypasses before executing tasks.
* **Destructive Actions:** Any action that deletes data or files MUST be protected by a strict confirmation mechanism.
* **Statelessness:** Maintain a stateless architecture where possible (e.g., avoid standard PHP sessions if token-based routing is used).