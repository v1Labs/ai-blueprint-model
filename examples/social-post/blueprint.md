---
id: social-post
version: 0.1.0
artifact_type: social_post
intent:
  audience: social media managers and content teams
  objective: produce platform-appropriate social post variants from a source announcement or topic
---

# Social Post Blueprint

Demonstrates multiple output variants, style consistency, and a simple human review step.

**Concepts introduced:** multiple output variants, human review workflow, style consistency, reusable examples.

## Intent

Generate two social post drafts — one for LinkedIn and one for X — based on a provided announcement or topic.

**Input:** A brief description of an announcement, launch, or update.
**Output:** Two labeled social post drafts: one LinkedIn-style and one X-style.

## Hard Contracts

- Output MUST include two clearly labeled variants:
  - `[LinkedIn]` — 3–5 sentences, professional tone.
  - `[X]` — 1–2 sentences or fragments, under 280 characters.
- Both variants MUST reflect the same core message.
- Output MUST NOT include hashtags unless explicitly requested in the input.

## Soft Contracts

- Prefer active voice.
- Prefer direct, confident language over hedging.
- LinkedIn posts may include a call to action.
- X posts should lead with the most compelling detail.

## Example

**Input:**

> We just launched a public API for our product. Developers can now build integrations without waiting for a partnership agreement.

**Output:**

> **[LinkedIn]**
> We just opened our API to the public. Developers can now build integrations with our product without a partnership agreement or waiting period. This is the first step toward a full developer platform. We're excited to see what teams build with it.
>
> **[X]**
> Our API is now public. Build integrations without a partnership agreement. Ship faster.

## Evaluation

- **Variant completeness (required):** Both `[LinkedIn]` and `[X]` variants present.
- **Character limit (required):** X variant is under 280 characters.
- **Message consistency (0–2):** Both variants reflect the same core idea.
- **Tone fit (0–2):** Each variant matches its platform's style.

Pass threshold: Both required checks pass, plus 3/4 on scored criteria.

## Workflow

1. Generate both variants from the provided input.
2. Human reviewer checks tone and message accuracy.
3. Apply any adjustments.
4. Publish.
