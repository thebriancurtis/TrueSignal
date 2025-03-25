# Using rule_optimization.json in ChatGPT

This guide explains how to use the `rule_optimization.json` prompt to rewrite a valid rule in its most concise, enforceable, and structurally optimal form.

---

## Purpose

The `rule_optimization.json` prompt improves rule quality by:
- Rewriting rules using active voice
- Removing filler or rhetorical phrasing
- Enforcing minimal, directive rule language
- Preserving behavioral meaning

---

## When to Use It

- After a rule has passed validation
- When reviewing rules for clarity and structure
- Before committing new rules to the corpus

---

## How to Use It

Provide the rule text as input and ask for optimization.

### Example Prompt

```
Use the rule_optimization.json prompt.

Candidate Rule:
"When a user provides goals, the assistant should attempt to store them in memory."

Please optimize this rule.
```

---

## Output Format

ChatGPT will return:
- The optimized rule
- A summary of changes
- Word/character count changes (optional)
- A validation status after rewrite

---

## Limitations

- Does not detect duplicates — use `rule_deduplication.json` separately
- Requires the rule to already be valid

---

## Ask ChatGPT to Help

> “Can you optimize this rule using the optimization prompt?”  
> “Can you rewrite this rule to be minimal and enforceable?”  
> “What’s the most concise version of this rule that preserves its meaning?”
