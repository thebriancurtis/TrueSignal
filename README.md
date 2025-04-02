# TrueSignal

[![License](https://img.shields.io/github/license/thebriancurtis/truesignal)](./LICENSE)
[![Docs](https://img.shields.io/badge/docs-100%25-success)](./docs)
[![Standards](https://img.shields.io/badge/standards-strict-blue)](./standards)
[![Last Commit](https://img.shields.io/github/last-commit/thebriancurtis/truesignal)](https://github.com/thebriancurtis/truesignal/commits/main)
[![Contributors](https://img.shields.io/github/contributors/thebriancurtis/truesignal)](https://github.com/thebriancurtis/truesignal/graphs/contributors)

Bring clarity to assistant behavior — with structured rules and reusable prompts. Write it once. Validate it forever. All signal, none of the noise.

TrueSignal lets you structure and audit assistant behavior using reusable, validated rules —  
defined in JSON, enforced through prompts, and applied without code.

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

## 📚 Start Here

- [Getting Started](docs/getting_started.md)
- [How to Use Rule Sets](docs/usage/using_rule_sets.md)
- [How to Write a Rule](docs/writing/how_to_write_a_rule.md)
- [How to Write a Prompt](docs/writing/how_to_write_a_prompt.md)
- [Glossary](docs/glossary.md)

---

## 📐 Standards
- [Rule Set Principles](docs/principles/rule_set.md): Why TrueSignal rule sets are structured the way they are.

- [Rule Standards](standards/README.md) — JSON schemas for defining and validating rules, prompts, and rule sets
- [TrueSignal Principles](PRINCIPLES.md)

---

## 🧱 Project Structure

```
/docs/                 # User-facing documentation
/standards/            # Public JSON schemas for rules, prompts, and rule sets
/internal/docs/        # Contributor documentation and standards
/internal/prompts/     # Prompts used for validation, optimization, categorization
/internal/rule_sets/   # Authorable rule sets (before compilation)
/rule_sets/            # Compiled, user-ready rule sets
```

---

## 👥 Contributing

We welcome both casual and core contributors.

- See the [CONTRIBUTING.md](CONTRIBUTING.md) guide for how to report issues, suggest improvements, or add rules and prompts.
- For core contributors working on internal standards, prompts, or architecture, see  
  [`internal/docs/meta/contributing.md`](internal/docs/meta/contributing.md)

