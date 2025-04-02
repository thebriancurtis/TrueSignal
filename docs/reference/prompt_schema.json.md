# `prompt.json` Schema

This schema defines the structure for all TrueSignal prompts — both user-facing and internal. Prompts are designed to validate, optimize, or apply rules and rule sets in structured, composable ways.

## 📐 Purpose

The schema ensures that prompts:
- Are modular and testable
- Use a consistent structure for inputs, logic, and outputs
- Can declare which standards, rule sets, and constraints they depend on
- Are interpretable by both humans and tooling

## 🔑 Key Fields

| Field             | Type      | Required | Description |
|------------------|-----------|----------|-------------|
| `name`           | `string`  | ✅       | A short, descriptive name for the prompt |
| `description`    | `string`  | ✅       | Summary of what the prompt does and how |
| `uses_standards` | `array`   | ❌       | List of standards this prompt relies on (e.g., `rule.json`) |
| `uses_rule_sets` | `array`   | ❌       | List of compiled rule sets the prompt references |
| `inputs`         | `object`  | ✅       | Describes the structure and expected fields of user inputs |
| `output_format`  | `object`  | ✅       | Describes the expected structure of the AI assistant's response |
| `examples`       | `array`   | ❌       | Optional usage examples including inputs and outputs |
| `notes`          | `string`  | ❌       | Additional guidance or constraints for use |

## 📎 Related Files

- [prompt.json](/standards/prompt.json) — the canonical schema
- [How to Write a Prompt](/docs/prompts/how_to_write_a_prompt.md)
- [Prompt Principles](/docs/principles/prompt.md)

## 🧠 Guidelines

Prompts should:
- Be declarative, not procedural
- Rely on TrueSignal rule sets via composition
- Produce reliable, observable outputs
- Be testable using structured inputs and outputs

