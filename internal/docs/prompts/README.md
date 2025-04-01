# Prompt Index

This document summarizes all prompts used in TrueSignal — both internal toolchain prompts and user-facing instruction prompts.

---

## 🧭 Prompt Types

### 🔧 Internal Prompts (`/internal/prompts/`)
Used for validation, transformation, and compilation. Manually run in an AI assistant or composed into higher-level flows.

| Prompt | Purpose |
|--------|---------|
| `validate_rule.json` | Checks atomicity, teachability, testability |
| `optimize_rule.json` | Shortens rule language without losing intent |
| `rule_deduplication.json` | Flags potential overlap with existing rules |
| `rule_consolidation.json` | Merges redundant rules |
| `is_core_rule.json` | Determines whether a rule belongs in `core` |
| `validate_rule_set.json` | Checks rule set structure and references |
| `compile_rule_set.json` | Merges and validates rule set + core |
| `suggest_rule_set_category.json` | Classifies rule set by theme |

### 💬 User-Facing Prompts (`/prompts/`)
Prompts designed to be used directly by an AI assistant users (currently none published).

User-facing prompts:
- Must conform to `prompt.json`
- Should reference compiled rule sets by link
- Should expose helpful assistant functionality (e.g. enforcement, optimization)

---

## 📎 Prompt Format

All prompts must conform to:
- [`prompt.json`](../../docs/reference/prompt.json.md)

Required fields:
- `description`
- `input_format`
- `output_format`
- `example_input`
- `example_output`
- `instruction`

---

## 🔗 Related Docs

- [How to Write a Prompt](../../docs/writing/how_to_write_a_prompt.md)
- [prompt.json Schema](../../docs/reference/prompt.json.md)
