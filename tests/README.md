# Chat-Native Test Runner Instructions

This project includes a modular, prompt-based test suite organized under the `/test` directory.

## ✅ What It Tests

Each `.json` file defines:
- One module of the TrueSignal instruction set (e.g., Execution Discipline)
- Multiple test cases including:
  - `prompt`: what to send to the model
  - `expected_behavior`: what should happen
  - `failure_criteria`: how to tell if it fails

## 📂 Structure

- `chat_test_framework.json`: An index of all test categories
- `/test/*.json`: Actual categorized test cases

---

## 🧪 How to Run Tests Using ChatGPT

1. **Upload the following files into your ChatGPT conversation**:
   - `chat_test_framework.json`
   - All JSON files in `/test/` (e.g., `execution_discipline_tests.json`, `clarification_tests.json`, etc.)

2. **Paste this test runner prompt** into the conversation:

```
You are a test harness for the TrueSignal project. The uploaded files include:
- A framework index (chat_test_framework.json) that lists all test modules
- Multiple test case files (e.g., execution_discipline_tests.json)

Load and process all tests. For each:
- Run the prompt
- Evaluate whether the model behavior matches `expected_behavior`
- Flag it as PASS or FAIL based on `failure_criteria`
- Summarize results by test ID, category, and outcome

At the end, provide:
- Total tests run
- Total passed
- Total failed
- Any edge cases or ambiguous results

Be strict. Use TrueSignal's expectations, not lenient defaults.
```

3. **Review the model’s output for summary + failure reasons.**

---

## 🔁 Re-running Tests

You can re-run tests at any time by:
- Uploading updated `.json` files
- Using the same test runner prompt

If you're a developer, this framework can be expanded into an automated tool using the OpenAI API and GitHub Actions.

---

## 🧠 Why It Works

This chat-native approach leverages ChatGPT's ability to:
- Read uploaded files
- Parse structured test definitions
- Simulate response evaluation using TrueSignal's expectations
