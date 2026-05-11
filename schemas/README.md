# Schemas

A schema defines how a blueprint is structured.

A blueprint defines what an AI system should create.

## Schema responsibilities

Schemas in this repository define reusable blueprint structure, including:
- expected file layout
- required and optional files
- allowed markdown sections
- metadata structure for machine-readable validation
- reusable blueprint shapes

Schemas do **not** define blueprint-specific artifact intent, examples, or evaluation outcomes.

## Available reusable schemas

- `basic/` — smallest useful blueprint shape (`README.md`, `inputs.md`, `outputs.md`, `constraints.md`, optional `evaluations.md`)
- `asset/` — extends `basic` with richer generation structure (`components.md`, `examples/`, `evaluations.md`)
- `blueprint-metadata.schema.json` — JSON Schema for YAML front matter metadata only

Artifact-specific schemas (for example one-pager/case-study/product-sheet schemas) are deprecated in favor of reusable structure schemas plus blueprint-specific intent files.
