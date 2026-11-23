# Extracted Component Designators

The following designators were extracted by scanning printable strings inside `Alvi_Routing.brd`. This is **not** a verified BOM; it may include padstack names, package names, and duplicate string references. Use Altium Designer to confirm the actual placed components.

## Summary by Prefix

| Prefix | Count | Likely Function |
|--------|-------|-----------------|
| `BDB` | 8 | Board-to-board connectors |
| `C` | 30 | Capacitors (some entries are package names like `C0402`) |
| `CAP` | 1 | Capacitor bank / group |
| `CMON` | 4 | Current monitor / sense points |
| `D` | 448 | Diodes / DUT interface pads / protection |
| `DPS` | 4 | Power supply / distribution blocks |
| `F` | 171 | Fuses or fault-indicating components |
| `FB` | 1 | Ferrite bead (`FB0805` package) |
| `G` | 52 | Connector pin groups `G1`–`G4` |
| `GND` | 2 | Ground references |
| `GRD` | 4 | Guard / ground rings |
| `LDB` | 5 | Left board connector |
| `LOGO` | 2 | Silkscreen logos |
| `LRB` | 5 | Right board connector |
| `M` | 1 | Mounting hole (`M3_NPTH169`) |
| `NGH` | 4 | NRE / engineering change notes |
| `NPTH` | 1 | Non-plated through hole (`NPTH120`) |
| `NUT` | 22 | Mounting nuts / hardware |
| `P` | 72 | Connector pin groups `P1`–`P4` |
| `R` | 1 | Resistor package (`R0603`) |
| `RD` | 9 | Resistor / DUT references |
| `SB` | 3 | Shield / bracket (`SB13`–`SB15`) |
| `SITE` | 4 | Test sites (`SITE1`–`SITE4`) |
| `SO` | 1 | Stiffener / outline (`SO8_215X127MM`) |
| `SQ` | 5 | Square / keep-out / fiducial references |
| `TP` | 2 | Test points (`TP01`, `TP040`) |
| `TYPE` | 2 | Board type selectors |
| `UHC` | 2 | High-current / power blocks (`UHC230`, `UHC430`) |
| `URW` | 9 | Unit read/write channel references |
| `UT` | 81 | Test unit pin designators `UT1`–`UT4` |
| `UTL` | 4 | Test unit labels `UTL1`–`UTL4` |
| `UW` | 16 | Unit write channel references `UW00`–`UW15` |
| `VRD` | 2 | Voltage / resistor divider references |

## Detailed Lists

### Board-to-Board / Mechanical

- `BDB5`, `BDB6`, `BDB7`, `BDB8`, `BDB25`, `BDB26`, `BDB27`, `BDB28`
- `NUT1`–`NUT22`
- `LDB1`–`LDB5`
- `LRB1`–`LRB5`
- `LOGO1`, `LOGO2`
- `M3_NPTH169`
- `NPTH120`
- `SB13`, `SB14`, `SB15`

### Test Sites and Units

- `SITE1`, `SITE2`, `SITE3`, `SITE4`
- `UTL1`, `UTL2`, `UTL3`, `UTL4`

#### UT Pin Designators

Each test unit (`UT1`–`UT4`) exposes pins such as:

- `PDCF`, `PDCS`, `PGDS`, `PGRD` — power / return / sense
- `UP5V` — +5 V rail
- `URW00`–`URW06` — read/write channels 0–6
- `UW07`–`UW15` — write channels 7–15

Example extracted references:

- `UT1_PDCF`, `UT1_PDCS`, `UT1_PGDS`, `UT1_PGRD`, `UT1_UP5V`
- `UT1_URW00` through `UT1_URW06`
- `UT1_UW07` through `UT1_UW15`
- Same pattern repeated for `UT2`, `UT3`, `UT4`

### Connector Pin Groups

#### G Groups (`G1`–`G4`)

Pins `G1_1` through `G1_13`, `G2_1` through `G2_13`, etc. (52 total extracted).

#### P Groups (`P1`–`P4`)

Pins `P1_1` through `P1_18`, `P2_1` through `P2_18`, etc. (72 total extracted).

### Passives and Protection

- Capacitors: `C181`–`C218` range (30 extracted, including package names)
- Fuses: `F100`–`F270` range (171 extracted)
- Diodes / DUT pads: `D101`–`D448` range (448 extracted, many are multi-pin connector references)
- Resistors / references: `RD002`, `RD016_008P01`, `RD050`, `RD050_028`, `RD055_041`, `RD060_040`, `RD090_059`, `RD120_093`
- Ferrite bead: `FB0805`
- Voltage references: `VRD016_008P01`, `VRD024_012P01`

### Test Points

- `TP01`, `TP040`
- Named test points found in strings: `TP_VCCK`, `TP_VCC3IO_1`, `TP_VCC12A_PLL`

## Notes

- The `D` prefix count is very high because many connector pins are labeled with `D` followed by multi-digit numbers (e.g., `D10101`–`D10116`).
- Package names such as `C0402`, `C0603`, `R0603`, and `FB0805` appear in the file as padstack/footprint references, not necessarily placed components.
- Always cross-check with the Altium schematic and PCB editor.
