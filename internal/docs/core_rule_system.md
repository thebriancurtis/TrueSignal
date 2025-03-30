# Core Rule System: Behavior and Eligibility

This document defines the **foundation of the TrueSignal system**: its core rules. These rules are **non-optional**, **context-agnostic**, and applied to **every assistant behavior**.

---

## 🔹 What Are Core Rules?

Core rules define the baseline for:
- Instruction alignment
- Execution discipline
- Truthfulness and safety
- Behavior not tied to domain, tool, persona, or runtime

They are:
- Defined in `/internal/core/`
- Automatically included in every rule set
- Validated by `rule_schema.json`
- Compiled to `/rule_sets/core.json`

### 🚫 Restrictions

| Aspect | Value |
|--------|-------|
| Composable? | ❌ No |
| Referencable in rule_sets? | ❌ No |
| Required? | ✅ Always |
| Location | `/internal/core/` |
| Output | `/rule_sets/core.json` |

---

## ✅ Eligibility Criteria

### 1. Structural Necessity

A rule **must** be in core if its absence causes:
- Failure to execute valid instructions
- Instruction–response misalignment
- Silent ambiguity or invalid output

### 2. Context-Agnostic Universality

Core rules must apply regardless of:
- Domain, tools, runtime, output type
- User role or persona
- One-off vs. persistent interactions

### 3. Non-Derivability

A rule is **disqualified** if it can be accomplished using:
- Prompt logic
- Rule set composition
- Runtime behavior (e.g. memory)

### 4. Exclusivity

No rule may exist in both `core` and a composable rule set. If migrated, it must be:
- Removed from the rule set
- Added to `/core/`
- Reviewed via `rule_deduplication.json`

### 5. Scope

Core rules may **only govern execution**. They must **not influence**:
- Tone, style, emotionality
- Ethical judgment or safety heuristics
- Corpus-based expectations

### 6. Observability

A core rule must be:
- Behaviorally observable
- Traceable via validation
- Demonstrable with at least one test case

### 7. Reviewer Accountability

Every core rule must be:
- Justified against one or more eligibility criteria
- Audited using `rule_deduplication.json`
- Reviewed for uniqueness and operational behavior

### 8. Enumerated Behaviors Only

If a behavior is **not explicitly listed**, it is **not core**. No inference or tool behavior can expand it.

### 9. Required Test Case

Every rule must include at least one test case proving:
- Trigger conditions
- Failure modes without enforcement

### 10. Feedback Loop Constraints

Rules must not create behavioral recursion (e.g. reinforcement, verbosity, preference loops). Continuity constraints must define:
- Amplification limits
- Reset conditions

---

## 🔍 Enforcement Tools

| Tool | Purpose |
|------|---------|
| `rule_schema.json` | Structural validity |
| `rule_deduplication.json` | Redundancy checks |
| `rule_categorization.json` | Scope verification |
| Manual review | Eligibility and clarity |
