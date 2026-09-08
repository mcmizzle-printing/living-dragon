# Architecture

Proposed components, pending design validation:

| Component | Source directory | Intended role |
| --- | --- | --- |
| Dragon body | `cad/dragon/` | Structural shell and visual form |
| Scale sockets | `cad/scale-sockets/` | Interfaces for removable scales or inserts |
| Timemass inserts | `cad/timemass-inserts/` | Experimental insert geometry; see the [material profile](../profiles/timemass-glowing-plant-vitamin.md) |
| Planter | `cad/planter/` | Planting volume and water management |

## Proposed physical decomposition

Follow the [concept reference](concept.md): upright torso, arched neck/head, wings, curled tail, and rocky planted base. Evaluate separate printable sections with durable joints and removable dorsal inserts. Exact splits, dimensions, support strategy, and stability under watering loads are pending design work.

Separate the structural joints from insert retention. Include accessible drainage and cleaning paths, and account for insert changes during water exposure. Proposed first prototype: a curved back segment with three leaf-shaped insert sockets, before scaling to the full body.

## Interfaces to define

Record socket dimensions, insertion direction, clearances, retention method, drainage paths, assembly order, and access for cleaning. Values remain TBD until coupon testing.

## Export workflow

Keep editable sources in `cad/`, trial meshes in `stl/prototypes/`, and validated meshes in `stl/production/`. Store printer-specific project files under `3mf/` only after checking the exact machine and material settings. Record source revision, units, orientation, and validation status for each export.
