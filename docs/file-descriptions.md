# File Descriptions

## `Alvi_Routing.brd`

- **Type:** Altium Designer PCB board file (binary)
- **Size:** ~6.85 MB
- **Description:** Contains the routed printed circuit board layout, including footprints, tracks, vias, nets, and design rules. This is the primary design file in the repository.
- **Software required:** Altium Designer (or Altium 365 Viewer / CircuitMaker for read-only viewing).
- **Notes:** The file is binary and cannot be meaningfully diffed in Git. Generated documentation in `docs/` was produced by extracting printable strings from this file.

## `pcb-layout.jpg`

- **Type:** JPEG image
- **Size:** ~275 KB
- **Description:** Rendered visual of the PCB layout, likely a screenshot or export from Altium Designer showing the board routing, component placement, and silkscreen.
- **Purpose:** Provides a quick visual reference for the board without opening Altium Designer.

## `README.md`

- **Type:** Markdown
- **Description:** Repository overview, file list, and instructions for opening the design.

## `docs/design-overview.md`

- **Type:** Markdown
- **Description:** High-level summary of the design type, layer stackup, functional blocks, and observed power nets.

## `docs/components.md`

- **Type:** Markdown
- **Description:** Component designators extracted from the board file, grouped by prefix with counts and examples.

## `docs/nets.md`

- **Type:** Markdown
- **Description:** Net names extracted from the board file, including power rails, differential pairs, and test-point nets.

## `docs/file-descriptions.md`

- **Type:** Markdown
- **Description:** This file — detailed descriptions of every file in the repository.
