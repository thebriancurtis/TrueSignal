# Glossary: Core Concepts

---

### ✅ Rule
A single behavior constraint (e.g. “Avoid speculation”)

- Format: JSON (`rule.json`)
- Must be atomic, testable, and teachable
- Lives in `/rules/`
- Validated using `validate_rule.json`

---

### 📦 Rule Set
A named collection of rule IDs that belong to a shared theme

- Defined in `/internal/rule_sets/`
- Compiled into `/rule_sets/`
- Must conform to `rule_set.json`
- Categorized by `rule_set_categorization.json`

---

### 🔄 Compilation
The process of validating and merging a rule set and its dependencies

- Uses `compile_rule_set.json`
- Automatically includes the `core` rule set
- Output is flat, deduplicated, ready for use

---

### 📜 Core Rule Set
Universal rules enforced in all compiled rule sets

- Not manually included
- Automatically merged by compiler

---

### 🧠 Prompt
A structured, reusable ChatGPT-native instruction

- Stored in `/prompts/` (user) or `/internal/prompts/` (toolchain)
- Must follow `prompt.json` schema
- Validates, categorizes, optimizes, deduplicates

---

### 🧪 Test Case
Example-based validation of a rule, rule set, or prompt

- Lives in `/internal/tests/`
- Often embedded inline or used by test prompts

---

### 🧰 Standard
A constraint or meta-rule governing rule text, testability, deduplication, etc.

- Includes `rule_authoring_standards.md`, `rule_optimization.md`, etc.
- Referenced by prompts and schema enforcement
