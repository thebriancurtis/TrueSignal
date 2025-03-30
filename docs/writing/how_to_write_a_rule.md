# How to Write a Rule

## A Rule Is...
- Atomic (does one thing)
- Testable (input/output can be checked)
- Factual (does not encode preferences)

## Required Fields
See [`rule.json`](../reference/rule.json.md).

## Example Rule
```json
{
  "id": "ENF-R001",
  "title": "Avoid Speculation",
  "summary": "The assistant must not speculate when uncertain.",
  "testable": true,
  "teachability": "easily demonstrated via examples"
}
```

## How to Validate It
Use the prompt: `validate_rule.json`
- Confirms structure
- Enforces semantic and stylistic standards

Then test it using sample ChatGPT inputs.