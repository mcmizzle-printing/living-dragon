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

The dragon planter with removable scale inserts is a working interpretation of the supplied folder layout, not a finalized design specification. PETG remains a candidate structural material. Kevin identified the TimeMass insert product; the [material profile](../profiles/timemass-glowing-plant-vitamin.md) records supplier evidence and unresolved processing questions.

## Open decisions

- Confirm the physical concept, size, pose, scale function, and first prototype scope.
- Confirm the first printer and actual hardware; resolve the supplier profile inconsistencies recorded in the material profile.
- Choose plants/growth medium and define watering, drainage, and cleaning.
- Select an editable design tool and reproducible export workflow.
- Define socket/insert tolerances and measurable experiment acceptance criteria.
- Replace the image placeholder and select license terms when appropriate.

## Suggested next step

Confirm the concept and printing setup, then define one socket-and-insert test coupon with dimensions and acceptance criteria before designing the complete dragon. This is a proposed sequence, not a recorded user decision.

## Handoff practice

Update this page when project state changes. Link detailed decisions and evidence from `../build-log/`; do not duplicate a full session transcript here. Record checks actually run and distinguish pending physical tests from completed digital checks.

## Latest context update

Identified the insert product from Kevin's supplied link. Reviewed the supplier product page and manual, updated the material profile, and removed obsolete identity questions from the shared context and design documents. Product claims remain distinct from measurements. Relative links and whitespace checks passed; no print tests were run. Next: choose the first printer and confirm its nozzle, plate, and feed path before creating a material preset.
