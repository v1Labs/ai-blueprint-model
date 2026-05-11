# Schemas

A schema defines how a blueprint is structured.

A blueprint defines what an AI system should create.

## Schema responsibilities

Schemas in this repository define reusable blueprint structure, including:
- expected file layout
- required and optional files
- relationships between blueprint files
- markdown authoring guidance
- reusable blueprint shapes

Schemas do **not** define blueprint-specific artifact intent, examples, or evaluation outcomes.

## Available reusable schemas

- `basic/` — smallest useful markdown-first blueprint shape with modular file guidance
- `asset/` — extends `basic` with richer generation structure, including `content.md`, `style.md`, `components.md`, and example guidance
- `blueprint-metadata.schema.json` — JSON Schema for YAML front matter metadata only; this is not the primary reusable schema definition format

Each reusable schema package is defined through:
- `README.md` — schema overview, required structure, and authoring philosophy
- `files/` — modular guidance for each blueprint file
- `examples/README.md` — guidance for how blueprint-local examples should be authored

Artifact-specific schemas (for example one-pager/case-study/product-sheet schemas) are deprecated in favor of reusable structure schemas plus blueprint-specific intent files.
