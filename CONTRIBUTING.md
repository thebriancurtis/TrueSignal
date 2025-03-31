# Contributing to TrueSignal

**Bring clarity to assistant behavior — with structured rules and reusable prompts.**
Write it once. Validate it forever. All signal, none of the noise.


We welcome contributions from anyone who uses an AI assistant and wants to improve control over assistant behavior through rules, rule sets, and prompts.

---

## 🔰 Before You Begin

- Review the [Getting Started Guide](docs/getting_started.md)
- Browse the [Glossary](docs/glossary.md)
- Read relevant authoring guides in `/docs/writing/`
- Reference contributor documentation in `/internal/docs/`

---

## 🧱 Contribution Types

| Type | Location | Key Standards |
|------|----------|----------------|
| **Rules** | `/rules/` | `rule.json`, `rule_schema.json` |
| **Rule Sets** | `/internal/rule_sets/` → compiled to `/rule_sets/` | `rule_set.json`, `rule_set_categorization.json` |
| **Prompts** | `/internal/prompts/` (internal), `/prompts/` (user-facing) | `prompt.json` |
| **Tests** | `/internal/tests/` | See `test_cases.md` (rule set/prompt only) |

---

## ✍️ Contributing a Rule

1. Add a new file in `/rules/`
2. Ensure it conforms to:
   - [`rule.json`](docs/reference/rule.json.md)
   - [`rule_schema.json`](docs/reference/rule_schema.md)
3. Run `validate_rule.json`
4. Run `optimize_rule.json`
5. Run `rule_deduplication.json`
6. If redundant, use `rule_consolidation.json` to merge overlapping rules
7. Run `is_core_rule.json` to determine placement in `core/` or elsewhere

> 📁 If the rule is core, move it into `/rules/core/`. Otherwise, leave it in the appropriate theme folder.

---

## 📦 Contributing a Rule Set

1. Create your rule set in:
   ```
   /internal/rule_sets/{category}/{name}.json
   ```
2. Ensure it conforms to `rule_set.json`
3. Use `suggest_rule_set_category.json` if you're unsure of the category
4. Validate with `validate_rule_set.json`
5. Compile with `compile_rule_set.json` — output goes to `/rule_sets/{category}/{name}.json`

> Do **not** include `"core"` in `rule_sets` — it is added automatically at compile time.

---

## 💬 Contributing a Prompt

### Internal Prompt (`/internal/prompts/`)
- Must follow `prompt.json`
- Should perform a reusable function (e.g. validation, transformation)
- Should compose existing prompts where applicable
- Must include example input/output

### User-Facing Prompt (`/prompts/`)
- Must follow `prompt.json`
- Should be general-purpose and reusable by an AI assistant users
- Should reference compiled rule sets by link or path
- Must state which standards it supports (e.g. `rule.json`, `rule_set.json`)

---

## 🧪 Tests

- Rule tests are not yet supported — skip for now
- Prompt and rule set tests live in `/internal/tests/`
- Test format is documented in [`test_cases.md`](internal/docs/validation/test_cases.md)

---

## 📤 Submitting a Pull Request

1. Fork the repo
2. Branch from `main`
3. Make your change + test it
4. Update any relevant documentation
5. Open a pull request with a clear title and description

---

Thank you for contributing to a more structured, testable, and transparent an AI assistant experience.

---

See [PROJECT_PRINCIPLES.md](PROJECT_PRINCIPLES.md) to understand the values that guide all contributions.

For writing and reviewing documentation, see our [documentation principles](internal/docs/meta/documentation_principles.md).

For detailed architecture and documentation standards, see [`internal/docs/meta/index.md`](internal/docs/meta/index.md).
