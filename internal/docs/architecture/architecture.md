# System Architecture

This document explains how rules, rule sets, prompts, and standards work together in the TrueSignal system.

---

## 🧱 System Layers

### Authoring Layer

| Component | Description |
|----------|-------------|
| `/rules/` | Atomic rule definitions |
| `/internal/rule_sets/` | Thematic collections of rule IDs |
| `/internal/standards/` | Rule structure, duplication, optimization, categorization standards |
| `/internal/prompts/` | Prompts used for validation, compilation, and tooling |

### Compilation & Validation Layer

| Component | Description |
|----------|-------------|
| `validate_rule.json` | Ensures atomicity, teachability, testability |
| `deduplicate_rule.json` | Prevents overlap with existing rules |
| `compile_rule_set.json` | Flattens, validates, and assembles rule sets |
| `rule_set_categorization.json` | Taxonomy for organizing sets by theme |

### Runtime / Usage Layer

| Component | Description |
|----------|-------------|
| `/rule_sets/` | Fully compiled rule sets |
| `/prompts/` | End-user prompts that apply compiled logic |

---

## 🔁 Compilation Flow

```
rules/
  ↓ validate + deduplicate
internal/rule_sets/
  ↓ compile_rule_set
rule_sets/  ← includes core.json
```

- All compiled rule sets include:
  - Their declared rules
  - Any nested `rule_sets`
  - The `core` rule set (automatically)
- Output is a single, flat, deduplicated JSON file

---

## 🧠 Design Principles

- ✅ Rule authorship is separated from enforcement
- ✅ Compilation enforces consistency and prevents duplication
- ✅ Prompt-based validation provides structured, testable workflows
