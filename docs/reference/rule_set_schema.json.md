# `rule_set_schema.json`

Defines the structure of TrueSignal rule set definitions (`rule_set.json` format).

## 🔍 Purpose
- Used to validate rule sets before they are compiled
- Enforces correct `uses_rule_sets`, rule references, and metadata

## 🔑 Key Fields
- `name`, `description`: Required string metadata
- `uses_rule_sets`: List of included sets by reference
- `rules`: Inline rule definitions or references
- `notes`, `category`: Optional documentation and grouping

## 🔗 Related
- [Compiled Rule Sets](/rule_sets/)
- [`rule_set_categorization.json`](/docs/reference/rule_set_categorization.json.md)
- [Rule Set Principles](/docs/principles/rule_sets.md)
