# Examples

Blueprint examples organized as a learning progression.

## Schema-aligned package examples

These examples follow the reusable schema model directly:

| Example | Schema | Purpose |
|---|---|---|
| [`basic-blueprint/`](basic-blueprint/README.md) | `basic` | Smallest useful multi-file blueprint package |
| [`asset-blueprint/`](asset-blueprint/README.md) | `asset` | Richer package with components, examples, and evaluations |

## Learning progression (single-file blueprints)

These legacy single-file examples remain for quick learning and concept walkthroughs:

| Example | Suggested schema level | New concepts introduced |
|---|---|---|
| [`hello-world/`](hello-world/blueprint.md) | `basic` | Blueprint structure, inputs, outputs, intent, minimal contracts |
| [`structured-summary/`](structured-summary/blueprint.md) | `basic` | Output formatting, tone guidance, evaluation criteria, example outputs |
| [`social-post/`](social-post/blueprint.md) | `asset` | Multiple output variants, human review workflow, style consistency |
| [`simple-one-pager/`](simple-one-pager/blueprint.md) | `asset` | Layout-aware thinking, stronger contracts, supporting examples, rigorous evaluation |

Start with `hello-world` if you are new to blueprints. Each subsequent example builds on the previous one.

## Starter template

- [`blueprint-template/blueprint.md`](blueprint-template/blueprint.md) — Blank starter template for authoring new blueprints.

## Advanced examples

More complex operational blueprints (such as full GTM one-pager workflows with human-in-the-loop review and multi-step pipeline orchestration) are maintained as external blueprint libraries and linked from [`Blueprints.md`](../Blueprints.md).
