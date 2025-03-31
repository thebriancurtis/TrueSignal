# How to Write a Prompt (User-Facing)

TrueSignal prompts are self-contained an AI assistant-native instruction files designed to guide or constrain assistant behavior.

They are stored in `/prompts/` and used by anyone interacting with an AI assistant or TrueSignal APIs.

---

## ✅ Prompt Format

All prompts must conform to [`prompt.json`](../reference/prompt.json.md). Required fields include:

- `description`
- `input_format`
- `output_format`
- `example_input`
- `example_output`
- `instruction` (an AI assistant prompt content)

---

## 🧱 Composition

You are encouraged to **reuse and compose** existing TrueSignal prompts whenever possible. For example:

- Use `validate_rule.json` before categorizing
- Combine `deduplicate_rule.json` and `optimize_rule.json` for rule preparation

---

## 📦 Referencing Rule Sets in Prompts

TrueSignal rule sets are structured `.json` files containing behavior constraints.

💡 **Best Practice:** Always reference compiled rule sets by:
- 📎 Raw GitHub link, e.g.:
  ```
  https://raw.githubusercontent.com/your-org/TrueSignal/main/rule_sets/persona/investigator.json
  ```
- 📁 File path (if using uploads), e.g.:
  ```
  rule_sets/domain/legal_guidance.json
  ```

**Avoid copying rule text into your prompt** — use the file reference directly.

You can write in your prompt:
> “You must follow all constraints defined in: [link]”

---

## 🔗 Related Standards

Prompts may reference or enforce standards from:
- `rule.json`
- `rule_set.json`
- `rule_set_categorization.json`
- `rule_authoring_standards.md`

Always indicate dependencies in the prompt metadata.

---

## 🛠️ Example Prompt: `optimize_rule.json`

```json
{
  "description": "Shortens a rule without losing meaning.",
  "input_format": "A valid rule object.",
  "output_format": "Optimized rule object.",
  "example_input": { "id": "...", "summary": "..." },
  "example_output": { "id": "...", "summary": "..." },
  "instruction": "Compress this rule's language..."
}
```
