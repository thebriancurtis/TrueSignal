# Folder Structure

This document describes the organizational structure of the TrueSignal documentation system.

---

## 📂 /docs/

User-facing documentation for anyone using TrueSignal with an AI assistant.

- `index.md` — Entry point for the user docs
- `getting_started.md` — How to start using rule sets and prompts
- `glossary.md` — Terminology used throughout the project
- `usage/` — How to use compiled rule sets
- `writing/` — How to write rules and prompts

---

## 📂 /internal/docs/

Contributor-facing documentation for people working on TrueSignal itself.

### 📁 /internal/docs/meta/

Meta-level documentation for organizing and maintaining the system.

- `documentation_principles.md` — Principles that guide how documentation is written across the project
- `project_principles.md` — High-level principles that guide the project's purpose and values

### 📁 /internal/docs/prompts/

Documentation for internal tooling prompts.

- `index.md` — Describes prompt roles and categories

---

## 📂 /standards/

Public-facing schemas for defining rules, rule sets, and prompts.

- `rule.json` — Schema for authoring an individual rule
- `rule_schema.json` — Schema for validating structured rules
- `rule_set_schema.json` — Schema for rule set authoring (pre-compilation)
- `prompt.json` — Schema for authoring reusable assistant prompts
Standards for rules, prompts, schemas, and validations.

- Files describing schema expectations and JSON structure
