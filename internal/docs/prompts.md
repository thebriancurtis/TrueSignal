
# TrueSignal Prompts

TrueSignal uses a series of prompts to validate, categorize, optimize, and deduplicate rules. Each prompt is modular and focuses on a specific responsibility.

## Prompts:

1. **`is_core_rule.json`**:
    - Checks if a rule is eligible to be a core rule.
    - Must be run **first** in the workflow.

2. **`rule_categorization.json`**:
    - Categorizes the rule based on its type after core eligibility is determined.
    - Categories could include optimization, safety, or other rule types.

3. **`rule_optimization.json`**:
    - Optimizes rules based on their category and type.
    - Runs **after categorization**.

4. **`rule_deduplication.json`**:
    - Removes duplicate rules after optimization.
    - Ensures the final rule set contains no redundant entries.

Each prompt is designed to follow a clear, modular sequence, ensuring maintainability and flexibility in future rule handling.
