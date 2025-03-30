# Rule Set Framework

A rule set:
- Is defined in `/internal/rule_sets/{category}/{name}.json`
- Is compiled into `/rule_sets/{category}/{name}.json`
- Conforms to `rule_set.json`
- Belongs to a category defined in `rule_set_categorization.json`

Each rule set can include:
- Rules: `rules` array
- Other rule sets: `rule_sets` array

---

## 🔒 Core Rule Set Inclusion

The compiler always adds `core` to every compiled rule set.

- **Do not include `core` manually** inside your `rule_sets` array
- Attempting to do so will result in an error
