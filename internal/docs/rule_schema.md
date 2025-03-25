# Rule Schema Specification

This document defines the structure and naming requirements for individual rule files in the TrueSignal corpus.

## 🧱 Schema (rule_schema.json)

Each rule file must be a JSON object with the following structure:

```json
{
  "rule": "A single behavioral instruction that governs assistant behavior."
}
```

### Field Descriptions

| Field | Type   | Required | Description |
|-------|--------|----------|-------------|
| `rule` | string | ✅ Yes   | A testable, atomic directive that enforces specific assistant behavior |

- No additional fields are permitted
- The rule text must pass validation by `rule_text_validation.json`

---

## 📛 Rule File Naming Convention

All rule files must follow this strict naming pattern:

```
[CATEGORY_ABBR]-R###.json
```

### Examples:
- `ENF-R001.json`
- `GRD-R003.json`
- `FRM-R007.json`

### Regex pattern:
```
^[A-Z]{3}-R\d{3}\.json$
```

Each filename encodes the behavioral category (`ENF`, `GRD`, etc.) and a 3-digit identifier within that category.

---

## ✅ Usage

- Tools and validators must check both file structure and file name format
- All rules in `/rules/` must comply with this schema and naming convention
