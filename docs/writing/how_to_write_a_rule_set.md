# How to Write a Rule Set

Rule sets are stored in `/internal/rule_sets/{category}/{name}.json` and compiled into `/rule_sets/{category}/{name}.json`

## What Goes in a Rule Set
- `rules`: A list of rule IDs
- `rule_sets`: Optional list of other sets to include

See [`rule_set.json`](../reference/rule_set.json.md)

## Categories
Use a category from [`rule_set_categorization.json`](../reference/rule_set_categorization.json.md)

## 🔒 Core Rule Set

**Do not include `core` in the `rule_sets` array.**

- The `core` rule set is always included automatically during compilation.
- If you try to include it manually, **compilation will fail.**

## Validate and Compile
1. Validate with: `validate_rule_set.json`
2. Compile with: `compile_rule_set.json`