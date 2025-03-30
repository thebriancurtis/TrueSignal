# Contributing to TrueSignal

We welcome contributions to the TrueSignal rule system, tooling, and documentation.

## 📋 Ways to Contribute

- 🧠 Write or revise a rule
- 🧪 Add a test case for a rule or rule set
- 🧰 Improve documentation or onboarding
- 🧪 Propose new prompt logic or validation stages

## ✅ Rules for Rules

- Must be testable and atomic
- Must conform to [rule_schema.json](docs/rule_schema.md)
- Must pass deduplication
- Must be categorized with [rule_set_categorization.json](docs/rule_set_categorization.md)

## 📦 Submitting a Rule

1. Draft the rule in a `.json` file
2. Validate it using prompt `validate_rule.json`
3. Check for duplicates using `rule_deduplication.json`
4. Propose a category via `suggest_rule_set_category.json`

## 🧪 Submitting a Test

Include:
- Rule ID(s)
- Input prompt
- Expected behavior
- Supported models (if relevant)

## 🤝 Community Standards

- Write clearly and concretely
- Use schema validation
- Cross-reference your changes with impacted rules or prompts

