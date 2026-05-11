# Schemas

Machine-readable schema artifacts for optional validation workflows.

This repository remains markdown-first; schemas are support tools, not the source of truth.

- `blueprint-metadata.schema.json`: JSON Schema for blueprint YAML front matter fields (id, version, artifact_type, intent). This schema validates blueprint **metadata only** — it does not validate blueprint behavior, outputs, evaluations, or operational workflows.

---

## Scope of current schemas

The current schema covers blueprint front matter / metadata. It intentionally does not attempt to validate:
- the content or structure of blueprint sections
- generation behavior or AI outputs
- evaluation results or scoring
- operational workflow execution

---

## Future schema categories

As the ABM tooling ecosystem matures, additional schema categories are planned:

### Input schemas
Machine-readable definitions of the structured inputs a blueprint requires before generation can begin. Used by automation pipelines to validate that required context is present.

### Evaluation schemas
Structured definitions of evaluation rubrics, scoring dimensions, and pass/fail thresholds. Enables automated evaluation pipelines to score outputs consistently.

### Output schemas
Structural definitions of the expected artifact output. Used to validate that generated outputs conform to the blueprint's structural requirements before delivery.

