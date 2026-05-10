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

### 3) Components
Reusable building blocks used across blueprints.

Examples:
- section templates
- prompt fragments
- policy snippets
- transformation rules

### 4) Examples
Reference outputs and counter-examples.

Purpose:
- reduce ambiguity
- show expected quality bar
- improve model alignment

### 5) Evaluations
Explicit rubric for scoring artifact quality.

Typical dimensions:
- structural compliance
- factual grounding
- usefulness for intended audience
- clarity and actionability

### 6) Operational metadata
Execution-facing context for workflows.

Examples:
- blueprint version
- compatible model classes
- required inputs
- review checkpoints
- ownership and change log references

### 7) Workflow guidance
Instructions for human-in-the-loop, semi-automated, or operational runs.

Examples:
- pre-generation checks
- post-generation review steps
- approval gates
- escalation rules

### 8) Rendering assets
Optional style/layout assets that define final presentation.

Examples:
- markdown templates
- table formats
- tokenized visual styles
- export hints

## Minimal blueprint shape

A practical baseline blueprint should include:
- intent
- hard contracts
- soft contracts
- componentized structure
- at least one example
- evaluation rubric
- operational metadata
