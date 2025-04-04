# Rule Set Framework

This document defines how rule sets are structured, categorized, and compiled within the TrueSignal system.

---

## 📁 File Locations

| Location | Purpose |
|----------|---------|
| `/internal/rule_sets/{category}/{name}.json` | Authorable, raw rule sets |
| `/rule_sets/{category}/{name}.json` | Compiled, flattened rule sets ready for use |
| `/standards/rule_set_categorization.json` | Defines theme categories |
| `/docs/reference/rule_set.json.md` | Rule set schema definition |

---

## 📦 Rule Set Schema

Authorable rule sets must match the `rule_set.json` schema:

```json
{
  "composable_rules": ["ENF-R001", "CTX-R002"],
  "rule_sets": ["shared_structure"]
}
```

- `rules` must reference known rule IDs
- `rule_sets` must reference other rule sets in the same or other categories
- `core` must **not** be included — it will be automatically injected during compilation

---

## 🧠 Compilation Behavior

When you run `compile_rule_set.json`, the system will:

1. Validate your input structure
2. Recursively include all nested rule sets
3. Inject the `core` rule set automatically
4. Deduplicate all rule IDs
5. Output a flattened `.json` file into `/rule_sets/{category}/`

### Example

```json
// internal/rule_sets/tone/educational.json
{
  "composable_rules": ["TONE-R007"],
  "rule_sets": ["shared_structure"]
}
```

→ Compile

```json
// rule_sets/tone/educational.json (output)
{
  "composable_rules": [
    "TONE-R007",
    "ENF-R001",   // from core
    "CTX-R004",   // from shared_structure
    ...
  ],
  "rule_sets": []
}
```

---

## ✅ Rule Set Constraints

| Constraint | Required |
|------------|----------|
| Must not include `core` manually | ✅ |
| Must validate against `rule_set.json` | ✅ |
| All referenced rule sets must exist | ✅ |
| Must compile without errors | ✅ |
| Output must be flat and deduplicated | ✅ |

---

## 🔁 Category Behavior

Each rule set belongs to a category defined in:
```
/standards/rule_set_categorization.json
```

Categories include: `tone`, `persona`, `tool`, `audience`, `context`, etc.

Use `suggest_rule_set_category.json` to classify new sets.


---

## 📦 Runtime Usage

Compiled rule sets are designed to be used **as-is**.

- Do not attempt to merge or deduplicate them at runtime
- Simply refer to them by file path or GitHub URL in your prompt
- Each includes the `core` rule set and is fully validated


---

## ✍️ Contributor Workflow

To contribute a new rule set:

1. Create it in `/internal/rule_sets/{category}/`
2. Conform to `rule_set.json` and naming conventions
3. Use `suggest_rule_set_category.json` to check classification
4. Validate it using `validate_rule_set.json`
5. Compile it using `compile_rule_set.json`
6. Submit the compiled output to `/rule_sets/{category}/`

Do not include `"core"` in `rule_sets`. It will be automatically included during compilation.

---

## 🔗 Related Prompts

- `validate_rule_set.json`
- `compile_rule_set.json`
- `suggest_rule_set_category.json`
