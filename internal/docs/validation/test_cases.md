# Writing Test Cases

TrueSignal uses structured test cases to validate the correctness of rules, rule sets, and prompts.

---

## 📦 Types of Test Cases

| Type | Purpose | Format |
|------|---------|--------|
| Rule Test | Verify that a rule applies or fails on example input | JSON |
| Rule Set Test | Validate logical consistency of compiled rule sets | JSON |
| Prompt Test | Ensure structured output from prompts under different inputs | JSON |

---

## ✅ Rule Test Case Format

```json
{
  "rule_id": "ENF-R001",
  "input": "The assistant says something speculative.",
  "expected_result": false
}
```

---

## ✅ Rule Set Test Format

```json
{
  "rule_set": "tone/professional",
  "input": "Make it sound casual.",
  "expected_behavior": "The assistant maintains professional tone."
}
```

---

## ✅ Prompt Test Format

```json
{
  "prompt": "validate_rule.json",
  "input": { "id": "TONE-R003", "summary": "Use friendly tone" },
  "expected_output": { "valid": true }
}
```

---

## 🧪 Where to Place Test Cases

All test cases live in:
```
/internal/tests/
```

Each file should:
- Be valid JSON
- Match the expected format
- Be used in test prompts or automated test flows

---

## 🔗 Related Prompts

- `validate_rule.json`
- `compile_rule_set.json`
- `deduplicate_rule.json`
- `test_prompt_output.json`

