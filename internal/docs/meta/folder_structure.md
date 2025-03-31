# Folder Structure

This document describes the organizational structure of the TrueSignal project and its documentation.

---

## 📂 /docs/

User-facing documentation for anyone using TrueSignal with an AI assistant.

- `index.md` — Entry point for all user documentation
- `getting_started.md` — How to begin using rule sets and prompts
- `glossary.md` — Definitions of key terms used across the project
- `usage/` — How to use compiled rule sets in prompts
- `writing/` — How to write reusable rules and prompts

---

## 📂 /internal/docs/

Contributor-facing documentation for people maintaining or extending TrueSignal.

### 📁 /internal/docs/meta/

- `project_principles.md` — Guiding values for the entire TrueSignal project
- `documentation_principles.md` — Expectations for writing and reviewing documentation
- `contributing.md` — Internal contribution guidelines and standards
- `folder_structure.md` — This file
- `index.md` — Meta documentation index

### 📁 /internal/docs/prompts/

- `index.md` — Describes prompt roles and types used internally

---

## 📂 /standards/

Public-facing JSON schemas used to define and validate rules, rule sets, and prompts.

- `rule.json` — Schema for authoring an individual rule
- `rule_schema.json` — Validation schema for structured rules
- `rule_set_schema.json` — Schema for authoring uncompiled rule sets
- `prompt.json` — Schema for writing reusable assistant prompts
- `README.md` — Explains the use and structure of each standard

---

## 📂 /internal/standards/

Internal-only standards and schemas used in rule processing and tooling logic.

- Files related to internal validation, categorization, naming, and workflows

---

## 📂 /rule_sets/

User-facing, compiled rule sets organized by theme.

- Each folder contains a compiled `.json` rule set
- Includes all applicable rules, including those from the core rule set

---

## 📂 /internal/rule_sets/

Source rule sets authored by contributors.

- Organized by theme
- Used as input for rule set compilation
- Each folder contains one or more raw rule definitions

---

## 📂 /internal/prompts/

Internal prompt files used for categorizing, validating, optimizing, and deduplicating rules.

- Prompt JSON files follow the `prompt.json` schema
- Used manually or in composition with other prompts

