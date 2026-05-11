# Evaluation Guide

Evaluation systems are optional infrastructure-layer concerns that teams may build on top of blueprints.

This document describes how teams can approach evaluation without embedding evaluation logic into the core blueprint model.

---

## Where evaluation fits

| Layer | Responsibility |
|---|---|
| Blueprint | Generation contract — intent, constraints, structure, examples |
| Execution System | Runtime and infrastructure |
| Evaluation System | QA, scoring, and observability |

Blueprints define what should be generated. Evaluation systems observe whether the output meets expectations. These are separate concerns.

---

## Evaluation is optional

A blueprint does not need to include evaluation criteria to be valid.

Teams may implement evaluation however they choose — through manual review, automated checks, scoring tools, or observability pipelines. The blueprint model does not prescribe a specific approach.

---

## Common evaluation approaches

### Manual review

A human reviewer reads the output and checks it against the blueprint's constraints and intent.

Useful for:
- early-stage workflows
- one-off or low-volume generation
- artifacts where human judgment is the primary quality gate

### Review checklist

A reviewer uses the blueprint's `constraints.md` as a checklist. Each `MUST` constraint becomes a pass/fail check.

Useful for:
- repeatable human-in-the-loop workflows
- team consistency across reviewers
- structured handoff and approval gates

### Automated constraint checks

Tooling reads the blueprint's constraints and validates structural compliance programmatically.

Useful for:
- high-volume or semi-automated pipelines
- catching structural failures before human review
- gating downstream steps on constraint compliance

### Scoring and rubrics

Teams define weighted scoring criteria — separate from the blueprint — and apply them during review.

Useful for:
- operational pipelines with defined quality thresholds
- multi-dimensional quality reporting
- long-running workflows where observability matters

---

## Keeping evaluation separate

When building evaluation tooling, treat the blueprint as a read-only input. The blueprint defines the generation contract. Evaluation systems interpret and apply that contract.

Avoid:
- embedding scoring logic inside blueprint files
- requiring evaluation artifacts for a blueprint to be valid
- coupling blueprints to specific evaluation tools or frameworks

Teams are encouraged to build QA workflows, scoring systems, and observability pipelines. The goal is only to keep those concerns outside the core blueprint model so blueprints remain lightweight and portable.

---

## See also

- [Blueprint Anatomy](blueprint-anatomy.md) for core blueprint structure.
- [Execution Modes](execution-modes.md) for workflow and validation expectations by mode.
- [Specification v1](specification-v1.md) for baseline compliance requirements.
