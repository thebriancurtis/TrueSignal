# How to Write a Rule in TrueSignal

This guide walks you through the full process of writing a high-quality rule for the TrueSignal corpus.

---

## When to Write a Rule

Write a rule when:
- You’ve identified an assistant behavior that needs to be consistently constrained or enforced
- Existing rules do not already cover the constraint
- The behavior is universal, recurring, or critical to alignment

---

## Step-by-Step Process

### 1. Define the Behavior

What *specific* action should the assistant take or avoid?  
Keep it simple, atomic, and testable.

### 2. Write the Rule

Follow the format:
> Condition (optional) → Assistant behavior → Constraint

Use directive verbs. Avoid passive voice or vague language.

### 3. Validate the Rule

Check against the `rule_text_validation.json` standard:
- Is it valid?
- Is it enforceable?
- Is it a single behavioral constraint?

### 4. Optimize the Rule

Use `rule_optimization.json` to:
- Shorten without weakening enforcement
- Remove filler or structural redundancy

### 5. Check for Duplicates

Run the rule through `rule_deduplication.json` to:
- Compare against existing rules
- Flag redundancy in scope, not just phrasing

### 6. Classify the Rule

Use `rule_categorization.json` to assign it to:
- `ENF`, `MEM`, `GRD`, etc.
- Ensure it fits based on **behavioral enforcement**, not topic

### 7. Submit the Rule

- Add it to the appropriate directory (usually `internal/rules`)
- If submitting a rule set, define it in `rule_sets.json`

---

## Summary

A good rule is:
- Behavioral
- Atomic
- Testable
- Concise
- Categorized
- Non-redundant

Every rule you write shapes the assistant’s contract with users. Write deliberately.
