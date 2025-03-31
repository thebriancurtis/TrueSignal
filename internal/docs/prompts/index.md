# Prompt Index

This document summarizes all system-level prompts used to validate, categorize, optimize, or compile rules and rule sets.

---

## 📋 Prompt Registry

| Prompt | Purpose | Input | Output | Related Standards |
|--------|---------|-------|--------|-------------------|
| `validate_rule.json` | Check rule atomicity, teachability, testability | Rule JSON | `{ valid: true/false }` | `rule_authoring_standards.md`, `rule.json` |
| `deduplicate_rule.json` | Detect semantic overlap | Rule JSON + rule base | `{ duplicate: true/false }` | Rule uniqueness |
| `optimize_rule.json` | Improve clarity, brevity, compressibility | Rule JSON | Rule JSON | `rule_optimization.md` |
| `suggest_rule_set_category.json` | Classify rule set theme | Rule Set JSON | `{ category: "tone" }` | `rule_set_categorization.json` |
| `compile_rule_set.json` | Merge and validate full rule set | Raw rule set JSON | Compiled rule set JSON | `rule_set.json`, `core` auto-inclusion |
| `validate_rule_set.json` | Schema + semantic check | Rule set JSON | `{ valid: true/false }` | `rule_set_framework.md` |

---

## 📄 Format and Structure

All prompts must conform to [`prompt.json`](../../docs/reference/prompt.json.md)

They must include:
- Description
- Input/output format
- Example input/output
- Full ChatGPT-native instruction block

---

## 📎 Related Docs

- [Writing a Prompt](../../docs/writing/how_to_write_a_prompt.md)
- [Internal Prompt Authoring](how_to_write_an_internal_prompt.md)
