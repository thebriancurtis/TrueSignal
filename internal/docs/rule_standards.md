# Rule Standards in TrueSignal

This document defines how rule standards are structured, governed, and extended within the TrueSignal framework.

## 🧱 Core Convention: Implicit Inheritance

All rule standards in TrueSignal are expected to **implicitly extend** the global base rule standard: `rule.json`. This means:

- Every rule standard **must conform to everything required by `rule.json`**
- Additional fields, restrictions, or validation logic may be layered **on top**
- No `"extends"` field is needed — this relationship is enforced by project convention and validation logic

### ✳️ Why Implicit?
This enforces:
- 🔒 Global consistency across all rules
- 🔁 Simplified schema design with no inheritance complexity
- 🧠 Mental clarity — all rules are at minimum `rule.json`-conformant

## 📐 Structure of a Rule Standard

All rule standards must conform to the `rule_standard_schema.json` meta-schema. This ensures consistency, validation support, and tooling compatibility.

A valid rule standard **must** include:
- `"required"`: An array of required rule fields
- `"properties"`: JSON schema definitions of rule fields
- `"description"`: A plain language explanation of the standard’s purpose
- `"examples"`: One or more example rule objects
- `"type"`: Must always be `"object"`
- `"additionalProperties"`: Boolean that defines strictness

## 🧩 Current Rule Standards

| Standard        | Description |
|----------------|-------------|
| `rule.json`     | The base rule standard. All rules and rule standards must conform to it. |
| `core_rule.json`| A constrained extension of `rule.json` used for TrueSignal core rules. |
| *(embedded)*    | Some rule sets may define their own standards inline, so long as they also conform to `rule.json`. |

## 🧠 Reminder

Any tool, prompt, or validation system must first validate rules against `rule.json`, then layer additional logic from any specific rule standard.

---
