# core_rule_set_reference.json

## What
Specifies the location of the compiled core rule set for systems that need to read but not compile it.

## Why
Allows safe referencing of the immutable core rule set without exposing raw core rules.

## Fields

### core_rule_set_path
- **Type**: string
- **Description**: Path to the compiled `core.json` rule set file.
- **Value**: `rule_sets/core.json`
- **Constraints**:
  - Path must be relative.
  - File must match `core.json`.

## Conventions
- Used by tools or prompts that need to include or reference the core rule set by location.
