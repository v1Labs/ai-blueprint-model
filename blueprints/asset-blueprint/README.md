# Asset Blueprint Example

Purpose: Demonstrate a blueprint package aligned to the `schemas/asset` reusable structure.

This example shows how an asset blueprint can separate:
- content sourcing and message grounding in `content.md`
- visual and tonal direction in `style.md`
- reusable asset patterns in `components.md`
- example guidance and scenario outputs in `examples/`

## Package walkthrough

- `inputs.md`: source facts and request context available during generation
- `outputs.md`: output shape, required variants, and completion expectations
- `constraints.md`: non-negotiable rules and quality boundaries
- `content.md`: grounding strategy and fallback behavior
- `style.md`: voice, channel, and consistency guidance
- `components.md`: optional reusable content + layout patterns
- `examples/`: blueprint-local examples showing expected quality level
- `assets/`: optional supporting references (layout, visual, and fixtures)

## Operational guidance

- Treat `constraints.md` as the primary acceptance contract.
- Use `content.md` and `style.md` together so channel variants stay consistent.
- Use `components.md` only when it improves consistency for repeated asset types.
- Keep supporting assets as references, not hidden requirements.
