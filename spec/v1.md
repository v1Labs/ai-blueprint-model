# AIBM Specification v1 (Scaffold)

Status: Draft

## Scope

Defines repository-native conventions for markdown-first blueprint packages and evaluation-ready artifact generation.

## Normative terms

- **MUST**: required for compliance
- **SHOULD**: recommended unless justified otherwise
- **MAY**: optional

## Baseline requirements

An AIBM-compliant blueprint **MUST** define:
1. intent metadata
2. constraints expressed with normative language
3. generation structure/components
4. evaluation criteria

An AIBM-compliant blueprint **SHOULD** define:
1. operational metadata
2. workflow guidance
3. one or more examples

Evaluations **SHOULD** validate whether the blueprint's stated constraints were met.

## File conventions

- Blueprint definitions SHOULD be markdown-first.
- Files SHOULD remain human-readable in standard git diffs.
- Structured metadata MAY be represented in YAML front matter.
- Optional machine validation MAY use `/schemas` artifacts.
- Multi-file blueprint packages SHOULD store generation guidance in `constraints.md`.
- Constraints SHOULD use normative terms such as `MUST`, `SHOULD`, and `MAY`.
- Blueprint packages MAY include supporting files such as schemas, example inputs, reference outputs, templates, code, images, design assets, test data, and related documentation.

---

## Compliance levels

AIBM defines three progressive compliance levels. Teams may adopt the model incrementally, starting with AIBM-Lite and advancing toward AIBM-Operational as their workflows mature.

### AIBM-Lite

The minimum viable blueprint. Suitable for manual and early human-in-the-loop workflows.

Required sections:
- `intent` — artifact type, audience, objective, success criteria
- `constraints` — required, recommended, and optional guidance expressed with normative terms
- `evaluation criteria` — rubric for assessing output quality

AIBM-Lite blueprints are suitable for manual and lightly structured workflows. `MUST` constraints are typically enforced by human reviewers, while `SHOULD` and `MAY` guidance improves quality without over-constraining the work.

---

### AIBM-Standard

Extends AIBM-Lite with structured operational context. Suitable for repeatable human-in-the-loop and semi-automated workflows.

Adds:
- `examples` — at least one positive example and, where useful, a counter-example
- `operational guidance` — notes on inputs required, review checkpoints, and ownership
- `workflow metadata` — intended execution mode, escalation rules, approval gates
- `structured outputs` — description of the expected output shape and format

AIBM-Standard blueprints are **designed-for workflows**. They provide enough structure for teams to run repeatable processes without ambiguity about what a valid output looks like.

---

### AIBM-Operational

The full specification. Required for semi-automated and operational execution modes.

Adds:
- `machine-readable inputs` — structured input definitions consumable by automation
- `validation schemas` — JSON Schema or equivalent artifacts for automated constraint enforcement
- `evaluation outputs` — structured scoring definitions with pass/fail thresholds
- `automation compatibility` — explicit declarations of execution mode, version constraints, and pipeline integration requirements

AIBM-Operational blueprints make `MUST` constraints machine-validated, score or review `SHOULD` guidance, and gate outputs on evaluation results.
