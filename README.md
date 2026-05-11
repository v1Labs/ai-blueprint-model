# AI Blueprint Model (AIBM)

AI teams can generate impressive outputs quickly, but they often cannot run the same workflow twice with consistent quality.

In practice, prompts get copied around without context, quality standards live in someone’s head, examples drift over time, and generated artifacts become hard to review and approve consistently.

AIBM is a practical, repository-native specification for solving that problem.

It is **not** an agent framework. It is a blueprint system for designing, evaluating, versioning, and operationalizing AI-generated artifacts.

## Why blueprints?

Prompts alone are useful, but they are not enough for repeatable team workflows. A prompt library usually stores text snippets; it does not reliably package the full contract needed to produce and review a specific artifact.

A blueprint is a **portable contract package** for generating a specific AI-assisted artifact or workflow. It is markdown-first for readability, and it can include any files needed to define the contract end-to-end.

Blueprints improve:
- **Repeatability**: the same inputs and constraints can produce consistently shaped outputs
- **Reviewability**: requirements and quality criteria are explicit and inspectable in git
- **Portability**: teams can move the full contract across tools, repos, and environments
- **Iteration**: contracts, examples, and validation criteria can be versioned and improved over time

## What a blueprint is

A blueprint is a markdown-first package of instructions and constraints used to produce a target artifact reliably.

A blueprint can include:
- intent contracts
- design and structure rules
- component definitions
- examples and counter-examples
- evaluation criteria
- workflow and handoff guidance
- rendering assets and formatting policies
- schemas, templates, code, or other supporting files when needed

## What this repo provides

- A shared model and vocabulary for AI blueprint contracts
- Specification scaffolding and normative guidance in `spec/`
- Conceptual and operational docs in `docs/`
- Canonical templates and reusable components in `blueprints/`
- Realistic artifact examples in `examples/`
- Optional machine-readable helpers in `schemas/`
- Shared rendering/style assets in `assets/`

## Example use cases

- GTM one-pagers generated from product inputs
- product overview briefs with consistent narrative structure
- technical specification sheets with standardized sections
- reusable artifact workflows for human-in-the-loop review

## Repository structure

```text
/spec        # Specification scaffolding and normative guidance
/examples    # Concrete, realistic blueprint examples
/docs        # Conceptual and operational documentation
/schemas     # Optional machine-readable schemas and validation helpers
/assets      # Shared rendering/style assets used by blueprints
/blueprints  # Canonical blueprint templates and reusable components
```

## Roadmap (v1)

- [x] Repository bootstrap and structure
- [x] Blueprint anatomy documentation
- [x] Minimal example blueprint
- [x] Schema refinement and validation conventions
- [x] Versioning and compatibility guidance
- [x] Execution modes documentation
- [x] Compliance levels (AIBM-Lite, AIBM-Standard, AIBM-Operational)
- [ ] Additional domain examples

## Contributing

If you care about practical, composable AI specification systems, contributions are welcome.

Start with:
- `CONTRIBUTING.md`
- `spec/v1.md`
- `docs/blueprint-anatomy.md`
- `examples/gtm-one-pager/README.md`

## License

MIT (`LICENSE`)
