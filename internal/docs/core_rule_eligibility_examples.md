# Core Rule Eligibility Examples

This document provides examples of rules that do and do not qualify for inclusion in the TrueSignal `core` rule set. Each example includes rationale tied directly to the eligibility principles defined in `core_rule_eligibility_3.md`.

---

## ✅ Eligible for Core

### Example 1: Instruction Execution Requires Explicit Context
**Rule:**  
> Before executing any complex task or chain of steps, verify that all required context, assumptions, or dependencies are explicitly defined or confirmed.

**Why:**  
- Prevents silent misalignment or invalid execution (Principle 1)
- Applies in every domain and task type (Principle 2)
- Cannot be reliably delegated to prompts (Principle 3)
- Behavior can be observed (Principle 6)

---

### Example 2: No Placeholder Output After Instruction Validation
**Rule:**  
> Once input and context are confirmed, execution must begin in the same response. Do not insert transitional language or filler unless explicitly instructed.

**Why:**  
- Ensures immediate execution fidelity (Principle 1)
- Not context-specific; applies to all tasks (Principle 2)
- Observable difference in model output (Principle 6)

---

## ❌ Not Eligible for Core

### Example 3: Use Accessible Language
**Rule:**  
> Use plain, accessible language when the user has not indicated a preference for technical terminology.

**Why Not:**  
- Varies by user domain and role (Violates Principle 2)
- Affects tone, not execution behavior (Violates Principle 5)
- Can be expressed via prompt customization (Violates Principle 3)

---

### Example 4: Reflect Emotional Tone
**Rule:**  
> Mirror user tone or emotion when appropriate.

**Why Not:**  
- Relies on tone detection and style interpretation (Violates Principle 5)
- Behavior is not universally required (Violates Principle 2)
- Not observable through deterministic execution (Violates Principle 6)

---

## ⚠️ Edge Case Examples

### Example 5: Source Attribution for Facts
**Rule:**  
> All factual claims must include source attribution where feasible.

**Review Consideration:**  
- Possibly core-worthy if the system requires consistent behavioral attribution across all contexts  
- Must prove it's not tool- or domain-specific  
- Reviewer must reference Principles 1, 2, and 6 if included

---

### Example 6: Reject Instructions That Lack Executable Context
**Rule:**  
> Reject instructions that are ambiguous, contradictory, or lack actionable context.

**Review Consideration:**  
- Eligible only if observable failure occurs in absence of rule  
- Reviewer must prove behavior applies globally and cannot be achieved via prompt logic

---

# Reviewer Checklist

For any proposed core rule, confirm:
- [ ] The rule addresses a failure of execution or instruction alignment
- [ ] It is not context-specific
- [ ] It cannot be accomplished via composition or runtime behavior
- [ ] Its behavior is observable and testable
- [ ] Reviewer cites applicable eligibility principles

