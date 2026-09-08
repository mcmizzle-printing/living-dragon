# Bootstrap plan

Status: proposed implementation sequence. No environment has been created or prototype generated yet.

## 1. Define one prototype

The first proposed milestone is a small socket-and-insert coupon, not a complete dragon. Resolve:

- The insert product is now identified: see the [TimeMass profile](../profiles/timemass-glowing-plant-vitamin.md). Resolve its conflicting processing instructions and confirm the actual print hardware.
- What the insert does: holds seeds, supports growth medium, glows, or combines these functions.
- Approximate dragon size and scale size; how inserts are installed and removed.
- First printer, nozzle, structural filament, and desired support strategy.

Record confirmed requirements in `concept.md` and `architecture.md`. Choose a few measured clearance variants and acceptance criteria before generating the coupon. Material-dependent decisions can remain pending while tooling is set up.

## 2. Establish a reproducible build

Use a local `.venv` and declare a pinned printing-toolkit release in the project's dependency manifest. The inspected local toolkit has a `v0.2.0` tag and declares Python >=3.9; confirm the selected release includes the APIs needed by the first generator. Local main may contain unreleased additions.

Python, `f3d`, and `/Applications/BambuStudio.app` were found locally during bootstrap review. Presence does not establish runtime compatibility; verify them with the first end-to-end build.

Prefer a Python generator for the initial mechanical coupon using suitable toolkit primitives. Keep its editable source under `cad/`, make dimensions explicit in millimeters, and export to `stl/prototypes/`. Record exact generation and verification commands once implemented. Defer the full dragon's organic modeling approach until the shape is defined.

## 3. Reuse and improve printing-toolkit

Common tooling belongs in [printing-toolkit](https://github.com/mcmizzle-printing/printing-toolkit). Living Dragon owns the design and its data.

| Shared in printing-toolkit | Specific to Living Dragon |
| --- | --- |
| General geometry and mesh I/O | Dragon shape and scale arrangement |
| Reusable socket/retention primitives | Selected socket dimensions and placement |
| Mesh, support, and printer checks | Prototype acceptance criteria and results |
| Rendering and slicer integration | Camera choices, assembly, and material settings |

The reviewed toolkit exposes `ptk-check-all`, `ptk-islands`, `ptk-slicecheck`, and `ptk-render`. Supply explicit STL paths: their default `out/*.stl` location differs from this repository's layout.

Before adopting or extending checks, account for documented limits:

- `islands.py` misses curved overhangs. Add independent support/slicer review for curved parts; reusable improvements belong in the toolkit.
- Bed checks and slicer defaults are P2S-specific. H2C validation needs appropriate machine support before those checks can establish suitability.
- Rendering requires `f3d`; slicing requires Bambu Studio and suitable profiles. Record missing or failed checks, not an implied pass.

No toolkit edits or new release are required merely to establish this plan. Introduce shared changes when a concrete prototype need demonstrates the gap.

## 4. Complete one build-to-print cycle

Generate the coupon, check mesh and bed placement, inspect rendered views, and review the slice with the selected material and machine settings. Preserve the STL, relevant 3MF, source revision, and check results.

Print the coupon and record fit, removal, retention, and any applicable water-exposure observations in the numbered experiments and build log. Use the measurements to choose the interface before integrating it into a dragon body. A digital check does not substitute for physical measurements.

## Completion criteria

A fresh checkout can reproduce the coupon using declared dependencies and documented commands. The exact printer/material setup and digital checks are recorded, physical results are clearly distinguished from pending tests, and reusable tooling has not been duplicated in this repository.
