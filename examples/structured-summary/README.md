---
id: structured-summary
version: 0.1.0
artifact_type: summary
intent:
  audience: readers who need a quick understanding of a longer document
  objective: produce a structured, reader-friendly summary of a provided text
---

# Structured Summary Blueprint

Demonstrates how blueprints can shape output quality, formatting, and tone without becoming complex operational systems.

**Concepts introduced:** output formatting, tone and style guidance, evaluation criteria, example outputs.

## Intent

Generate a structured summary of a provided source text.

**Input:** A block of text (article, document, or excerpt).
**Output:** A formatted summary with a headline, key points, and a closing sentence.

## Hard Contracts

- Output MUST include, in order:
  1. A one-line headline summarizing the core message.
  2. 3–5 key points in bullet form (one sentence each).
  3. A single closing sentence.
- Output MUST NOT introduce facts not present in the source text.

## Soft Contracts

- Prefer neutral, informational tone.
- Prefer plain language over technical jargon.
- Order key points from most to least important.

## Example

**Input:**

> The team shipped a new API last week. It reduces integration time by 40% and supports three authentication methods. Early adopters report fewer support tickets since the rollout.

**Output:**

> **New API cuts integration time by 40%**
>
> - The team released a new API last week.
> - Integration time is reduced by 40% compared to the previous approach.
> - The API supports three authentication methods.
> - Early adopters report fewer support tickets since the rollout.
>
> The new API delivers measurable time savings and improved developer experience for early users.

## Evaluation

- **Completeness (0–2):** All required output sections present (headline, bullets, closing sentence).
- **Accuracy (0–3):** No facts introduced beyond the source text.
- **Clarity (0–3):** Key points are concise and easy to read.
- **Tone (0–2):** Neutral and appropriately plain.

Pass threshold: 8/10.
