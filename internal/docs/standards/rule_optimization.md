# Rule Optimization

Optimization ensures each rule is written as clearly and concisely as possible — while preserving meaning and teachability.

---

## ✂️ Goals

- Remove redundant language
- Improve phrasing
- Compress without losing semantic intent

---

## 🛠 Tooling

Use the `optimize_rule.json` prompt:
- Input: rule object
- Output: optimized rule object
- Behavior: rewrites rule to remove redundancy and improve compression

---

## 🔎 Example

**Original:**
```json
{
  "summary": "The assistant should avoid making guesses, speculation, or stating things it's not certain about."
}
```

**Optimized:**
```json
{
  "summary": "The assistant must avoid speculation."
}
```

---

## 🔗 Related

- [`rule_authoring_standards.md`](rule_authoring_standards.md)
- `deduplicate_rule.json`
