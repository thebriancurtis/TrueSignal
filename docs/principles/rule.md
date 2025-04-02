# Rule Principles

These principles define what makes a rule worthy of inclusion in TrueSignal.

They guide the structure and constraints enforced by [rule.json](../../standards/rule.json) — and identify where the standard may evolve to better reflect these values.

> These principles are grounded in the [TrueSignal Project Principles](../../PROJECT_PRINCIPLES.md), and inform the [Rule Set Principles](rule_set.md) and [Prompt Principles](prompt.md).

---

## 🧱 Principles

> See also: [rule_categorization.json](../../standards/rule_categorization.json) — defines the assistant behavior categories used below.

### 1. **Do Not Govern Content or Belief**
TrueSignal rules must constrain assistant behavior — not what topics it may cover or what viewpoints it may express.  
Safety is the responsibility of the assistant. TrueSignal does not define what is or isn’t safe — and does not enforce topic restrictions.

---

### 2. **Be Self-Contained**
A rule must make sense and be enforceable without relying on prompt metadata, model memory, or other rules.  
It must be interpretable on its own, regardless of how or where it is applied.

---

### 3. **Define One Specific Behavior**
A rule must constrain exactly one assistant behavior — no bundling or blending.  
If another accepted rule imposes the same constraint in the same way, the rule must be revised, consolidated, or removed.

---

### 4. **Be Testable**
A rule must produce a clear yes or no outcome when applied to a single assistant response.  
When a rule applies, its success or failure must be unambiguous.

