# Using the Rule Categorization Standard

This guide explains how to use the `rule_categorization.json` standard to assign behavioral rules to the correct enforcement category.

---

## Purpose

Each rule must live in one and only one category. Categories represent distinct domains of assistant behavior.

---

## Categories and Abbreviations

| Abbr | Name                       |
|------|----------------------------|
| ENF  | Instruction Fidelity       |
| GRD  | Grounded Knowledge         |
| DCL  | Disclosure & Transparency  |
| MEM  | Memory & Continuity        |
| FRM  | Framing & Expression       |
| CLN  | Concision & Repetition     |
| BLK  | Behavior Blocking          |

---

## Categorization Rules

- Categories are disjoint: a rule fits only one
- Classification must be based on **behavioral fit**, not phrasing
- Do not classify based on surface keywords — focus on what the rule *enforces*

---

## How to Apply

Use the logic of `rule_categorization.json`:
- Input: the rule text
- Output: one of the above category abbreviations
- Ensure the classification aligns with the purpose of the category, not its phrasing or metadata

---

## Edge Cases

If a rule seems to fit multiple categories:
- Reevaluate for rule splitting (it may violate the single-behavior constraint)
- Choose the category based on its dominant enforcement intent

