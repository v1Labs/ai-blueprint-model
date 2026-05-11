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

A blueprint is a portable contract package for generating a specific AI-assisted artifact or workflow. It is markdown-first for readability, but it may include supporting files needed to define the contract end-to-end.

A blueprint can include:
- intent contracts
- design and structure rules
- component definitions
- example inputs, example outputs, and counter-examples
- evaluation criteria
- workflow and handoff guidance
- rendering assets and formatting policies
- schemas, templates, code, images, design assets, test data, or other supporting files when needed

## What this repo provides

- A shared model and vocabulary for AI blueprint contracts
- Normative model specification in `spec/`
- Explanatory documentation and guidance in `docs/`
- Starter blueprint structures in `templates/` (see `examples/blueprint-template/` in this repo)
- Illustrative examples in `examples/` (not a canonical production blueprint library)
- Optional machine-readable helpers in `schemas/`
- Shared rendering/style assets in `assets/`

## Example use cases

- simple greetings and structured summaries
- social post variants with style consistency
- internal one-pagers and stakeholder documents
- GTM one-pagers generated from product inputs
- reusable artifact workflows for human-in-the-loop review

## Repository map

```text
/spec         # Normative model specification
/docs         # Explanatory documentation and guidance
/templates    # Starter blueprint structures (starter template currently in /examples/blueprint-template/)
/examples     # Illustrative examples only, not canonical production blueprint libraries
/Blueprints.md # Directory/index of external blueprint libraries and examples
/schemas      # Optional machine-readable schemas and validation helpers
/assets       # Shared rendering/style assets used by blueprints
```

## Roadmap (v1)

- [x] Repository bootstrap and structure
- [x] Blueprint anatomy documentation
- [x] Minimal example blueprint
- [x] Schema refinement and validation conventions
- [x] Versioning and compatibility guidance
- [x] Execution modes documentation
- [x] Compliance levels (AIBM-Lite, AIBM-Standard, AIBM-Operational)
- [x] Progressive minimal examples (hello-world → structured-summary → social-post → simple-one-pager)
- [ ] Additional domain examples

## Examples

The `examples/` directory contains a progression of minimal examples, each introducing a small number of new blueprint concepts:

1. [`examples/hello-world/`](examples/hello-world/blueprint.md) — The smallest valid blueprint.
2. [`examples/structured-summary/`](examples/structured-summary/blueprint.md) — Adds output formatting, tone guidance, and evaluation.
3. [`examples/social-post/`](examples/social-post/blueprint.md) — Adds multiple output variants and a human review step.
4. [`examples/simple-one-pager/`](examples/simple-one-pager/blueprint.md) — Adds stronger contracts and more rigorous evaluation.

Start with `hello-world` if you are new to blueprints. Advanced and operational blueprint examples are listed in [`Blueprints.md`](Blueprints.md).

## Blueprint libraries

External blueprint libraries built on AIBM are listed in [`Blueprints.md`](Blueprints.md), which serves as a directory/index of libraries and examples outside this repo. Blueprint libraries are encouraged to live in separate repositories that reference the AIBM spec.

## Contributing

If you care about practical, composable AI specification systems, contributions are welcome.

Start with:
- `CONTRIBUTING.md`
- `spec/v1.md`
- `docs/blueprint-anatomy.md`
- `examples/hello-world/blueprint.md`

## License

MIT (`LICENSE`)
