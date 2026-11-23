# Extracted Net Names

Net names below were extracted from printable strings inside `Alvi_Routing.brd`. They represent likely signal, power, and test-point nets, but the list is not exhaustive and should be verified in Cadence Allegro.

## Power and Ground

| Net | Notes |
|-----|-------|
| `+5V` | Positive 5 V supply |
| `AGND` | Analog ground |
| `DGND` | Digital ground |
| `GND1`, `GND2` | Ground references |
| `VCCK` | Core / PLL voltage rail |
| `VCC12A_PLL` | 1.2 V PLL analog rail |
| `VCC3IO_1`, `VCC3IO_2` | 3.3 V I/O rails |
| `VCC33A_ADC` | 3.3 V analog / ADC rail |

## Differential / Data Sense Pairs

| Net Group | Nets |
|-----------|------|
| DS pair 1 | `+DS1`, `-DS1` |
| DS pair 2 | `+DS2`, `-DS2` |
| DS pair 3 | `+DS3`, `-DS3` |
| DS pair 4 | `+DS4`, `-DS4` |

These appear to be four differential data/sense channels routed to the test units.

## Test Point Nets

Named test points found in the board file:

- `TP_VCCK`
- `TP_VCC3IO_1`
- `TP_VCC12A_PLL`

Numbered test points:

- `TP01`
- `TP040`

## Test Unit Channel Nets

Each `UT` block (`UT1`–`UT4`) has pins named after channel nets. The suffixes observed are:

- `PDCF`, `PDCS`, `PGDS`, `PGRD` — power / return / sense connections
- `UP5V` — +5 V test-unit rail
- `URW00`–`URW06` — read/write channels 0–6
- `UW07`–`UW15` — write channels 7–15

These are likely routed to pogo-pin or spring-contact test probes.

## Other Candidate Nets

Strings that may be net names or net labels include:

- `-2U`
- `0-5-S4`
- `0.1U-10-X-S2-MU`
- `0.1U-25-X-S6`
- `0.1U-50-X-S4-MU`

Many additional strings in the file are component package names, padstack dimensions, or library references rather than net names.

## Verification

For a complete and accurate netlist, open `Alvi_Routing.brd` in Cadence Allegro and export the netlist or PCB net report.
