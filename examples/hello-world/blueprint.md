---
id: hello-world
version: 0.1.0
artifact_type: greeting
intent:
  audience: first-time blueprint authors
  objective: produce a short, friendly greeting for a named person
---

# Hello World Blueprint

The smallest possible valid blueprint. It takes a name as input and produces a one-sentence greeting as output.

This example is intentionally minimal. It introduces the core blueprint concepts — intent, inputs, outputs, contracts, and evaluation — without adding operational complexity.

**Concepts introduced:** blueprint structure, inputs, outputs, intent, minimal contract definition.

## Intent

Generate a warm, single-sentence greeting addressed to a specific person.

**Input:** A person's name.
**Output:** A one-sentence greeting that addresses that person by name.

## Hard Contracts

- Output MUST be a single sentence.
- Output MUST address the person by the provided name.
- Output MUST be friendly in tone.

## Soft Contracts

- Prefer warm, welcoming language.
- Avoid formal or corporate phrasing.

## Example

**Input:** `name: Alice`

**Output:** `Hello, Alice — glad you're here!`

## Evaluation

- Does the output address the person by name? (required)
- Is the output a single sentence? (required)
- Does it feel genuinely friendly? (preferred)
