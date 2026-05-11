# AI Blueprint Model

This is a practical, repository-native model for building repeatable AI blueprint packages.

## Why blueprints?

Prompt-only systems are useful for one-off tasks, but they break down when teams need repeatability, reviewability, and operational handoffs.

Blueprints package intent, constraints, examples, and supporting artifacts so humans and automation systems can run the same workflow consistently.

Blueprints improve:
- **Repeatability**
- **Reviewability**
- **Portability**
- **Iteration**

## Core concepts

- A **schema** defines how a blueprint is structured.
- A **blueprint** defines what an AI system should create.

Schemas define reusable structure (`basic`, `asset`).
Blueprints define artifact intent (inputs, outputs, constraints, and examples).

Blueprints are markdown-first, but not markdown-only. A blueprint package may include reference assets such as PNG, PDF, SVG, JSON, CSV, datasets, diagrams, screenshots, fixtures, and sample outputs when they improve generation quality or output clarity.

## Repository map

```text
README.md        # Project introduction and navigation
Community.md     # Community discovery: libraries, blueprints, schemas
/docs            # Long-form guidance and model documentation
/schemas         # Reusable blueprint structure schemas
/blueprints      # Learning blueprints, schema-aligned packages, and starter packages
```

## What this repo provides

- Long-form model and implementation docs in `docs/`
- Reusable structure schemas in `schemas/`
- Self-contained blueprint packages in `blueprints/`
- Community discovery links in `Community.md`

## Canonical blueprint examples

The canonical schema-aligned references in this repository are:

- `blueprints/basic-blueprint/`
- `blueprints/asset-blueprint/`

Legacy single-document examples are in `blueprints/legacy/`.

## Getting started

1. Start with `blueprints/basic-blueprint/README.md`
2. Continue to `blueprints/asset-blueprint/README.md`
3. Read `docs/blueprint-anatomy.md`
4. Read `docs/execution-modes.md`
5. Read `docs/specification-v1.md`

## Contributing

If you care about practical, composable AI specification systems, contributions are welcome.

Start with:
- `CONTRIBUTING.md`
- `docs/blueprint-anatomy.md`
- `docs/specification-v1.md`
- `blueprints/basic-blueprint/README.md`
- `blueprints/asset-blueprint/README.md`

## License

MIT (`LICENSE`)
