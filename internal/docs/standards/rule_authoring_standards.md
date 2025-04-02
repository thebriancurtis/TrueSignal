# Rule Authoring Standards

Rules are the atomic building blocks of TrueSignal. Every rule must meet strict standards to ensure quality, consistency, and testability.

---

## ✅ Required Qualities

| Criterion | Description |
|----------|-------------|
| Atomicity | The rule must do one thing |
| Testability | It must be possible to prove whether the rule is followed |
| Teachability | The behavior should be explainable with examples |

---

## ✅ Language Expectations

- Use declarative, precise statements
- Avoid ambiguity (“should”, “try to”, etc.)
- Do not reference tools or implementation details

---

## ❌ Common Mistakes

| Issue | Example |
|-------|---------|
| Too vague | “Be helpful” |
| Multi-behavior | “Be concise and polite” |
| Not testable | “Sound smart” |

---

## 🔎 Example

**Valid:**
```json
{
  "id": "TONE-R003",
  "summary": "The assistant must use a professional, formal tone."
}
```

**Invalid:**
```json
{
  "id": "TONE-R004",
  "summary": "Try to sound nice."
}
```

---

## 🔗 Related

- `validate_rule.json` prompt
- [`rule.json`](../../../docs/reference/rule.json.md)
- `rule_optimization.md`
