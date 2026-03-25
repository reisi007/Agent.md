# AI Agent Guidelines - Template Management

## 🎯 Purpose
This repository serves as the central hub for managing, refining, and distributing `AGENTS.md` templates. These templates establish the "laws" and operational constraints for AI coding agents working across different development environments. 

Instead of writing instructions from scratch for every new project, this repository provides standardized, battle-tested guidelines that ensure AI agents write clean, secure, and maintainable code while adapting strictly to their execution context (CLI vs. Web UI).

## 🚀 Added Value & Core Features

* **Environment-Specific Optimization:** * **CLI Templates:** Enforces token minimization and strict use of native shell commands (e.g., `sed`, `awk`) while strictly forbidding full-file outputs to optimize performance and prevent destructive overwrites.
  * **Web/Chat Templates:** Mandates complete, copy-pasteable file outputs without snippets to prevent manual merging errors.
* **The "Golden Rule" of Abstraction:** Clearly defines what belongs in a global AI prompt (architectural principles, security constraints) versus what should be written as localized inline code comments (specific workarounds).
* **Strict Quality & Language Policies:** Enforces English for all codebase architecture and comments, while keeping user-facing strings in the target language (e.g., German). It also mandates dead code removal and comprehensive method documentation.
* **Security by Default:** All templates instruct AI agents to never hardcode environment variables, to proactively evaluate routing/authentication vulnerabilities, and to maintain a stateless architecture.

## 📁 Repository Structure
* `AGENTS.md`: The meta-level guidelines for AI agents working *on* these templates.
* `/template/cli/AGENTS.md`: Optimized for terminal-based AI agents (e.g., Cursor, Aider).
* `/template/web/AGENTS.md`: Optimized for web-based AI interactions (e.g., ChatGPT, Claude UI).

## 🛠️ Usage
Copy the appropriate `AGENTS.md` file from the `template/` directory into the root of your target project. The AI agent analyzing your repository will automatically pick up the rules and adjust its behavior accordingly.
