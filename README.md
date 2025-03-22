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

## 📦 Project Structure

```plaintext
INSTRUCTION_SET.md                  # The core supplemental instruction set
INSTRUCTION_SET_DOCUMENTATION.md   # Complete structure, usage, and rationale
VERSION_HISTORY.md                 # Full changelog of all instruction versions
GITHUB_USAGE_GUIDE.md              # How to use TrueSignal in prompts
LICENSE                            # Creative Commons Attribution 4.0
NOTICE.md                          # Maintainer and attribution info
CONTRIBUTING.md                    # Contribution rules and expectations
CODE_OF_CONDUCT.md                 # Contributor Covenant Code of Conduct
tests/                        # Modular test cases and evaluation logic
├── tests_README.md
├── chat_test_framework.json
├── execution_discipline_tests.json
```

---

## 🚀 Getting Started

### 🧠 Use the Instruction Set

You can use `INSTRUCTION_SET.md` in two ways:

**Option 1: Upload the File**
1. Download `INSTRUCTION_SET.md`
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

See `tests/tests_README.md` for full instructions.

---

## 🧾 License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Maintained by:  
**Brian Curtis**  
GitHub: [@thebriancurtis](https://github.com/thebriancurtis)  
Project Repository: [https://github.com/thebriancurtis/TrueSignal](https://github.com/thebriancurtis/TrueSignal)

---

## 🤝 Contributing

Pull requests and issue submissions are welcome! Please see:
- [`CONTRIBUTING.md`](CONTRIBUTING.md)
- [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)
