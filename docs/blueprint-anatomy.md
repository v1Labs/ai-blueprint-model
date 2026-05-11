# Blueprint Anatomy

A blueprint is a portable, markdown-first blueprint package for generating a specific artifact type.

Markdown remains the primary authoring and coordination layer, but blueprints may include supporting files such as schemas, example inputs, reference outputs, templates, code, images, design assets, test data, and related documentation when needed for constraint clarity.

## Core sections

### 1) Intent
Defines the outcome the artifact must achieve.

Typical fields:
- artifact type
- audience
- decision/use context
- success criteria

**Required** for all compliance levels. Without a clear intent, a blueprint cannot be assessed.

### 2) Constraints
Rules that govern what is required, recommended, or optional during generation. Constraints should use normative language so authors and AI systems can tell what is rigid versus flexible.

#### MUST
Non-negotiable requirements. Violations represent a structural failure of the blueprint's contract.

Examples:
- required sections
- required data fields
- forbidden claims without evidence
- output format constraints

Why they exist:
- enforce safety and consistency
- guarantee minimum structural quality
- support deterministic validation

#### SHOULD
Strong recommendations that improve usefulness but allow justified exceptions.

Examples:
- tone guidance
- preferred section order
- stylistic defaults
- depth targets

Why they exist:
- preserve adaptability across contexts
- improve quality without over-constraining generation
- support human judgment in review loops

#### MAY
Optional behaviors or additions that teams can include when useful.

Examples:
- extra implementation notes
- optional call to action
- supplementary formatting hints

**Required** for all compliance levels: every blueprint MUST define its constraints, and those constraints SHOULD be expressed with normative language.

### 3) Components
Reusable building blocks used across blueprints.

Examples:
- section templates
- prompt fragments
- policy snippets
- transformation rules

**Optional** at Lite. Recommended at Standard and above.

### 4) Examples
Reference outputs, example inputs, and counter-examples.

Purpose:
- reduce ambiguity
- show expected quality bar
- improve model alignment

**Required** at Standard and above. At least one positive example SHOULD be included. Counter-examples are recommended wherever common failure modes exist.

### 5) Operational metadata
Execution-facing context for workflows.

Examples:
- blueprint version
- compatible model classes
- required inputs
- review checkpoints
- ownership and change log references

**Required** at Standard and above. At the Operational level, inputs MUST be machine-readable.

### 6) Workflow guidance
Instructions for human-in-the-loop, semi-automated, or operational runs.

Examples:
- pre-generation checks
- post-generation review steps
- approval gates
- escalation rules

**Required** at Standard and above. SHOULD declare the intended execution mode explicitly.

### 7) Rendering assets
Optional style/layout assets that define final presentation.

Examples:
- markdown templates
- table formats
- tokenized visual styles
- export hints

**Optional** at all levels. Recommended when output formatting is critical to usability.

---

## Required vs optional sections by compliance level

| Section | Lite | Standard | Operational |
|---|---|---|---|
| Intent | Required | Required | Required |
| Constraints | Required | Required | Required |
| Components | Optional | Recommended | Recommended |
| Examples | Optional | Required | Required |
| Operational metadata | Optional | Required | Required (machine-readable) |
| Workflow guidance | Optional | Required | Required |
| Rendering assets | Optional | Optional | Optional |

---

## Minimal blueprint shape

A practical baseline blueprint should include:
- intent
- constraints
- componentized structure
- at least one example
- operational metadata

---

## Constraint Rigidity

The appropriate level of constraint rigidity depends on execution context and operational risk.

### Exploratory blueprints

Used in manual or early-stage workflows where the primary goal is to guide human thinking.

- MUST constraints: few, focused on essential structure only
- SHOULD constraints: broad stylistic guidance
- MAY constraints: optional additions where they help the author
- AI freedom: high — the blueprint is a scaffold, not a fence

### Assisted workflows

Used in human-in-the-loop workflows where AI generates a draft that a human reviews and approves.

- MUST constraints: clearly defined, enforced by human review
- SHOULD constraints: specific enough to guide consistent output across reviewers
- MAY constraints: used for optional enhancements that do not affect compliance
- AI freedom: medium — constrained by MUST requirements and guided by SHOULD recommendations

### Operational automation systems

Used in semi-automated or fully operational pipelines where human review is the exception, not the rule.

- MUST constraints: machine-validated, blocking on failure
- SHOULD constraints: scored automatically; thresholds configurable
- MAY constraints: used only when automation can safely ignore them
- AI freedom: minimal — prompts are deterministic, outputs are structurally constrained

Blueprints designed for operational automation **MUST** be held to a higher standard of precision. Ambiguous MUST constraints, underspecified output schemas, or missing machine-readable inputs are not acceptable at this level.

## See also

- [Execution Modes](execution-modes.md) for how anatomy choices map to workflow rigor.
- [Specification v1](specification-v1.md) for baseline compliance requirements.
- [Schemas](../schemas/README.md) for reusable package structures (`basic`, `asset`).
- [Canonical blueprints](../blueprints/README.md) for schema-aligned package examples.
