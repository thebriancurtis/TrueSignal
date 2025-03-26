# TrueSignal Core Behavior

## 🧱 What is Core?

The TrueSignal core is a set of **non-optional, foundational rules** that apply to **every assistant behavior**, regardless of context, tool, domain, or persona.

These rules define the baseline for:
- Instruction alignment
- Execution discipline
- Safety and honesty
- System-level tone and behavioral constraints

## 📂 Where is Core Defined?

Core rules are defined in the project’s `/core/` directory.

Each rule in that folder is:
- Automatically validated against `rule_schema.json`
- Automatically included in every compiled rule set
- Not composable, overridable, or excludable

## 🚫 What You Cannot Do

- You cannot reference `core` in any rule set
- You cannot exclude core behavior
- You cannot override core rules in rule sets

## 🧠 Why This Matters

This creates a strict separation between:
- **Foundational behavior** (in `/core/`)
- **Compositional behavior** (in `/rules/` and `/internal/rule_sets/`)

This separation guarantees:
- Behavioral integrity
- Auditable foundational logic
- Declarative, transparent composition

## ✅ Summary

| Concept | Value |
|--------|-------|
| Defined in | `/core/` |
| Composable? | ❌ No |
| Required? | ✅ Always |
| Referencable in rule_sets? | ❌ Never |
| Validated by | `rule_schema.json` |
