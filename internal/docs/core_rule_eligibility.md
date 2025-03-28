# Core Rule Eligibility (Generated from JSON)

## 1. Structural Necessity

A rule must be included in `core` only if its absence would produce at least one of the following effects:

- Failure to execute a valid instruction
- Misalignment between instruction and response
- Silent behavioral ambiguity
- Invalid output despite validated context

Rules must not exist in `core` solely to improve convenience or frequency of use. Only functionally necessary rules may be included.

Each rule must specify:
- A clear, explicit triggering condition
- At least one test case showing the behavior activated or broken by the absence of the rule

---

## 2. Context-Agnostic Universality

A rule must apply across all:

- Domains and subject areas
- Tool and runtime configurations
- Output types and task modes
- User roles, intents, or personas
- System scales (from one-off queries to persistent sessions)

Rules that vary by any contextual, runtime, or configuration factor must be excluded.

---

## 3. Non-Derivability

A rule must be excluded from `core` if its behavior can be accomplished using:

- Prompt logic
- Rule set composition
- User-defined instruction constraints
- Runtime-dependent behavior (memory, functions, browsing, tools)

Rules that vary in behavior based on toolchain, implementation layer, or system integration state are disqualified.

---

## 4. Migration-Driven Uniqueness

Rules may not exist in both `core` and any composable rule set.

If a composable rule is found to meet all `core` criteria, it must be:

- Removed from the rule set
- Migrated to `/core/`
- Validated using `rule_deduplication.json`, schema enforcement, and reviewer review

All `core` rules must be semantically unique.

---

## 5. Behavioral Enforcement Scope

Core rules must strictly define **execution behavior** — how the assistant interprets, aligns with, and carries out validated instructions. They must not affect:

- Tone or politeness
- Style, pacing, or formatting
- Emotional mirroring or audience sensitivity
- Content classification, ethics, safety, or risk heuristics

Rules must not introduce tone modulation, hedging, disclaimers, or moral framing — even implicitly.

Rules must never model, infer, or anticipate user beliefs, cultural values, or implicit norms. Behavior must arise only from **explicitly validated context**.

Rules must not be derived from or reference learned corpus behavior, usage frequency, or model output history.

---

## 6. Observability Requirement

Each core rule must be auditable through one or more of the following:

- Observable behavior when applied
- Traceable state change or validation check
- Measurable failure mode if omitted

Each rule must:
- Be associated with at least one test case showing its application or necessity
- Admit only one valid behavioral interpretation, enforceable by tools and reviewers

---

## 7. Reviewer Accountability

During authoring, optimization, or migration, reviewers must:

- Justify every rule’s inclusion by referencing one or more specific eligibility criteria
- Validate that no disallowed dimensions are present
- Confirm the rule describes operational behavior, not aspirational logic
- Use `rule_deduplication.json` and schema enforcement to ensure uniqueness
- Reject rules based on corpus behavior, legacy expectations, or inferred precedent

---

## 8. Enumerated Behaviors

Only behaviors explicitly defined in this document or its future extensions may be included in `core`.

No rule or system process may expand `core` functionality through implication, inference, tool behavior, or corpus generalization.

If a behavior is not defined, it does not exist in `core`.

The absence of a behavior must not be interpreted as permission. Composability or augmentation must occur explicitly through rule sets.

---

## 9. Test Case Requirement (Applies to All Rules)

All rules in the project — whether in `core` or a composable rule set — must include at least one test case. A test case must demonstrate:

- The triggering conditions for the rule
- How failure to enforce the rule would result in degraded output, misalignment, or invalid behavior

More than one test case is strongly encouraged, particularly for rules:
- With multiple edge cases
- That affect iterative chains or memory
- With nonlinear or stateful dependencies

---

## 10. Feedback Constraint

Rules must avoid creating behavioral loops that amplify verbosity, hedging, preference reinforcement, or recursive dependency.

Any rule that influences continuity, memory, or persistent response behavior must define:
- Bounds on amplification
- Decay logic or termination conditions
- How response shaping adapts to prompt guidance or resets cleanly

This prevents self-reinforcing instruction drift and long-tail behavior pollution over time.

---

# Enforcement Tools and Workflow

The following systems must be used:

- ✅ `rule_deduplication.json` — semantic overlap detection
- ✅ `rule_categorization.json` — domain alignment and scoping
- ✅ `rule_schema.json` — field presence and enforcement
- ✅ Manual review — including test case and interpretation validation
