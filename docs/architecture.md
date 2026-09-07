# Architecture

Proposed components, pending design validation:

| Component | Source directory | Intended role |
| --- | --- | --- |
| Dragon body | `cad/dragon/` | Structural shell and visual form |
| Scale sockets | `cad/scale-sockets/` | Interfaces for removable scales or inserts |
| Timemass inserts | `cad/timemass-inserts/` | Experimental insert geometry; material identity pending |
| Planter | `cad/planter/` | Planting volume and water management |

## Interfaces to define

Record socket dimensions, insertion direction, clearances, retention method, drainage paths, assembly order, and access for cleaning. Values remain TBD until coupon testing.

## Export workflow

Keep editable sources in `cad/`, trial meshes in `stl/prototypes/`, and validated meshes in `stl/production/`. Store printer-specific project files under `3mf/` only after checking the exact machine and material settings. Record source revision, units, orientation, and validation status for each export.
