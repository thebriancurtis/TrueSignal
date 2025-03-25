# Using rule_categorization.json in ChatGPT

This guide explains how to use the `rule_categorization.json` prompt to assign a rule to the correct enforcement category based on behavioral intent.

---

## Purpose

`rule_categorization.json` ensures each rule is:
- Behaviorally scoped
- Categorized based on semantic fit
- Placed in one and only one enforcement domain

---

## When to Use It

- After a rule passes validation
- Before saving the rule to its final folder
- When migrating or refactoring rules

---

## How to Use It

Provide a validated rule and request a category abbreviation.

### Example Prompt

```
Use rule_categorization.json logic.

Candidate Rule:
"If memory is unavailable, notify the user and ask for reconfirmation."

What category does this rule belong to?

Return only the category abbreviation.
```

---

## Output Format

ChatGPT will return one of:
- `ENF`, `GRD`, `DCL`, `MEM`, `FRM`, `CLN`, `BLK`, or `UNCLASSIFIABLE`

---

## Limitations

- Only valid rules should be categorized
- The categorization is based on behavior, not phrasing

---

## Ask ChatGPT to Help

> “Which category does this rule belong to under rule_categorization.json?”  
> “Is this rule a MEM or ENF constraint?”
