# Rule Text Validation Theory

This document defines the theoretical basis and structural requirements for valid rule definitions in the TrueSignal framework. These rules govern assistant behavior in a way that is observable, testable, and enforceable across both human and machine contexts.

---

## Purpose of Rule Validation

Rule validation ensures that all rules in the system are:

- Behaviorally specific
- Structurally complete
- Semantically unambiguous
- Functionally enforceable

The purpose is not to optimize or stylistically refine rules, but to determine whether they meet the minimum standard for inclusion in a behavior-governing corpus.

---

## Definition of a Valid Rule

A valid rule describes a **single, testable behavior** that the assistant must either perform or avoid. It must do so in a way that is:

- Independent of prompt design or system metadata
- Enforceable using binary outcomes (pass/fail)
- Self-contained and interpretable in isolation

Valid rules operate as precise behavioral contracts between the assistant and its operating constraints.

---

## Structural Requirements

A valid rule must follow these structural criteria:

- **Single Behavioral Intent**: The rule must govern only one behavior or output constraint.
- **Semantic Completeness**: The rule must be grammatically and logically complete.
- **Enforceable Directive**: The rule must contain a directive verb that describes what the assistant must or must not do.
- **Isolated Testability**: The rule must be interpretable without access to context, metadata, prompts, or adjacent rules.

A typical rule structure follows the pattern:

**Condition (optional) → Assistant Behavior → Constraint or Outcome**

---

## Disqualifiers

A rule is **invalid** if it meets any of the following conditions:

- Governs more than one behavior
- Uses vague, subjective language (e.g., "helpful", "natural", "appropriate")
- References metadata, prompt structures, or internal configuration
- Expresses a motivational or meta-rule (e.g., "Rules should be clear")
- Uses passive voice that obscures agency or enforcement
- Functionally duplicates the enforcement scope of another rule

A rule is **unclassifiable** if it is malformed, ambiguous, or lacks a testable behavioral constraint.

---

## Evaluation Model

Validation is performed using a fixed sequence of evaluations:

1. Check for grammatical and logical completeness
2. Ensure the rule governs a single assistant behavior
3. Confirm the presence of a directive verb
4. Test whether the behavior can be evaluated using a binary result
5. Determine if the rule duplicates existing behavioral logic in the corpus
6. If conditional, verify that it enforces a single outcome
7. Ensure the rule is free of rhetorical, illustrative, or explanatory content

Only rules that pass all checks are accepted as valid.

---

## Validation vs Optimization

Validation assesses whether a rule is enforceable. Optimization refines how well that behavior is expressed. Verbosity, passive voice, or indirect phrasing do not disqualify a rule if it is otherwise valid—but they should be corrected during optimization.

Validation ensures correctness. Optimization ensures clarity.

---

## Summary

The validation standard ensures that all rules:

- Describe exactly one assistant behavior
- Are structurally and semantically complete
- Can be enforced using binary logic
- Are free from ambiguity, redundancy, or non-directive language

This guarantees that every rule admitted into the system supports precise behavioral control and classification within a robust, scalable framework.
