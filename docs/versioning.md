# Blueprint Versioning

Blueprints are operational specifications. Like APIs and schemas, they evolve over time — and that evolution must be managed carefully to avoid breaking downstream workflows.

This document defines semantic versioning conventions for AIBM blueprints.

---

## Why versioning matters

Blueprints are used by teams, tools, and automated pipelines. A change that seems minor (updating required inputs, reordering `MUST` constraints, tightening evaluation criteria) can break existing implementations or invalidate previously approved outputs.

Treating blueprints as versioned specifications ensures:
- teams know when a blueprint change is safe to adopt automatically
- automation pipelines can gate on compatible versions
- downstream consumers are not silently broken by upstream changes
- the history of a blueprint's operational assumptions is traceable

---

## Versioning scheme

AIBM blueprints use [Semantic Versioning](https://semver.org/) in the form `MAJOR.MINOR.PATCH`.

```
1.3.2
│ │ └─ patch: non-breaking refinement
│ └─── minor: additive, backward-compatible improvement
└───── major: breaking change
```

---

## Patch releases

**Patch** changes are safe to adopt without review of downstream workflows.

Examples:
- wording improvements to section descriptions
- example refinements that do not change pass/fail criteria
- clarification of existing guidance without changing intent
- formatting or typographic corrections
- documentation-only changes that do not affect behavior

A patch release **MUST NOT**:
- change required inputs
- change `MUST` constraints
- alter evaluation criteria in ways that affect scoring
- modify output structure expectations

---

## Minor releases

**Minor** changes add capability without breaking existing compliant workflows.

Examples:
- additive optional fields in operational metadata
- new `SHOULD` recommendations
- additional examples (positive or counter)
- expanded workflow guidance for new execution modes
- compatible improvements to evaluation criteria (additive dimensions only)
- new optional components or rendering assets

A minor release **MUST NOT**:
- change or remove existing required inputs
- alter existing `MUST` constraints
- change expected output structure in breaking ways
- invalidate outputs that were previously compliant

---

## Major releases

**Major** changes indicate breaking operational assumptions. Consumers must review and update their implementations.

Examples:
- changed required inputs (new fields required, existing fields removed or renamed)
- changed output structure expectations
- changed constraints (tightened, loosened, or restructured)
- changed evaluation criteria in ways that affect pass/fail outcomes
- breaking changes to operational metadata structure
- removal of components, sections, or workflow guidance that downstream systems depend on

When releasing a major version:
- document the breaking changes explicitly in a changelog or release notes
- provide a migration guide where possible
- do not assume consumers will automatically adopt the new version

---

## Version declaration in blueprints

Blueprint files SHOULD declare their version in YAML front matter:

```yaml
---
id: gtm-one-pager
version: 1.2.0
artifact_type: gtm-document
---
```

Consumers and automation pipelines SHOULD reference the specific version they depend on, not a range, unless the pipeline is explicitly designed to handle version compatibility.

---

## Compatibility expectations

| Change type | Patch | Minor | Major |
|---|---|---|---|
| Wording and clarification | ✓ | | |
| Additive optional fields | | ✓ | |
| New examples | | ✓ | |
| New `SHOULD` recommendations | | ✓ | |
| Changed `MUST` constraints | | | ✓ |
| Changed required inputs | | | ✓ |
| Changed output structure | | | ✓ |
| Changed evaluation pass/fail criteria | | | ✓ |

---

## Pre-release and experimental blueprints

Blueprints with versions below `1.0.0` (e.g., `0.1.0`, `0.3.2`) are considered experimental. During the `0.x.y` range, breaking changes SHOULD increment the minor version (e.g., `0.1.0` → `0.2.0`) to signal incompatibility. Patch increments in pre-release blueprints are reserved for non-breaking refinements, consistent with the Patch guidelines above.

Once a blueprint reaches `1.0.0`, full semantic versioning applies with the Major/Minor/Patch rules defined above.

Teams SHOULD NOT depend on pre-release blueprints in operational or semi-automated execution modes without explicit acknowledgment of instability.
