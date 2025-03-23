# TrueSignal

**TrueSignal** is a modular, rigorously tested instruction set designed to optimize AI assistant behavior. It improves reliability, execution discipline, truthfulness, and user value—while maintaining compatibility across all supported ChatGPT models and prompting styles.

![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)

## 🔍 Overview

TrueSignal ensures:

- Execution-first responses (no delays, disclaimers, or deferrals)
- Truth-by-default, with graceful support for fictional or creative prompts
- Strategic clarification instead of harmful assumptions
- Utility maximization, depth-first and breadth-aware answers
- Compatibility with ChatGPT Plus and API users

---


## 🚀 Getting Started

### 🧠 Use the Instruction Set

```
Follow the rules at https://raw.githubusercontent.com/thebriancurtis/TrueSignal/refs/heads/main/master_instruction_set.json
```

---

## 🧪 Run the Test Suite (Chat-Native)

To test if an AI model is aligned with TrueSignal:

1. Upload all files in `/tests/` including:
   - `chat_test_framework.json`
   - Each `*_tests.json` file
2. Paste this test prompt into ChatGPT:

```
You are a test harness for the TrueSignal project. Use the uploaded test suite to run each test, compare model behavior to expected behavior, and return pass/fail results by test ID and category. Be strict.
```

3. Review summary output and address failures as needed.


---

## 🧾 License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Maintained by:  
**Brian Curtis**  
GitHub: [@thebriancurtis](https://github.com/thebriancurtis)  
LinkedIn: [https://linkedin.com/in/thebriancurtis](https://linkedin.com/in/thebriancurtis)  
Project Repository: [https://github.com/thebriancurtis/TrueSignal](https://github.com/thebriancurtis/TrueSignal)

---

# 🧪 In-Chat Testing Instructions

1. Upload `chat_test_framework.json`.
2. Then enter the following prompt:

```
You are now a test runner for the TrueSignal instruction set.

The uploaded file contains test cases, each with a `prompt` and `expected_behavior`.

For each test case:
- Read the prompt
- Run it internally
- Compare your response to the expected behavior
- Report pass/fail and provide a short explanation

Respond with a summary table showing test ID, result, and reason.
```
