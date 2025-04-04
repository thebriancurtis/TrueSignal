# `rule_set.json` — Rule Set Schema

Each rule set file contains:
- `rules`: list of rule IDs
- `rule_sets`: list of rule set names to include

## Example
```json
{
  "composable_rules": ["ENF-R001", "CTX-R004"],
  "rule_sets": ["common_structure"]
}
```

## Where Used
- `/internal/rule_sets/` (authoring)
- `/rule_sets/` (compiled)

---

## 🔒 Core Rule Set Behavior

The `core` rule set is automatically merged into every compiled rule set.

- **Do not manually list `"core"`** in the `rule_sets` array.
- Doing so will result in a compilation error.
