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
Follow the rules at https://raw.githubusercontent.com/thebriancurtis/TrueSignal/refs/heads/main/rule_sets/rules.json
```

---

## 🧪 Run the Test Suite (Chat-Native)

1. Upload `tests.json`.
2. Then enter the following prompt:

```
You are now a test runner for the TrueSignal instruction set.

The uploaded file contains test cases. Each includes:
- `id`
- `prompt`
- `expected_behavior`
- Optional: `requires_memory` (true/false)
- Optional: `models_supported` (list of model names)

Instructions:
1. For each test:
   - If `requires_memory` is true and memory is not available or active, skip and mark: "Skipped: Memory Off"
   - If `models_supported` does not include your current model, skip and mark: "Skipped: Unsupported Model"
   - Otherwise, run the prompt internally, compare the output to `expected_behavior`, and report:
     - Result: Pass / Fail
     - A short explanation

2. Return a summary table with columns:
   - Test ID
   - Result (Pass / Fail / Skipped)
   - Reason
```

---
---

## 📚 Documentation Index

### 🧱 Core System
- [Core Rule System](internal/docs/core_rule_system.md)

### ✍️ Rule Authoring
- [How to Write a Rule](internal/docs/how_to_write_a_rule.md)
- [Rule Categorization Standard](internal/docs/rule_set_categorization.md)
- [Rule Schema Overview](internal/docs/rule_schema.md)

### ⚙️ Validation Workflow
- [Validation Workflow](internal/docs/workflow.md)
- [Rule Deduplication and Consolidation](internal/docs/rule_deduplication_and_consolidation.md)

### 🔎 Usage Guides
- [Using Rule Sets](internal/docs/using_rule_sets.md)
- [Using Rule Optimization Prompt](internal/docs/using_rule_optimization_prompt.md)
- [Using Rule Categorization Prompt](internal/docs/using_rule_categorization_prompt.md)
- [Using Rule Deduplication with ChatGPT](internal/docs/using_rule_deduplication_with_chatgpt.md)
- [Using Rule Text Validation Standard](internal/docs/using_rule_text_validation_standard.md)

### 📐 Standards and Theory
- [Rule Standards](internal/docs/rule_standards.md)
- [Rule Optimization Theory](internal/docs/rule_optimization_theory.md)
- [Rule Text Validation Theory](internal/docs/rule_text_validation_theory.md)
- [Category Theory and Justification](internal/docs/category_theory_and_justification.md)


## 🧾 License

This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Maintained by:  
**Brian Curtis**  
GitHub: [@thebriancurtis](https://github.com/thebriancurtis)  
LinkedIn: [https://linkedin.com/in/thebriancurtis](https://linkedin.com/in/thebriancurtis)  
Project Repository: [https://github.com/thebriancurtis/TrueSignal](https://github.com/thebriancurtis/TrueSignal)
