# Rule Set Taxonomy

This document defines the canonical taxonomy for organizing rule sets in the TrueSignal framework. These axes govern assistant behavior and provide clear, composable structure for activating behavioral constraints in any context.

---

## ✅ Canonical Axes (9 Total)

Each axis controls a distinct dimension of assistant behavior. They are independently composable and semantically disjoint.

| Axis        | Governs |
|-------------|------------------|
| `domain/`   | Field of knowledge or practice (e.g., `software_engineering`, `medicine`)  
| `context/`  | Task being performed (e.g., `code_review`, `diagnosis`)  
| `constraint/` | Risk, compliance, or safety limits (e.g., `high_risk`, `enterprise_policy`)  
| `tone/`     | Output voice, formality, and phrasing style (e.g., `direct`, `explanatory`)  
| `persona/`  | Role or behavioral voice (e.g., `mentor`, `executive`, `peer_reviewer`)  
| `audience/` | Who the output is for (e.g., `beginner`, `technical_peer`, `C_suite`)  
| `tool/`     | Platform or instrument being used (e.g., `python`, `github`, `figma`)  
| `method/`   | Reasoning or problem-solving approach (e.g., `stepwise`, `analogy`)  
| `language/` | Output natural language (e.g., `english`, `japanese`)  

---

## ⚠️ Excluded Axis: `format/` (Behavioral Modifier Only)

### What it Represents
Structural preferences such as `json`, `table`, `markdown`, `bullet_points`, `APA_style`.

### Why It Is Not an Axis
- ❌ Not persistent across tasks
- ❌ Often derived from context, tool, or audience
- ❌ More often part of prompt-level instruction
- ✅ Can be expressed as a *rule* within another set, or as metadata

### Recommendation
Do not treat `format/` as a standalone axis. Support format rules inside other sets (e.g., `context/report`, `tool/markdown`).

---

## 📂 Folder Layout

Each axis has a corresponding subfolder in `/rule_sets/`:

```
/rule_sets/
  ├── domain/
  ├── context/
  ├── constraint/
  ├── tone/
  ├── persona/
  ├── audience/
  ├── tool/
  ├── method/
  └── language/
```

---

## ✅ Design Goals
- Cognitive clarity
- Behavioral separation
- Composability of intent and style
- Academic and scientific grounding
- Scalable to new tasks, tools, and personas

This taxonomy is complete and will hold under the highest scientific and practical standards for behavioral modeling.
