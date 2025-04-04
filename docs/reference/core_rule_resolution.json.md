# core_rule_resolution.json

## What
Defines the fixed location of the core rules used during core rule set compilation.

## Why
Ensures core compilation is locked to a single, trusted directory and cannot be overridden or extended.

## Fields

### core_rule_dir
- **Type**: string
- **Description**: The only valid path from which core rules may be loaded.
- **Value**: `internal/core`
- **Constraints**:
  - Must point to exactly one directory.
  - Must not match any allowed rule directories in `rule_set_resolution.json`.

## Conventions
- Used only by `compile_core_rule_set.json`.
- Path must be relative to the prompt root.
