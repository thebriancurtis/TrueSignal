# Object Metadata Specification

This document describes the metadata specification that all JSON objects in TrueSignal must comply with.

## Required Fields

Each JSON object **must begin** with the following fields, in this exact order:

1. `description`
2. `justification`
3. `type`
4. `constraints`
5. `conventions`
6. `examples`

### All fields must be:
- Present
- Non-empty
- Defined at the top of the object before any functional content

## Enforcement

This metadata specification is enforced by the `validate_object_metadata.json` prompt.

## Use Cases

- Required in all standards, prompts, and rule definitions
- Enforced in both manual and automated reviews
