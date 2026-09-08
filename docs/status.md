# Project status

Updated: 2026-09-07

## Established

- GitHub repository: `mcmizzle-printing/living-dragon` (private).
- Local checkout: `~/Printing/living-dragon`, per Kevin's location preference.
- Kevin uses both Claude and Codex. Shared instructions live in `../.context/context.md`; root `AGENTS.md` and `CLAUDE.md` are plain Markdown prompts directing each tool to read it, per Kevin's preference for a single context source and simple text entry points.
- The requested directory structure and starter documentation exist.
- Kevin prefers a large build and is leaning toward H2C for plate size; H2C is the provisional planning target.
- Kevin designates `mcmizzle-printing/printing-toolkit` as the home for common printing tooling; Living Dragon keeps project-specific design and experiment work.
- [Bootstrap plan](bootstrap.md) records the proposed first coupon and tooling integration sequence.

## Current state

This is a planning scaffold. There are no CAD models, STL/3MF designs, executable build tools, installed project dependencies, automated tests, or recorded physical experiments. Kevin's concept board is saved in `images/living-dragon-concept.png`; the license has not been selected.

The visual direction is an upright winged dragon with an arched neck, curled tail, planted base, and replaceable dorsal inserts; see [concept](concept.md). Engineering dimensions and assembly remain unresolved. PETG remains a candidate structural material. Kevin identified the TimeMass insert product; the [material profile](../profiles/timemass-glowing-plant-vitamin.md) records supplier evidence and unresolved processing questions.

## Open decisions

- Set height, wingspan, footprint, and section boundaries for the supplied pose; define the curved three-insert prototype.
- Verify the proposed H2C setup: usable envelope, installed nozzle, plate, and feed path; resolve the supplier profile inconsistencies recorded in the material profile.
- Choose plants/growth medium and define watering, drainage, and cleaning.
- Select an editable design tool and reproducible export workflow.
- Define socket/insert tolerances and measurable experiment acceptance criteria.
- Select license terms when appropriate.

## Suggested next step

Set the overall size and printing setup, then define a curved back segment with three insert sockets and measurable acceptance criteria. This is a proposed sequence, not a recorded user decision.

## Handoff practice

Update this page when project state changes. Link detailed decisions and evidence from `../build-log/`; do not duplicate a full session transcript here. Record checks actually run and distinguish pending physical tests from completed digital checks.

## Latest context update

Saved Kevin's supplied concept board unchanged, replacing the transparent placeholder. Updated the concept, architecture, bootstrap plan, and shared context with the observed pose and proposed component layout. Image captions remain concept claims, not test evidence. Verified the image copy by hash, checked relative documentation links, and passed whitespace checks. No CAD or print tests were produced. Next: establish overall dimensions and the first curved insert segment.
