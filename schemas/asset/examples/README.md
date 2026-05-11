# asset schema example guidance

This directory documents how examples should be used in blueprints that follow the `asset` schema.

## Purpose

Examples should help authors, reviewers, and AI systems understand:
- the intended fidelity of the asset
- how constraints apply in practice
- how content and style guidance come together in a finished artifact

## Recommended formats

- markdown files for lightweight examples and reviewable diffs
- one file per example scenario or channel variant
- optional companion notes when the reason for inclusion is not obvious

## Naming conventions

- use descriptive names tied to the scenario, channel, or variant
- avoid generic file names such as `example1.md`

## Fidelity guidance

- examples should illustrate the quality bar, not become hidden requirements
- counter-examples are useful when common failure modes are likely

## Relationship between examples and constraints

Examples should reinforce `constraints.md`, `content.md`, and `style.md`.

Actual examples belong in individual blueprint packages. This schema package only documents how those examples should be authored.
