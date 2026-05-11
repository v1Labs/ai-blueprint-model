# asset schema

The `asset` schema extends `basic` for richer artifact-generation blueprints.

This schema is markdown-first: the schema is defined by this README and the guidance files in `files/`, not by a reusable `schema.json`.

## When to use it

Use `asset` when a blueprint needs a clearer separation between:
- what content should be communicated
- how the artifact should look and feel

This schema is a good fit for presentations, social assets, one-pagers, product sheets, and other artifact-generation workflows that need examples, reusable components, and separate content/style authoring guidance.

## Required files

- `README.md`
- `inputs.md`
- `outputs.md`
- `constraints.md`
- `content.md`
- `style.md`
- `components.md`

## Required directories

- `examples/`

## Schema package structure

```text
asset/
  README.md
  files/
    README.md
    inputs.md
    outputs.md
    constraints.md
    content.md
    style.md
    components.md
  examples/
    README.md
```

## File relationships

- `README.md` explains the blueprint's purpose and how the package fits together.
- `inputs.md` defines what source information is available at generation time.
- `outputs.md` defines the artifact shape and deliverables.
- `constraints.md` defines the rules that govern acceptable output.
- `content.md` explains how content should be sourced, grounded, and generated when information is missing.
- `style.md` explains the visual, tonal, and brand direction for the artifact.
- `components.md` defines reusable building blocks that connect content and style into repeatable patterns.
- `examples/` contains blueprint-local examples; this schema package's own `examples/README.md` documents how those examples should be organized.

## Authoring philosophy

- separate content direction from visual/style direction
- keep schema guidance modular and easy to scan
- make file responsibilities self-documenting
- preserve portability across blueprint repositories and workflows

## Example blueprint shape

```text
my-asset-blueprint/
  README.md
  inputs.md
  outputs.md
  constraints.md
  content.md
  style.md
  components.md
  examples/
    README.md
    example-1.md
```

## Scope

Use `asset` when the blueprint needs reusable components, concrete examples, and separate content/style authoring guidance.
