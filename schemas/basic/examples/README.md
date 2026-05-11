# basic schema example guidance

The `examples/` guidance for the `basic` schema explains how blueprint-local examples should be authored when a team chooses to include them.

## Purpose

- show the expected quality bar
- reduce ambiguity in artifact interpretation
- provide optional reference material for reviewers and AI systems

## Recommended conventions

- keep examples inside the blueprint package, not inside the reusable schema package
- use descriptive file names that match the output type or scenario
- keep examples focused on illustrating structure, tone, or constraint application

## Relationship to the schema

Examples are optional for `basic`, but when present they should reinforce the blueprint's `outputs.md`, `constraints.md`, and `evaluations.md` rather than introduce a separate contract.
