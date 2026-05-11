# Blueprint Anatomy

A blueprint is a structured contract for generating a specific artifact type.

## Core sections

### 1) Intent
Defines the outcome the artifact must achieve.

Typical fields:
- artifact type
- audience
- decision/use context
- success criteria

**Required** for all compliance levels. Without a clear intent, a blueprint cannot be evaluated.

### 2) Contracts
Rules that govern what is allowed, required, or forbidden.

#### Hard contracts
Non-negotiable requirements. Violations should fail evaluation.

Examples:
- required sections
- required data fields
- forbidden claims without evidence
- output format constraints

Why they exist:
- enforce safety and consistency
- guarantee minimum structural quality
- support deterministic validation

**Required** for all compliance levels.

#### Soft contracts
Strong preferences that improve usefulness but allow controlled flexibility.

Examples:
- tone guidance
- preferred section order
- stylistic defaults
- depth targets

Why they exist:
- preserve adaptability across contexts
- improve quality without over-constraining generation
- support human judgment in review loops

**Required** for all compliance levels.

### 3) Components
Reusable building blocks used across blueprints.

Examples:
- section templates
- prompt fragments
- policy snippets
- transformation rules

**Optional** at AIBM-Lite. Recommended at AIBM-Standard and above.

### 4) Examples
Reference outputs and counter-examples.

Purpose:
- reduce ambiguity
- show expected quality bar
- improve model alignment

**Required** at AIBM-Standard and above. At least one positive example SHOULD be included. Counter-examples are recommended wherever common failure modes exist.

### 5) Evaluations
Explicit rubric for scoring artifact quality.

Typical dimensions:
- structural compliance
- factual grounding
- usefulness for intended audience
- clarity and actionability

**Required** for all compliance levels. At AIBM-Operational level, evaluation criteria MUST include structured pass/fail thresholds that automation can enforce.

### 6) Operational metadata
Execution-facing context for workflows.

Examples:
- blueprint version
- compatible model classes
- required inputs
- review checkpoints
- ownership and change log references

**Required** at AIBM-Standard and above. At AIBM-Operational, inputs MUST be machine-readable.

### 7) Workflow guidance
Instructions for human-in-the-loop, semi-automated, or operational runs.

Examples:
- pre-generation checks
- post-generation review steps
- approval gates
- escalation rules

**Required** at AIBM-Standard and above. SHOULD declare the intended execution mode explicitly.

### 8) Rendering assets
Optional style/layout assets that define final presentation.

Examples:
- markdown templates
- table formats
- tokenized visual styles
- export hints

**Optional** at all levels. Recommended when output formatting is critical to usability.

---

## Required vs optional sections by compliance level

| Section | AIBM-Lite | AIBM-Standard | AIBM-Operational |
|---|---|---|---|
| Intent | Required | Required | Required |
| Hard contracts | Required | Required | Required |
| Soft contracts | Required | Required | Required |
| Components | Optional | Recommended | Recommended |
| Examples | Optional | Required | Required |
| Evaluations | Required | Required | Required (structured) |
| Operational metadata | Optional | Required | Required (machine-readable) |
| Workflow guidance | Optional | Required | Required |
| Rendering assets | Optional | Optional | Optional |

---

## Minimal blueprint shape

A practical baseline blueprint should include:
- intent
- hard contracts
- soft contracts
- componentized structure
- at least one example
- evaluation rubric
- operational metadata

---

## Contract Strictness

The appropriate level of contract rigidity depends on execution context and operational risk.

### Exploratory blueprints

Used in manual or early-stage workflows where the primary goal is to guide human thinking.

- Hard contracts: few, focused on essential structure only
- Soft contracts: broad stylistic preferences
- Evaluation: informal; human judgment is the primary gate
- AI freedom: high — the blueprint is a scaffold, not a fence

### Assisted workflows

Used in human-in-the-loop workflows where AI generates a draft that a human reviews and approves.

- Hard contracts: clearly defined, enforced by human review
- Soft contracts: specific enough to guide consistent output across reviewers
- Evaluation: structured rubric with defined criteria per dimension
- AI freedom: medium — constrained by hard contracts, guided by soft contracts

### Operational automation systems

Used in semi-automated or fully operational pipelines where human review is the exception, not the rule.

- Hard contracts: machine-validated, blocking on failure
- Soft contracts: scored automatically; thresholds configurable
- Evaluation: automated, gated — outputs cannot proceed unless evaluation passes
- AI freedom: minimal — prompts are deterministic, outputs are structurally constrained

Blueprints designed for operational automation **MUST** be held to a higher standard of precision. Ambiguous hard contracts, underspecified evaluation criteria, or missing machine-readable inputs are not acceptable at this level.

