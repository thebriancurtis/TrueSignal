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
