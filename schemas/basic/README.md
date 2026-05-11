# basic schema

The `basic` schema defines the smallest useful reusable blueprint shape.

This schema is markdown-first: the schema is defined by this README and the guidance files in `files/`, not by a reusable `schema.json`.

## When to use it

Use `basic` when a blueprint needs a small, readable package with explicit inputs, outputs, and constraints, but does not need asset-specific content/style separation or reusable component libraries.

## Required files

- `README.md`
- `inputs.md`
- `outputs.md`
- `constraints.md`

## Schema package structure

```text
basic/
  README.md
  files/
    README.md
    inputs.md
    outputs.md
    constraints.md
  examples/
    README.md
```

## File relationships

- `README.md` introduces the blueprint and explains what it is for.
- `inputs.md` defines the source information the blueprint expects.
- `outputs.md` defines the artifact shape the blueprint should produce.
- `constraints.md` defines the hard and soft rules the generator must follow.

## Authoring philosophy

- optimize for human readability in git
- keep file purposes obvious at a glance
- prefer explicit markdown guidance over machine-oriented reusable schemas
- separate reusable structure from blueprint-specific intent

## Example blueprint shape

```text
my-blueprint/
  README.md
  inputs.md
  outputs.md
  constraints.md
```

The `basic` schema is intentionally minimal. It does not require:
- component libraries
- asset-specific examples
- design/rendering assets
- operational workflow files
