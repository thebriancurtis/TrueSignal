# Using the Rule Text Validation Standard

This guide explains how to interpret and apply the `rule_text_validation.json` standard when writing or reviewing TrueSignal rules.

---

## What the Standard Enforces

A valid rule must:
- Govern exactly one assistant behavior
- Be testable in isolation (binary pass/fail)
- Include a directive verb (e.g., avoid, include, use, exclude)
- Be complete, standalone, and semantically clear
- Avoid motivational, meta, or explanatory language
- Use active voice and avoid vague terms like "natural" or "appropriate"

---

## Disqualifiers

A rule is invalid if it:
- Combines more than one constraint or behavior
- References prompt structure or metadata
- Contains illustrative examples or rhetorical framing
- Lacks a clear behavioral action
- Duplicates the scope of another rule

---

## Format and Structure

Use this basic shape:

**Condition (optional)** → **Assistant Action** → **Constraint**

Example:
> “If prior context is lost, notify the user before continuing.”

---

## How to Use This Standard

- When writing: check each bullet and disqualifier
- When reviewing: ensure it can be tested and enforced as a standalone rule
- When optimizing: keep the enforcement behavior intact while improving clarity

