# TrueSignal Standards

This directory contains public JSON schemas used to define and validate rules and rule sets.

These schemas ensure structure, consistency, and clarity across the project.

---

## Included Schemas

- `prompt_schema.json` — Schema for defining reusable assistant prompts
- `rule_schema.json` — Structural schema for individual rule validation
- `rule.json` — Schema for authoring an individual rule
- `rule_set_schema.json` — Schema for authoring a rule set (before compilation)
- `rule_categorization.json` — Defines assistant behavior categories used for organizing rules

---

These standards are intended for anyone writing, validating, or using structured rules with an AI assistant.



Defines the categories used to classify assistant behavior at the rule level.
Used for organizing and evaluating rules in conjunction with [rule.json](./rule.json).

- [`rule_set_categorization.json`](./rule_set_categorization.json) — Defines the official categories for rule sets, used to determine where compiled rule sets belong and how they are composed.
