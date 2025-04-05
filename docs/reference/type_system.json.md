# TrueSignal Type System

This document describes all allowed `"type"` values used in TrueSignal JSON structures.

## Purpose

The `type` field is required for every structured object. It helps assistants, validators, and humans determine:

- What the object *is*
- How it should be interpreted
- Which validation rules apply

## Official Types

### `prompt`
A structured instruction for AI assistants to execute logic.
- Example: `compile_core_rule_set.json`

### `schema`
A formal definition of structure and field types.
- Example: `rule_set_schema.json`

### `specification`
A document defining required behavior, rules, or meaning.
- Example: `object_metadata.json`

## Validation

Only the types listed in `/standards/type_system.json` are valid.

This file is enforced by system validators and must be referenced by all structured TrueSignal files.
