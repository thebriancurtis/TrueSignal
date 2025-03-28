
# TrueSignal Workflow

The TrueSignal rule validation pipeline follows a modular workflow to ensure rules are validated, categorized, optimized, and deduplicated efficiently.

## Workflow Steps:

1. **Core Eligibility Check** (`is_core_rule.json`):
    - Determines whether a rule is eligible to be part of the core rule set or is composable.
    - This step is executed **first**.

2. **Rule Categorization** (`rule_categorization.json`):
    - Categorizes the rule after the core eligibility is determined.
    - Ensures that rules are placed in appropriate categories (e.g., optimization, safety).

3. **Rule Optimization** (`rule_optimization.json`):
    - Optimizes the rule after categorization.
    - Applies specific optimizations based on rule type and category.

4. **Rule Deduplication** (`rule_deduplication.json`):
    - Performs deduplication to ensure that redundant rules are removed after optimization.

## Workflow Sequence:
- **is_core_rule.json** -> **rule_categorization.json** -> **rule_optimization.json** -> **rule_deduplication.json**

This workflow ensures that each rule is handled in a modular and clear sequence, improving maintainability and flexibility.
