# Using rule_consolidation.json in ChatGPT

This guide explains how to use `rule_consolidation.json` to resolve behavioral overlap between two or more rules using merge, replacement, or removal.

---

## Purpose

This prompt helps you:
- Merge rules with complementary constraints
- Replace multiple rules with one superior version
- Retire redundant or superseded rules
- Justify resolution using enforcement logic

---

## When to Use It

- After rules are flagged by `rule_deduplication.json`
- During large-scale rule reviews or cleanup
- When merging similar rules across versions

---

## How to Use It

Provide a candidate rule and its overlapping reference rules.

### Example Prompt

```
Use rule_consolidation.json logic.

Candidate Rule:
"Retain user guidance after memory resets."

Reference Rules:
1. "Preserve user-defined expectations across sessions."
2. "Store user constraints unless reset."

What is the optimal consolidated rule?

Return type, merged rule, and justification.
```

---

## Output Format

ChatGPT will return:
- `consolidated_rule`: the final rule, or null
- `consolidation_type`: one of [replacement, merge, keep_one, remove_all, no_action]
- `rules_retired`: rules superseded
- `rationale`: explanation of decision

---

## Limitations

- Only apply to semantically overlapping rules
- Requires understanding of behavioral enforcement domains

---

## Ask ChatGPT to Help

> “Can you merge these rules using rule_consolidation.json?”  
> “Which rule should we keep or replace based on behavioral scope?”
