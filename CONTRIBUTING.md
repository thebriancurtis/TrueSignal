# Contributing to TrueSignal

Thank you for your interest in contributing to the TrueSignal project!

This guide explains how to contribute to both the **instruction set** and the **test suite**. Contributions should follow the structure and metadata requirements outlined below.

---

## 📘 Contributing to the Instruction Set

The instruction set is organized into **modular category files** in the `/instructions/` directory. Each file defines a specific area of behavioral guidance.

### 🔄 Modifying an Existing Instruction

- Locate the appropriate category file in `/instructions/`.
- Edit the relevant entry within the `instructions` array.
- Preserve formatting, clarity, and alignment with the file’s tone and structure.
- Do **not** modify `master_instruction_set.json`.

### ➕ Adding a New Instruction to an Existing Category

- Open the relevant file in `/instructions/` and append your instruction to the `instructions` array.
- Follow the formatting conventions of that file.
- Do **not** edit the master file.

### 🆕 Adding a New Instruction Category

- Create a new `.json` file inside `/instructions/`.
- Add your instruction(s) under an `instructions` array.
- Include the following top-level metadata:

```json
{
  "project": "TrueSignal",
  "version": "[project version]",
  "source_repository": "https://github.com/thebriancurtis/TrueSignal"
}
```

- Register your new file in `master_instruction_set.json` by adding its path to the `includes` array.

---

## 🧪 Contributing to the Test Suite

Tests are located in the `/tests/` directory and are used to validate the instruction set.

### ➕ Adding a New Test

- Create a new file in `/tests/` or append to an existing one.
- Structure your file with a `tests` array.
- Each test should include:
  - `id`
  - `prompt`
  - `expected_behavior`
  - `failure_criteria`

### 🛠 Modifying a Test

- Locate the relevant test file.
- Edit the fields to improve clarity or align with updated instruction logic.

### Metadata for Test Files

Each test file must include the following metadata:

```json
{
  "project": "TrueSignal",
  "version": "[project version]",
  "source_repository": "https://github.com/thebriancurtis/TrueSignal"
}
```

---

## ✅ Final Notes

- Only modify `master_instruction_set.json` when adding or removing an entire category file.
- Keep changes concise, clear, and purpose-driven.
- When in doubt, open an issue or discussion before starting a pull request.

Thank you for contributing to TrueSignal!
