# Contributing Guidelines for Test Writers

Thank you for helping expand the TrueSignal instruction set and test suite.

## How to Add New Tests

1. Create a new JSON file in the `tests/` directory (or append to an existing category).
2. Each test case must contain:
   - `id`: A unique identifier (e.g., `FMT003`)
   - `instruction`: The related instruction module (filename)
   - `prompt`: A short, testable prompt to evaluate AI behavior
   - `expected_behavior`: A clear and specific outcome that defines success

3. Test files must use the structure: `{ "tests": [ ... ] }`
4. Update `chat_test_framework.json` with the new filename.
5. Ensure your test supports one or more models listed in `support_matrix.json`.

See sample test files for formatting examples.
