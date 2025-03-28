# 🧪 TrueSignal Prompt Testing Suite

## Overview

This suite contains world-class tests for every internal prompt in the TrueSignal project. Tests are designed to ensure:

- ✅ Schema compliance
- ✅ Correct structure and types
- ✅ Logical consistency
- ✅ Handling of malformed, minimal, and edge-case input

---

## 🗂️ File Structure

```
/internal/tests/
├── test_prompts/
│   ├── is_core_rule.json
│   ├── rule_optimization.json
│   └── ...
├── test_runner.json
└── test_suite.md
```

Each file in `test_prompts/` contains tests for exactly one prompt.

---

## ✅ Test Format

```json
{
  "description": "Describes what the prompt does",
  "tests": [
    {
      "name": "Test case name",
      "input": { ... },
      "expected_keys": ["key1", "key2"],
      "assertions": {
        "key": "expected_value"
      },
      "expected_error": "if applicable"
    }
  ]
}
```

---

## 🧪 Test Types

| Type               | Description                                           |
|--------------------|-------------------------------------------------------|
| Valid              | Based on prompt example input/output                  |
| Minimal Valid      | Smallest valid structure                              |
| Missing Fields     | Required field(s) omitted                             |
| Wrong Types        | Mismatched types (e.g. string vs. int)                |
| Edge Cases         | Ambiguous or logically extreme input                  |

---

## 🚦 How to Run Tests

Specify a test file:

```json
{
  "test_suite": "internal/tests/test_prompts/is_core_rule.json"
}
```

This is run via the `test_runner.json` prompt.

---

## 🧠 Best Practices

- Add 5–10 tests per prompt minimum
- Favor edge cases and boundary violations
- Document any known exceptions or fuzzy logic
- Assert both structure and intent

