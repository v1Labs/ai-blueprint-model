# Execution Modes

Blueprints are not just static documents — they are operational contracts designed to be executed in specific workflows. This document defines the intended execution modes for AI Blueprint Model (AIBM) blueprints.

Understanding execution modes helps teams:
- choose the right blueprint structure for their workflow
- set appropriate validation expectations
- calibrate the degree of AI autonomy and human involvement
- align on what constitutes a passing or failing run

---

## Modes

### Manual

The blueprint is used as a reference or checklist by a human author. AI assistance is optional and ad hoc.

| Property | Value |
|---|---|
| **Expected rigidity** | Low — the blueprint guides rather than enforces |
| **Validation expectations** | Informal; human judgment is the primary quality gate |
| **AI freedom level** | High — no structured prompts or constrained generation |
| **Human involvement** | Full authorship |
| **Ideal use cases** | Early drafts, exploratory work, low-stakes artifacts |

In manual mode, blueprints function as **soft contracts**. Hard contracts exist but are checked informally by the author rather than evaluated programmatically.

---

### Human-in-the-Loop

AI generates a draft using the blueprint's structured prompt and constraints. A human reviewer must inspect and approve before the output is accepted.

| Property | Value |
|---|---|
| **Expected rigidity** | Medium — hard contracts must be satisfied; soft contracts guide generation |
| **Validation expectations** | Structured checklist or rubric reviewed by a human |
| **AI freedom level** | Constrained by hard contracts; soft contracts allow stylistic flexibility |
| **Human involvement** | Review and approval gate before delivery |
| **Ideal use cases** | Content pipelines, regulated domains, repeatable team workflows |

Human-in-the-loop mode is the recommended default for most production blueprints. It balances AI leverage with human accountability.

---

### Semi-automated

AI generates output using the blueprint. Automated checks validate structural compliance (hard contracts). Human review is reserved for edge cases or escalations.

| Property | Value |
|---|---|
| **Expected rigidity** | High — hard contracts are machine-validated; soft contracts are scored |
| **Validation expectations** | Automated schema/rubric checks pass before human escalation is triggered |
| **AI freedom level** | Low to medium; prompt structure and evaluation criteria are enforced |
| **Human involvement** | Exception handling only; routine outputs proceed without review |
| **Ideal use cases** | High-volume artifact generation, internal tooling, documented operational flows |

Semi-automated mode requires that blueprints define machine-readable inputs, structured evaluation criteria, and clear escalation rules.

---

### Operational

Fully automated pipeline. AI generates, validates, and delivers output without human review for routine runs. Audit logs and monitoring replace the human-in-the-loop gate.

| Property | Value |
|---|---|
| **Expected rigidity** | Very high — both hard and soft contracts are enforced programmatically |
| **Validation expectations** | Automated evaluation against defined rubric; outputs are gated on pass/fail scores |
| **AI freedom level** | Minimal; prompts are deterministic and heavily constrained |
| **Human involvement** | Monitoring and incident response only |
| **Ideal use cases** | Scheduled artifact generation, API-driven workflows, mature automation systems |

Operational mode requires full blueprint specification at **AIBM-Operational** compliance level. Blueprints must define machine-readable inputs, structured output schemas, and evaluation scoring thresholds.

---

## Contract Alignment by Mode

| Mode | Hard Contracts | Soft Contracts | Evaluation |
|---|---|---|---|
| Manual | Reference only | Aspirational | Informal |
| Human-in-the-Loop | Enforced by reviewer | Recommended | Rubric-guided |
| Semi-automated | Machine-validated | Scored | Automated + escalation |
| Operational | Machine-validated, blocking | Scored, enforced | Fully automated, gated |

---

## Designed-for Workflows

Blueprints should declare their intended execution mode in operational metadata. A blueprint designed for human-in-the-loop review should not be run in fully operational mode without explicit validation that its hard contracts and evaluation criteria are sufficient for automated gating.

Teams should treat execution mode as a **blueprint design constraint** — not just an operational choice made at runtime.

### Soft contracts vs hard contracts in execution context

- **Soft contracts** are always advisory. Even in operational mode, soft contract scoring informs quality metrics but should not block delivery unless explicitly configured to do so.
- **Hard contracts** are always enforced. In operational mode, a hard contract violation must trigger an escalation or halt the pipeline.
