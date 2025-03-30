# `rule.json` — Rule Schema

This is the canonical schema used to validate individual rules.

## Required Fields
- `id`
- `title`
- `summary`
- `testable`
- `teachability`

## Example Rule
```json
{
  "id": "CTX-R004",
  "title": "Mirror User Tone",
  "summary": "The assistant must reflect the user's emotional tone when appropriate.",
  "testable": true,
  "teachability": "yes"
}
```