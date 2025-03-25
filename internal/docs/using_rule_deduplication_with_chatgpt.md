# Using rule_deduplication.json with ChatGPT

This guide explains how to use the `rule_deduplication.json` prompt within the ChatGPT environment to identify redundant behavioral rules. It is written for contributors, maintainers, and curators working with the TrueSignal rule corpus.

---

## Purpose

`rule_deduplication.json` is a prompt specification designed to identify whether a proposed rule is behaviorally redundant with any other rule in a given reference set.

A rule is redundant if it governs the same assistant behavior as another rule, even if it uses different wording.

---

## Key Limitations in ChatGPT

While the prompt is structurally sound and functionally rigorous, the ChatGPT environment has constraints:

- ChatGPT cannot automatically access the entire rule corpus
- ChatGPT cannot internally compare all rules in a batch
- You must explicitly provide the rule(s) you want checked and their reference set
- There is no persistent memory across comparisons

---

## Best Practices for Using the Prompt in ChatGPT

To use the prompt effectively:

### 1. Use One Candidate at a Time
Always evaluate one `candidate_rule` against a `reference_rules` list.

### 2. Be Explicit
Copy and paste the rule text directly. Do not reference file names unless you're loading them in the same message.

### 3. Use the Full Prompt Structure

#### Example Prompt:

```
Use the rule_deduplication.json logic.

Candidate Rule:
"Use plain, accessible language and avoid obscure terminology unless the user requests technical phrasing."

Reference Rules:
1. "Avoid obscure or domain-specific phrasing unless required by the user’s context or request."
2. "Use plain, accessible language when the user has not indicated a preference for technical terminology."

Does the candidate rule duplicate the behavior of any of the reference rules?

Respond with:
- is_redundant (true/false)
- redundant_with (list of references)
- rationale (behavioral reasoning only)
```

### 4. Use Superprompts for Small Batches

If you're comparing multiple rules to each other, you can paste them all in and ask ChatGPT to:
- Treat each as a candidate in turn
- Compare it to the others
- Report redundancy findings in structured form

### 5. Use Scripts for Corpus-Wide Deduplication

For full-corpus checks, use an external script with:
- Sentence-transformers or other embedding models
- The logic of the prompt applied pairwise
- A CSV or JSON output format

---

## When to Use This Prompt

- Before adding a new rule to the corpus
- After merging or rewriting rules
- During periodic review of a category folder
- When prompted by `rule_optimization.json` to check for existing overlap

---

## Summary

You can use `rule_deduplication.json` effectively in ChatGPT as long as you provide the full context explicitly. This prompt cannot infer or search — but it can reason accurately when the candidate and references are provided.

Use it to maintain a clean, non-redundant rule corpus that preserves TrueSignal’s behavioral precision and classification integrity.



---

## You Can Ask ChatGPT to Build the Prompt for You

If you're unsure how to use the `rule_deduplication.json` prompt correctly, you can ask ChatGPT to construct a “superprompt” for you. This is especially helpful when you have a batch of rules and want to identify duplicates across them.

The superprompt will:
- Embed the full list of rules you provide
- Apply the deduplication logic rule-by-rule
- Output results in a structured format with behavioral reasoning

**Example request to ChatGPT:**

> “Can you generate a superprompt that applies rule_deduplication.json to all rules in internal/rules and identifies any behavioral duplicates?”

This allows you to delegate the construction of complex prompts without needing to write them yourself.
