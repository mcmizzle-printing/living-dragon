# Project status

Updated: 2026-09-07

## Established

- GitHub repository: `mcmizzle-printing/living-dragon` (private).
- Local checkout: `~/Printing/living-dragon`, per Kevin's location preference.
- Kevin uses both Claude and Codex. Shared instructions live in `../.context/context.md`; root `AGENTS.md` and `CLAUDE.md` are plain Markdown prompts directing each tool to read it, per Kevin's preference for a single context source and simple text entry points.
- The requested directory structure and starter documentation exist.
- Kevin designates `mcmizzle-printing/printing-toolkit` as the home for common printing tooling; Living Dragon keeps project-specific design and experiment work.
- [Bootstrap plan](bootstrap.md) records the proposed first coupon and tooling integration sequence.

## Current state

This is a planning scaffold. There are no CAD models, STL/3MF designs, executable build tools, installed project dependencies, automated tests, or recorded physical experiments. The concept image is a transparent placeholder and the license has not been selected.

The dragon planter with removable scale inserts is a working interpretation of the supplied folder layout, not a finalized design specification. PETG and Timemass are candidate material labels, not approved specifications.

## Open decisions

- Confirm the physical concept, size, pose, scale function, and first prototype scope.
- Identify the exact Timemass product and supplier documentation.
- Choose plants/growth medium and define watering, drainage, and cleaning.
- Select an editable design tool and reproducible export workflow.
- Define socket/insert tolerances and measurable experiment acceptance criteria.
- Replace the image placeholder and select license terms when appropriate.

## Suggested next step

Resolve the concept and material identity, then define one socket-and-insert test coupon with dimensions and acceptance criteria before designing the complete dragon. This is a proposed sequence, not a recorded user decision.

## Handoff practice

Update this page when project state changes. Link detailed decisions and evidence from `../build-log/`; do not duplicate a full session transcript here. Record checks actually run and distinguish pending physical tests from completed digital checks.

## Latest context update

Recorded the shared-tooling boundary in `.context/context.md` and added `bootstrap.md`. Reviewed the local toolkit README, dependency manifest, tag list, and relevant command definitions. Found Python, f3d, and Bambu Studio locally; no runtime or print validation has been performed. Documentation links and whitespace checks passed. Next: identify the insert material and define the first coupon while establishing reproducible tooling.
