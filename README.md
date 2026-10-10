# InkHand

**A CNC pen plotter that writes in my own handwriting.**

I write the alphabet by hand, turn each letter into single-line vectors, and a C++ program assembles any text, adds small natural variations so no two letters look the same, and generates G-code for the plotter.

> 🚧 **Status:** electronics bench test done (Oct 2026). Next: pen servo and mechanical design in Fusion 360.

<!-- Replace with photo F007 or a GIF of the plotter writing -->
<!-- ![InkHand](docs/img/hero.jpg) -->

## How it works

```
Machine:   Fusion 360 → FabLab (laser + 3D print) → assembly → electronics → GRBL + servo → calibration
Handwriting: template sheet ×4 → handwriting → 600 dpi scan → Inkscape centerline trace → inkhand import → glyphs
Writing:   letter.txt → inkhand write → letter.gcode → UGS → Arduino (GRBL) → paper
```

## Hardware

| Part | Choice |
|---|---|
| Controller | Arduino UNO + CNC Shield V3 |
| Drivers | 2 × DRV8825, 1/32 microstepping, 1.0 A (Vref 0.50 V) |
| Motors | 2 × NEMA 17 (17HS4401S) |
| Motion | Cartesian, moving bed in Y, GT2 belt, 20-tooth pulleys |
| Resolution | 160 steps/mm (0.006 mm per step) |
| Pen lift | Servo on Z+ (D11), powered by an LM2596 step-down at 5 V |
| Power | 12 V 5 A |

Full bill of materials: [hardware/bom.md](hardware/bom.md)

## Firmware

GRBL 1.1f with servo support (grbl-servo fork), sent from Universal G-code Sender (UGS). See [firmware/](firmware/).

## Software (planned)

C++20, Visual Studio. One executable, three commands:

```
inkhand import  data/sheets/variant1.svg 1     # sheet SVG → glyph files
inkhand write   samples/letter.txt out/letter.gcode
inkhand template out/template_sheet.svg        # printable handwriting template
```

## Repository layout

```
InkHand/
├─ InkHand.slnx      Visual Studio solution
├─ InkHand/          C++ source (app/, domain/, input/, layout/, output/, external/)
├─ data/             config, sheet layout, demo glyphs (my real glyphs stay private)
├─ samples/          example .txt files
├─ firmware/         GRBL settings and flashing notes
├─ hardware/         BOM, wiring, Fusion 360 exports (STEP, DXF, STL)
└─ docs/             lab journal, photos, README images
```

## Lab journal

Every work session is recorded by hand in a lab notebook and transcribed to [docs/journal/](docs/journal/).

## License

Code: MIT ([LICENSE](LICENSE)). Hardware files: CERN-OHL-P (to be added with the first CAD release).
