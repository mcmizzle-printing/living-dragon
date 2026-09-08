# Living Dragon — shared agent instructions

## Start here

Read `README.md`, `docs/status.md`, and the documents relevant to the task before editing. Check `git status --short --branch` and recent commits; preserve work from the user or another agent. These instructions live in `.context/context.md`. Root `AGENTS.md` and `CLAUDE.md` are short Markdown instructions directing each tool to read this single file. All project paths below are relative to the repository root unless explicitly stated otherwise.

## Project and location

- Repository: `mcmizzle-printing/living-dragon` on GitHub.
- Kevin keeps local printing projects under `~/Printing`; this checkout belongs at `~/Printing/living-dragon`. Do not create another canonical copy under Documents/Codex.
- Visual direction: Kevin supplied `docs/images/living-dragon-concept.png`, showing an upright winged dragon with an arched neck, curled tail, planted rocky base, and replaceable leaf-shaped dorsal inserts. Read `docs/concept.md` for design intent and unresolved engineering decisions.
- Kevin prefers a large build and is leaning toward the H2C for plate size. Use H2C as the provisional planning target; ownership, installed nozzle, usable print envelope, and feed setup remain unverified. Do not infer that the whole dragon must fit on one plate.
- The repository is currently documentation and placeholders. Never describe planned parts, tests, printer settings, or material properties as validated results.
- PETG is a candidate structural material. The insert product is Timeplast TimeMass Glowing Plant Vitamin, identified by Kevin. Read `profiles/timemass-glowing-plant-vitamin.md` for supplier sources, conflicting instructions, and pending validation.

## Where work belongs

- `docs/`: design intent, architecture, material evidence, safety review, and current status.
- `cad/`: editable source designs, including geometry-generation code if that approach is selected.
- `stl/prototypes/`: trial mesh exports; `stl/production/`: parts with documented validation.
- `3mf/bambu-p2s/` and `3mf/bambu-h2c/`: machine-specific projects, once settings are verified.
- `experiments/`: numbered protocols, measurements, and results.
- `profiles/`: exact material products and recorded process settings.
- `build-log/`: dated decisions and build/test evidence.
- `work/`: ignored scratch files. Keep durable evidence in the appropriate tracked directory.

## Design and validation

Use millimeters for new geometry and explicitly document units, axes, orientation, and parameter meanings. Preserve editable sources alongside exports. Record source revision, tool/version, generation command or export procedure, and applicable material/printer settings.

Before promoting a part to production, document mesh integrity, dimensions, orientation, support/overhang review, slicer review, and applicable physical fit or exposure tests. A successful export or slice does not establish physical performance. Distinguish digital checks from physical tests, and report checks that could not be run.

There is no build system, dependency manifest, or automated test suite yet. For documentation changes, check links, factual consistency, and `git diff --check`. Add runnable build and validation instructions when introducing executable geometry; do not invent commands for tooling that is not present.

## Shared tooling boundary

Kevin designates `mcmizzle-printing/printing-toolkit` as the home for common printing tooling. Its local checkout is `~/Printing/printing-toolkit`; its remote is https://github.com/mcmizzle-printing/printing-toolkit.

Reuse its existing geometry, mesh I/O, validation, rendering, and slicing tools before writing equivalents. Reusable new primitives, validators, printer support, and general utilities belong in printing-toolkit. Keep dragon geometry, project parameters, assembly logic, experiment protocols, and measurements in Living Dragon. Thin project-specific command wrappers may live here; do not copy toolkit internals into this repository.

Before changing printing-toolkit, read that repository's own instructions and inspect its working tree. Validate shared changes there, follow its versioning policy, and update Living Dragon's dependency pin after the needed release exists. Do not change unrelated consumers as part of a Living Dragon task.

Inspect the selected toolkit version's documentation and limitations before relying on its checks. The locally reviewed version documents a curved-overhang blind spot in `islands.py` and P2S-specific bed/slicer assumptions; a clean result does not validate curved dragon features or H2C settings. It is not yet an installed dependency here. Use a pinned release for reproducible project setup; an editable sibling install is only for deliberate toolkit development. See `docs/bootstrap.md` for the proposed first milestone.

## Working across Claude and Codex

Keep shared rules in `.context/context.md`; keep root `AGENTS.md` and `CLAUDE.md` as plain Markdown prompts directing each tool here. Edit shared context in this file and avoid duplicating it in the entry points. Put changing project state in `docs/status.md`, and detailed evidence or decisions in dated build-log entries. Do not rely on a chat transcript or one tool's private memory for project-critical facts.

After meaningful work, update status with what changed, validation performed, remaining uncertainties, and the next concrete step. Keep untested proposals clearly labeled. Record user decisions separately from agent assumptions.

If both tools work concurrently, use separate branches/worktrees under `~/Printing` and coordinate ownership of files. Do not overwrite another session's edits. Before committing, review the diff and stage only the task's files. Follow the user's requested commit/push scope, preserve repository visibility, and never force-push as a routine step.

The license is undecided. The concept PNG is Kevin's supplied visual reference; its captions and growth timeline are not validated performance evidence. Do not silently choose a license or turn image annotations into established engineering facts.
