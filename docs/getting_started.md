# Getting Started with TrueSignal

**Bring clarity to assistant behavior — with structured rules and reusable prompts.**
Write it once. Validate it forever. All signal, none of the noise.


TrueSignal gives you precise control over how an AI assistant behaves using structured, validated rules grouped into named rule sets.

---

## 🔍 What Can You Do With It?

- Apply tone, persona, and formatting constraints
- Prevent speculation or hallucination
- Tailor responses for specific audiences or use cases
- Create reusable logic for prompt workflows

---

## 🧱 The System

- **Rules** are atomic behavior constraints (e.g. “Avoid speculation”)
- **Rule Sets** are themed collections of rules (e.g. “Professional Tone”)

(Advanced: internal prompts are used to validate and compile rule sets. If you're interested in contributing, see `/internal/docs/`.)

---

## ✅ How to Use Rule Sets

You can apply one or more **compiled rule sets** in a single prompt.

Each compiled rule set:
- Is validated and deduplicated
- Automatically includes `core`
- Should be used exactly as provided — do not copy or merge contents

---

## 🔗 Usage Example

In your system prompt or custom instructions, you can say:

```text
Follow all constraints in:
https://raw.githubusercontent.com/your-org/TrueSignal/main/rule_sets/tone/professional.json
```

Or, when using an uploaded archive:

```text
Use the rules defined in: rule_sets/persona/investigator.json
```

There is no need to merge or deduplicate — compiled sets are ready to go.

---

## 🛠 Next Steps

- [Use Rule Sets](usage/using_rule_sets.md)
- [Write a Rule](writing/how_to_write_a_rule.md)
- [Understand Rule Set Structure](reference/rule_set.json.md)
