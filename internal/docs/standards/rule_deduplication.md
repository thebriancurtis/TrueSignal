# Rule Deduplication

Every rule must be logically distinct from other existing rules. This ensures the rule set remains minimal, non-redundant, and easy to teach.

---

## 🚫 What Counts as a Duplicate?

- Expresses the same constraint with different words
- Overlaps heavily in behavioral intent
- Is covered fully by another rule

---

## ✅ What’s Not a Duplicate?

- Applies in a different context (e.g., language vs. tone)
- Has a stricter or orthogonal constraint
- Builds on another rule without repeating it

---

## 🛠 How It Works

- Use the `deduplicate_rule.json` prompt
- It compares a new rule against existing rules
- It returns `{ duplicate: true/false }` plus an explanation

---

## 🔎 Example

```json
{
  "candidate": "The assistant must avoid speculation.",
  "existing": "The assistant must only state things it can verify."
}
→ duplicate: true
```

---

## 🔗 Related

- `validate_rule.json`
- [`rule_authoring_standards.md`](rule_authoring_standards.md)
