
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
    - Removes duplicate rules after optimization.
    - Ensures the final rule set contains no redundant entries.

5. **Rule Consolidation** (`rule_consolidation.json`):
    - Consolidates rules **only if deduplication results in any changes**.
    - Ensures consistency across the final rule set.

## Workflow Sequence:
- **is_core_rule.json** -> **rule_categorization.json** -> **rule_optimization.json** -> **rule_deduplication.json** -> **rule_consolidation.json** (if deduplication finds redundancy)

### Notes:
- **`compile_rule_set.json`** is **not part of the core rule validation pipeline** and is handled separately for rule set compilation.
