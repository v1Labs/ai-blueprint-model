# AI Blueprint Model (AIBM)

A repository-native specification for designing, evaluating, versioning, and operationalizing AI-generated artifacts.

AIBM is not an agent framework. It is a blueprint system for structured AI outputs and workflows.

## Why this exists

Most AI output quality problems are specification problems:
- intent is underspecified
- structure is inconsistent
- quality criteria are implicit
- workflows are hard to reproduce

AIBM defines blueprints as explicit, composable contracts that make AI work:
- reproducible
- inspectable
- versionable
- operational

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
- `docs/blueprint-anatomy.md`
- `examples/gtm-one-pager/README.md`

## License

MIT (`LICENSE`)
