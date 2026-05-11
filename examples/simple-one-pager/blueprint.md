---
id: simple-one-pager
version: 0.1.0
artifact_type: one_pager
intent:
  audience: internal teams and stakeholders who need a concise reference document
  objective: produce a focused, readable one-pager for a specific topic or initiative
---

# Simple One-Pager Blueprint

Demonstrates layout-aware generation, stronger structural contracts, supporting examples, and a more rigorous evaluation rubric — while remaining intentionally smaller than a full operational blueprint.

**Concepts introduced:** layout-aware thinking, stronger structural contracts, supporting assets and examples, more rigorous evaluation.

## Intent

Generate a concise one-pager document for an internal topic, initiative, or proposal.

**Input:** A topic description with key facts, goals, and intended audience.
**Output:** A one-pager with a defined structure, ready to share with stakeholders.

## Hard Contracts

- Output MUST follow this structure, in order:
  1. **Title** — a short, descriptive heading.
  2. **Summary** — 2–3 sentences describing the topic and its relevance.
  3. **Key Points** — 3–5 bullets with the most important details.
  4. **What's Needed** — one short paragraph on next steps or asks.
- Total length MUST be between 200 and 400 words.
- Output MUST NOT include unverifiable claims.
- All claims MUST be traceable to the provided input.

## Soft Contracts

- Prefer concise, direct writing.
- Prefer plain language suitable for a non-specialist audience.
- Use headers to guide visual scanning.

## Example Input

```
Topic: Engineering team wants to migrate CI pipeline to a new provider.
Goals: reduce build times, cut costs, improve reliability.
Audience: engineering leadership.
Key facts: current average build time is 14 minutes; new provider averages 6 minutes
in tests; estimated cost reduction is 30%.
```

## Example Output

> **CI Pipeline Migration Proposal**
>
> The engineering team is proposing a migration to a new CI provider to reduce build times, lower costs, and improve system reliability. Current build times average 14 minutes end-to-end, creating bottlenecks during active development sprints. Internal testing shows the new provider averages 6 minutes for equivalent pipelines. The migration is expected to reduce CI costs by approximately 30%, based on current usage and the new provider's pricing structure.
>
> **Key Points**
> - Current average build time is 14 minutes; the new provider averages 6 minutes in internal tests — a 57% reduction.
> - Estimated cost reduction is 30% based on current pipeline volume and provider pricing.
> - The migration can be staged across services to minimize disruption to active development.
> - Reliability improvements are expected based on the new provider's published uptime record.
> - A rollback plan will be prepared and tested before any production traffic is moved.
>
> **What's Needed**
> Engineering leadership approval to begin a phased migration starting with non-critical pipelines. The team estimates 2–3 sprints to complete the full transition. We will document progress, monitor build times and failure rates throughout, and report results after the first phase. No additional budget is required beyond existing CI spend, as the new provider's costs fall within current allocation.

## Evaluation

- **Structure (0–2):** All four required sections present and in the correct order.
- **Grounding (0–3):** Claims supported by provided inputs; no unverifiable assertions.
- **Clarity (0–3):** Writing is concise and appropriate for a non-specialist audience.
- **Completeness (0–2):** Sufficient detail for stakeholder decision-making.

Pass threshold: 8/10 with no hard contract violations.
