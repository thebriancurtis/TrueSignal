# Core Rule Promotion Workflow

This document describes the process by which core-eligible rules, stored in the `provisional/` folder, are automatically promoted to the `core/` folder.

## Overview

The `provisional/` folder contains rules that:
- Are core-eligible (per `core_rule.json`)
- Have passed all validation and categorization
- Are awaiting promotion after a comment period

Each rule file includes:
- `text`: the rule content
- `graduation_datetime`: the datetime (ISO 8601) after which the rule is eligible for promotion

## Promotion Process

The system periodically evaluates all rules in the `provisional/` folder by running the `promote_core_rule.json` prompt.

### `promote_core_rule.json` Behavior

- Input: All rules in `provisional/` + current datetime
- Output: A list of filenames whose `graduation_datetime` has passed

### Example Output

```
{
  "promotions": [
    "ENF-R006.json",
    "VAL-R002.json"
  ]
}
```

## Execution

For each rule listed in the `promotions` array:
- The file is moved from `provisional/` to `core/`
- The contents are not changed
- The rule is now considered a finalized core rule

## No Manual Review Required

Core promotion is **automatic** based on time.
- There is no revalidation or reapproval
- If a rule should not be promoted, it must be **removed from `provisional/`** before the `graduation_datetime`

## Related Standards

- `core_rule.json`
- `rule_filename.json`
- `promote_core_rule.json`