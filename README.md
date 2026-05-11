# AI Blueprint Model

AIBM is a practical, repository-native model for creating repeatable AI blueprint packages.

## Why blueprints?

Prompts alone are useful, but they do not reliably package the constraints, examples, and review criteria needed for repeatable team workflows.

Blueprints improve:
- **Repeatability**
- **Reviewability**
- **Portability**
- **Iteration**

## Core concepts

- A **schema** defines how a blueprint is structured.
- A **blueprint** defines what an AI system should create.

Schemas define reusable structure (`basic`, `asset`).
Blueprints define artifact intent (inputs, outputs, constraints, examples, and evaluations).

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

## Getting started

1. Read `docs/specification-v1.md`
2. Read `docs/blueprint-anatomy.md`
3. Start with `blueprints/hello-world/README.md`
4. Explore reusable schema-aligned packages in `blueprints/basic-blueprint/` and `blueprints/asset-blueprint/`

## Contributing

If you care about practical, composable AI specification systems, contributions are welcome.

Start with:
- `CONTRIBUTING.md`
- `docs/specification-v1.md`
- `docs/blueprint-anatomy.md`
- `blueprints/hello-world/README.md`

## License

MIT (`LICENSE`)
