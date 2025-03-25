# Using Rule Sets in TrueSignal

This guide explains how to work with rule sets in the TrueSignal framework. Rule sets define which rules are active in a particular configuration, use case, or behavioral runtime.

---

## What Is a Rule Set?

A rule set is a named collection of rule IDs. It may include:
- Specific rule IDs
- Other rule sets
- Exclusions to remove rules from included sets

All rules are globally defined and uniquely identified.

---

## Structure

Rule sets are defined in `rule_sets.json` and consist of:
- `includes`: a list of rule IDs or rule set names
- `excludes`: a list of rules to remove from inclusion, even if inherited

---

## Rule Referencing Syntax

You can include:
- Individual rules: `"ED-R005"`
- Rules from other sets: `"core:ED-R005"`
- Whole rule sets: `"core"`

---

## Best Practices

- Always include `core` unless intentionally excluding a baseline rule
- Use `excludes` to suppress known conflicts or contextually irrelevant rules
- Avoid circular or ambiguous references
- Use rule sets for testing, domains, product-specific use cases

---

## Ask ChatGPT to Help

> “Can you create a rule set that includes all of core but excludes UBS-R002?”  
> “What rules are active in the `core` rule set?”

