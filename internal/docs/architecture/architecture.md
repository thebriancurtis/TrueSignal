# Architecture

This document explains the structure and flow of the TrueSignal rule system.

## Components
- `rules/`: atomic constraints
- `internal/rule_sets/`: editable rule set definitions
- `rule_sets/`: compiled, validated rule sets
- `internal/standards/`: logic constraints and fallback policies
- `prompts/`: validation, categorization, optimization tools

## Flow
```
[rules] ─→ [validate, deduplicate] ─→ [categorize] ─→ [optimize] ─→ [compile rule sets]
```