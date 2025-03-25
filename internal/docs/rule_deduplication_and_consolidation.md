# Rule Deduplication and Consolidation

This document explains the purpose, structure, and integration of the rule deduplication and consolidation processes within the TrueSignal framework. These processes are designed to eliminate behavioral redundancy in the rule corpus while preserving enforcement integrity and semantic clarity.

---

## Purpose

Deduplication and consolidation ensure that:
- No two rules govern the same assistant behavior using different phrasing
- Redundant or overlapping rules are resolved into a single, enforceable constraint
- The rule corpus remains minimal, non-repetitive, and semantically disjoint

These steps support clarity, scale, and long-term maintainability across rule classification, validation, and optimization.

---

## Definitions

- **Behavioral Redundancy**: Two rules are redundant if they produce the same enforcement outcome when applied to the same assistant behavior, even if their phrasing differs.
- **Surface Similarity**: Rules that sound similar but govern different behaviors are *not* redundant.
- **Consolidation**: The process of resolving identified duplication into a cleaner outcome — via merge, replacement, retention, or removal.

---

## Prompt Roles

### `rule_deduplication.json`
- Identifies whether a rule is behaviorally redundant with any existing rule(s)
- Evaluates based on semantic behavior, not phrasing
- Outputs:
  - `is_redundant` (boolean)
  - `redundant_with` (list of rule IDs or texts)
  - `rationale` (explanation of overlap)

### `rule_consolidation.json`
- Accepts a candidate rule and a set of overlapping reference rules
- Produces one of five resolution types:
  - `replacement`: use a cleaner rule to supersede all
  - `merge`: combine constraints into one
  - `keep_one`: retain the best version and discard others
  - `remove_all`: discard all rules if covered elsewhere
  - `no_action`: preserve all rules as non-redundant
- Outputs:
  - `consolidated_rule`
  - `consolidation_type`
  - `rules_retired`
  - `rationale`

---

## Workflow Integration

1. A rule is validated and optimized
2. It is passed to `rule_deduplication.json` against the current corpus
3. If flagged, it is reviewed using `rule_consolidation.json` along with reference rules
4. Based on the result:
   - A new rule may be written
   - Existing rules may be replaced or removed
   - No action may be taken if redundancy is false

---

## Examples

### Replacement
- Rule A and Rule B enforce the same behavior
- Rule B is more concise and structurally aligned
- Output: `consolidation_type = "replacement"`, `consolidated_rule = Rule B`

### Merge
- Rule A governs tone
- Rule B governs disclaimer under the same condition
- Merged into: “Use neutral tone and include disclaimers when uncertain.”

### Keep One
- Two rules say the same thing
- One is canonical or older
- Output: Keep original, retire duplicate

### Remove All
- Three rules are all covered by another, more general rule
- All are removed for redundancy

### No Action
- Two rules share vocabulary but constrain different behaviors
- Example: tone vs. structure
- Output: Preserve both

---

## Best Practices

- Run deduplication after optimization and classification
- Only consolidate rules after confirming intent and enforcement overlap
- Never merge rules that govern different behaviors, even if thematically related
- Document every consolidation decision in the audit trail
- Prefer the clearest, shortest valid rule when choosing between duplicates

---

## Summary

Rule deduplication ensures the system does not enforce the same constraint more than once. Rule consolidation turns that insight into action. Together, they maintain the behavioral integrity and enforceability of the entire TrueSignal rule corpus.
