# Rule Set Framework

This document defines the architecture, purpose, and enforcement model for rule sets in TrueSignal. Rule sets allow structured composition of rules for validation, classification, runtime behavior, and contributor-facing workflows.

---

## Core Concepts

- **Global Rule Space**: All rules are defined globally and uniquely by ID.
- **Rule Set**: A named, declarative group of rule IDs that are included in a given context.
- **Includes**: Allows a rule set to reference other rule sets or specific rules.
- **Excludes**: Allows a rule set to suppress specific rules from included sources.

---

## Purpose

Rule sets allow:
- Testing and deploying subsets of the corpus
- Domain-specific or contextual rule groupings
- Conflict resolution via exclusion
- Composable logic without inheritance

---

## Design Principles

- Rule IDs are globally unique
- Rule sets are declarative (not inferred or inherited)
- No circular references are allowed
- Composition is preferred over inheritance

---

## Rule Set Example

```json
{
  "core": {
    "includes": ["ED-R005", "FI-R002"],
    "excludes": []
  },
  "sensitive": {
    "includes": ["core", "custom:SEN-R001"],
    "excludes": ["core:UBS-R002"]
  }
}
```

---

## Summary

Rule sets form the outermost layer of control in the TrueSignal rule system. They determine which rules are active, composable, and testable — and they allow precise inclusion without requiring structural or folder-level coupling.
