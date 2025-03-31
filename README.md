# TrueSignal

**Bring clarity to assistant behavior — with structured rules and reusable prompts.**  
Write it once. Validate it forever. All signal, none of the noise.

TrueSignal lets you structure and audit assistant behavior using reusable, validated rules — defined in JSON, enforced through prompts, and applied without code.

---

## 🚀 What Is It?

TrueSignal makes your prompts more consistent, your constraints reusable, and your behavior rules auditable.

It does this by giving you:

- ✅ Atomic rules that constrain assistant behavior
- ✅ Thematic rule sets you can reference in an assistant prompt
- ✅ Validation and optimization prompts to enforce quality
- ✅ A structured, testable, and extensible format for rule-based control

---

## 📦 Example: Use a Compiled Rule Set

```text
Follow all constraints in:
https://raw.githubusercontent.com/your-org/TrueSignal/main/rule_sets/tone/professional.json
```

Or reference an uploaded archive:

```text
rule_sets/persona/investigator.json
```

Each compiled rule set is ready for use — validated, deduplicated, and includes `core`.

---

## 🧱 Project Structure

```
rules/               # Atomic rules
internal/rule_sets/  # Authorable rule sets (uncompiled)
rule_sets/           # Compiled, user-ready rule sets
prompts/             # User-facing AI assistant prompts
internal/prompts/    # Tooling prompts (validation, optimization, etc.)
internal/docs/       # Contributor docs (architecture, standards, test cases)
docs/                # User-facing docs (how to use, write, contribute)
```

---

## 📚 Start Here

- [Getting Started](docs/getting_started.md)
- [How to Use Rule Sets](docs/usage/using_rule_sets.md)
- [How to Write a Rule](docs/writing/how_to_write_a_rule.md)

---

## 👥 Contributing

We welcome contributions!

- [CONTRIBUTING.md](CONTRIBUTING.md)
- Internal system docs in: [`/internal/docs/`](internal/docs/)

---

## 📝 License

TrueSignal is licensed under the [Creative Commons Attribution 4.0 International License (CC-BY-4.0)](https://creativecommons.org/licenses/by/4.0/).
