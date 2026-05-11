# Blueprints

This file is a directory of external blueprint libraries, community examples, and related projects built on or compatible with the AI Blueprint Model (AIBM).

Blueprint libraries are designed to live **independently** from the model repo. This repository defines the model, structure, terminology, templates, and examples — not a canonical library of production blueprints. External teams are encouraged to host their own blueprint collections in separate repositories that reference the AIBM spec.

---

## Official examples

Illustrative examples included in this repository, organized as a learning progression:

- [`examples/hello-world/`](examples/hello-world/blueprint.md) — Smallest valid blueprint; introduces basic structure, inputs, outputs, and intent
- [`examples/structured-summary/`](examples/structured-summary/blueprint.md) — Adds output formatting, tone guidance, evaluation criteria, and example outputs
- [`examples/social-post/`](examples/social-post/blueprint.md) — Adds multiple output variants, human review workflow, and style consistency
- [`examples/simple-one-pager/`](examples/simple-one-pager/blueprint.md) — Adds layout-aware thinking, stronger contracts, and more rigorous evaluation
- [`examples/blueprint-template/blueprint.md`](examples/blueprint-template/blueprint.md) — Blank starter template for authoring new blueprints

## Advanced examples

More complex operational blueprints live externally to keep the core repository approachable. The examples below demonstrate full operational workflows and are intended for teams already familiar with the blueprint model:

- [`examples/gtm-one-pager/`](examples/gtm-one-pager/README.md) — GTM one-pager blueprint with operational workflow, human-in-the-loop review, and structured evaluation

---

## Community blueprint libraries

_Blueprint libraries maintained by community contributors, compatible with AIBM._

> No community libraries listed yet. [Open a PR](CONTRIBUTING.md) to add yours.

---

## AssetMule blueprints

_Blueprint libraries designed for use with the AssetMule platform._

> Coming soon.

---

## Experimental blueprints

_Work-in-progress or research-oriented blueprints and libraries._

> No experimental libraries listed yet.

---

## Related tools and resources

- [AIBM Specification (v1)](spec/v1.md)
- [Blueprint Anatomy](docs/blueprint-anatomy.md)
- [Execution Modes](docs/execution-modes.md)
- [Versioning Conventions](docs/versioning.md)
- [Contributing Guide](CONTRIBUTING.md)
