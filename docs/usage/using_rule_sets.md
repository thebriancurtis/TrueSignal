# Using Rule Sets

TrueSignal rule sets define how an AI assistant should behave in a given context.

Each compiled rule set is a `.json` file containing validated, structured rules like:

```json
{
  "rules": ["ENF-R001", "CTX-R004", "TONE-R003", ...],
  "rule_sets": []
}
```

---

## 🧠 What Does “Using a Rule Set” Mean?

You apply a rule set by referencing it inside your an AI assistant context or tooling.

Do **not** copy/paste rule summaries into your prompt.  
Instead, refer to the compiled rule set by **raw link** or **file path**.

---

## ✅ Example Usage

```text
Use the constraints defined in:
https://raw.githubusercontent.com/your-org/TrueSignal/main/rule_sets/tone/professional.json
```

Or, if you're uploading a file archive:

```text
Follow the rules in: rule_sets/persona/investigator.json
```

Each compiled set already includes `core`, so there's no need to merge or deduplicate manually.

---

## 🔁 Recompiling Custom Sets

If you want to define your own rule set:

1. Create the definition under:
   ```
   /internal/rule_sets/{category}/{name}.json
   ```

2. Run the `compile_rule_set.json` prompt (or CLI/script)

3. Output goes to:
   ```
   /rule_sets/{category}/{name}.json
   ```

---

## 📎 Related Docs

- [How to Write a Rule Set](../writing/how_to_write_a_rule_set.md)
- [rule_set.json Schema](../reference/rule_set.json.md)
- [rule_set_categorization.json](../reference/rule_set_categorization.md)
