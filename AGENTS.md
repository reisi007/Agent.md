# AI Agent Guidelines (AGENTS.md) - Template Management Project

This document contains the core guidelines for AI agents working on creating, refining, and managing `AGENTS.md` templates for other projects.

## 1. Core Purpose & Role
* **Meta-Level Thinking:** Your primary job is to abstract specific coding issues into general rules. You are building the "laws" for other AI agents.
* **Proactive Rule Suggestion:** Continually analyze interactions to suggest new standard rules. If you notice a recurring prompt correction, propose adding it to the relevant template.

## 2. The Golden Rule of Rule-Making (Abstraction vs. Implementation)
* **Critical Evaluation:** Before adding any new rule to an `AGENTS.md` template, you MUST weigh whether it is a global, architectural principle or a localized implementation detail.
* **Global Rules:** If a rule applies to the entire architecture, security, or general workflow (e.g., "Always use responsive images", "Never hardcode ENV variables"), it belongs in the `AGENTS.md`.
* **Local Rules:** If a rule is highly specific to a single function or component workaround, DO NOT add it to `AGENTS.md`. Instead, instruct the agent to write a detailed inline code comment in the respective file to explain the *why* behind the logic.
* **Mandatory Documentation:** Enforce in all templates that methods and functions must have comprehensive block comments.

## 3. Template Environment Constraints
When generating or modifying templates, strictly differentiate between target environments:
* **CLI Templates:** Must enforce token minimization, the use of native shell operations (cp, mv, sed), and strictly forbid full-file outputs.
* **Web/Chat Templates:** Must enforce complete, copy-pasteable file outputs without snippets or diffs to prevent manual merging errors. Update exceptions only apply to the `AGENTS.md` file itself, where only new sections should be provided.

## 4. Language & Formatting Standards
* **Language Policy:** All templates, rules, and internal documentation MUST be written in English. If the target project has a different user-facing language (e.g., German), specify this clearly in the template's language policy.
* **Scannability:** Keep rules concise. Use bolding for key terms and bullet points for lists. Avoid long prose.
* **No Redundancy:** Keep the templates as clean and short as possible. Do not repeat standard programming knowledge (e.g., "write clean code") unless tied to a specific project constraint (e.g., "remove all dead code entirely").