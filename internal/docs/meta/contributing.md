# Contributing Internally

This guide is for contributors working inside the core of TrueSignal — including rules, prompts, schemas, documentation, and standards.

For general contribution guidance, see [CONTRIBUTING.md](../../../CONTRIBUTING.md).  
For writing documentation, see [documentation_principles.md](documentation_principles.md).

---

## 🧱 What This Covers

- How to contribute to internal rule sets and schemas
- How to maintain prompt logic and standards
- Where to place files inside `/internal/`
- Links to validation and tooling
- Expectations for clarity, structure, and documentation

---

## 🧠 Core Responsibilities

If you’re working within `/internal/`, you are likely doing one or more of the following:

- Adding or improving rules in an **uncompiled rule set**
- Writing or refining internal **prompt logic**
- Maintaining or extending **schemas and standards**
- Auditing for **consistency**, **deduplication**, or **coverage gaps**
- Improving internal **documentation** or **workflow files**

---

## 📦 Folder Overview

- `/internal/rule_sets/` — Uncompiled, editable rule sets by category
- `/internal/prompts/` — Prompts used for validation, categorization, optimization
- `/internal/docs/` — Contributor-facing documentation and standards
- `/internal/docs/meta/` — Meta documentation: principles, structure, contribution guides

---

## 🧰 Tooling

- Run `validate_rule_set.json` to check rule structure and coverage
- Use `compile_rule_set.json` to create compiled, user-facing rule sets
- Use `rule_deduplication.json` to ensure rule sets are optimized
- Use `rule_optimization.json` before deduplication for better results
- Refer to `rule_set_schema.json` for authoring rule sets
- Refer to `rule.json` for authoring individual rules

---

## 📝 Documentation Expectations

- Follow the [documentation principles](documentation_principles.md)
- Every document must be purposeful, connected, and accessible
- Use assistant-agnostic, factual language — no filler or hype

---

## 🧭 Design Standards

- Rules must be structured, deduplicated, and tested
- Prompts must use TrueSignal standards wherever possible (via composition)
- Schemas must remain declarative and transparent
- Internal logic should prefer clarity over cleverness

---

## 🧠 Remember

TrueSignal is not a product. It’s a system for designing behavior with clarity.  
Small contributions matter. Consistency matters. Trust is built rule by rule.

