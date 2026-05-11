# Execution Modes

Blueprints are not just static documents — they are markdown-first blueprint packages designed to be executed in specific workflows. This document defines the intended execution modes for AI Blueprint Model blueprints.

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

In manual mode, constraints guide the work informally. `MUST` constraints are checked by the author, while `SHOULD` and `MAY` guidance remains advisory.

---

### Human-in-the-Loop

AI generates a draft using the blueprint's structured prompt and constraints. A human reviewer must inspect and approve before the output is accepted.

| Property | Value |
|---|---|
| **Expected rigidity** | Medium — `MUST` constraints must be satisfied; `SHOULD` guidance shapes generation |
| **Validation expectations** | Structured checklist or rubric reviewed by a human |
| **AI freedom level** | Constrained by `MUST` constraints; `SHOULD` guidance allows stylistic flexibility |
| **Human involvement** | Review and approval gate before delivery |
| **Ideal use cases** | Content pipelines, regulated domains, repeatable team workflows |

Human-in-the-loop mode is the recommended default for most production blueprints. It balances AI leverage with human accountability.

---

### Semi-automated

AI generates output using the blueprint. Automated checks validate structural compliance (`MUST` constraints). Human review is reserved for edge cases or escalations.

| Property | Value |
|---|---|
| **Expected rigidity** | High — `MUST` constraints are machine-validated; `SHOULD` constraints are scored |
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
| **Expected rigidity** | Very high — `MUST` constraints and evaluation thresholds are enforced programmatically |
| **Validation expectations** | Automated evaluation against defined rubric; outputs are gated on pass/fail scores |
| **AI freedom level** | Minimal; prompts are deterministic and heavily constrained |
| **Human involvement** | Monitoring and incident response only |
| **Ideal use cases** | Scheduled artifact generation, API-driven workflows, mature automation systems |

Operational mode requires full blueprint specification at the **Operational** compliance level. Blueprints must define machine-readable inputs, structured output schemas, and evaluation scoring thresholds.

---

## Constraint Alignment by Mode

| Mode | `MUST` Constraints | `SHOULD` Constraints | `MAY` Guidance | Evaluation |
|---|---|---|---|---|
| Manual | Checked informally | Advisory | Optional | Informal |
| Human-in-the-Loop | Enforced by reviewer | Recommended | Optional | Rubric-guided |
| Semi-automated | Machine-validated | Scored | Allowed when safely ignorable | Automated + escalation |
| Operational | Machine-validated, blocking | Scored or policy-enforced | Rare; only when explicitly permitted | Fully automated, gated |

---

## Designed-for Workflows

Blueprints should declare their intended execution mode in operational metadata. A blueprint designed for human-in-the-loop review should not be run in fully operational mode without explicit validation that its `MUST` constraints and evaluation criteria are sufficient for automated gating.

Teams should treat execution mode as a **blueprint design constraint** — not just an operational choice made at runtime.

### Normative constraints in execution context

- **`MUST`** constraints are always enforced. In operational mode, a `MUST` violation must trigger an escalation or halt the pipeline.
- **`SHOULD`** constraints are recommended by default. In operational modes, they may be scored or policy-enforced when teams define that behavior explicitly.
- **`MAY`** guidance is optional. It should never be treated as a compliance failure unless a blueprint promotes it to `SHOULD` or `MUST`.
