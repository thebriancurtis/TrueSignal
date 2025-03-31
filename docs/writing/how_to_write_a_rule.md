# How to Write a Rule

Rules are atomic constraints on assistant behavior. Each rule must be precise, teachable, testable, and structurally valid.

---

## ✅ Rule Requirements

| Criterion | Description |
|----------|-------------|
| Atomicity | Rule does one thing only |
| Testability | Rule can be verified through examples |
| Teachability | A human can understand and apply it |
| Clarity | Direct, formal, unambiguous phrasing |

---

## 📄 Schema Compliance

All rules must conform to two schemas:

- [`rule.json`](../reference/rule.json.md): structural format
- [`rule_schema.json`](../reference/rule_schema.md): semantic requirements

---

## 🛠 Rule Authoring Workflow

Follow this exact sequence:

1. ✍️ **Author** your rule in `/rules/{theme}/`  
2. ✅ **Validate** using `validate_rule.json`
3. ✂️ **Optimize** using `optimize_rule.json`
4. 🔁 **Check for duplication** with `rule_deduplication.json`
5. 🧩 **If overlapping**, consolidate using `rule_consolidation.json`
6. 🧠 **Determine if it's core** using `is_core_rule.json`
   - If yes, move it to: `/rules/core/`

---

## ❌ Common Mistakes

| Issue | Example |
|-------|---------|
| Vague | “Try to be nice” |
| Multi-constraint | “Be concise and polite” |
| Not testable | “Act smart” |
| Tool-specific | “Use a numbered list in Notion” |

---

## 🔗 Related Prompts

- `validate_rule.json`
- `optimize_rule.json`
- `rule_deduplication.json`
- `rule_consolidation.json`
- `is_core_rule.json`
