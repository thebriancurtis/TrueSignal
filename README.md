# TrueSignal

**TrueSignal** is a modular, rigorously tested instruction set designed to optimize AI assistant behavior. It improves reliability, execution discipline, truthfulness, and user value—while maintaining compatibility across all supported ChatGPT models and prompting styles.

![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)

## 🔍 Overview

TrueSignal ensures:

- Execution-first responses (no delays, disclaimers, or deferrals)
- Truth-by-default, with graceful support for fictional or creative prompts
- Strategic clarification instead of harmful assumptions
- Utility maximization, depth-first and breadth-aware answers
- Compatibility with ChatGPT Free, Plus, and API users

---


## 🚀 Getting Started

### 🧠 Use the Instruction Set

You can use `master_instruction_set.json` in two ways:

**Option 1: Upload the File**
1. Download `master_instruction_set.json`
2. Upload it into ChatGPT
3. Reference it like:
   ```
   Use the uploaded TrueSignal instruction set when completing this prompt.
   ```

**Option 2: Reference the GitHub Repository**
```
Follow the instruction set at https://github.com/thebriancurtis/TrueSignal
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

## 🤝 Contributing

Pull requests and issue submissions are welcome! Please see:
- [`CONTRIBUTING.md`](CONTRIBUTING.md)

## 🧪 In-Chat Testing Instructions

# In-Chat Testing Instructions (TrueSignal)

This guide shows how to run TrueSignal test cases **within any chat-based interface**, including ChatGPT (Free and Plus).

---

## ✅ Method 1: Smart In-Chat Harness (Manual Paste-In)

Paste the following prompt into ChatGPT (preferably GPT-4) to run a batch of test cases. Replace the sample test data with any relevant entries from the test suite.

```
You are now a test runner for the TrueSignal instruction set.

I will provide you with test cases in the following format:
- `prompt`: the input to test
- `expected_behavior`: the correct output

For each test:
- Run the prompt
- Return your actual response
- Evaluate whether the response matches the expected_behavior
- Output: pass/fail, explanation

Test Case Format:
1.
prompt: "Ask the AI to retain your name and goal over the course of a session. Verify if it remembers and uses the data to improve output."
expected_behavior: "AI correctly stores and recalls name and goal across turns, and explains memory usage."

2.
prompt: "Provide multiple similar entries for storage. Ask the AI to optimize or compress them."
expected_behavior: "AI consolidates overlapping memories and removes redundancy while preserving intent."

Begin running the tests and reporting results.
```

---

## ✅ Method 2: In-Chat Testing from Uploaded Test File (ChatGPT Plus Required)

If you're using ChatGPT Plus with file upload:

1. Upload any of the test suite files from the `tests/` directory (e.g., `memory_optimization_tests.json`)
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

---

## 🧠 Notes

- These instructions are optimized for models with advanced context tracking such as **GPT-4 or Claude**.
- For ChatGPT Free users (GPT-3.5), functionality may be limited:
  - Use Method 1 only
  - Expect shorter context handling and no file upload
  - Run fewer tests per session to avoid cutoff or loss of earlier prompt memory

- This method allows full testing without needing external code, tools, or setup.
