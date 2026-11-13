# Bill of materials

Fill in supplier and price as you go.

| Qty | Part | Notes | Supplier | Price (BRL) |
|---|---|---|---|---|
| 1 | Arduino UNO | | | |
| 1 | CNC Shield V3 | | | |
| 4 | DRV8825 stepper driver + heatsink | 2 in use, 2 spare. 1/32 microstepping, Vref 0.50 V | | |
| 2 | NEMA 17 stepper, 17HS4401S | 1.7 A/phase | | |
| 1 | Power supply 12 V 5 A | about 2.5 A in use: motors, Arduino and servo, fan ([2026-10-27](../docs/journal/2026-10-27.md#the-fan)) | | |
| 1 | DC barrel jack (P4) to screw terminal adapter | 12 V to the shield, the LM2596 and the fan. Fixed on the base on 2026-10-27, terminal covered with hot glue | | |
| 1 | Fan 40 mm, 12 V 0.04 A (Botto Brasil, sleeve bearing) | from the lab. Blows on the 2 drivers, sticker side towards the board, on the 12 V input. On a printed support over the shield ([2026-10-27](../docs/journal/2026-10-27.md#the-fan)). The support broke twice and its third version is glued with super glue for now ([2026-11-06](../docs/journal/2026-11-06.md#the-fan-support-broke-again)). Replaced by a printed box in 2 parts on 2026-11-10, with the fan inside, held by double-sided tape on its side. About 1 mm under the bed ([2026-11-10](../docs/journal/2026-11-10.md#fan-box)). The printed box was too stiff to snap onto the shield, so on 2026-11-12 one of its legs became a separate part, screwed to the box ([journal](../docs/journal/2026-11-12.md#fan-box-with-a-screwed-leg)) | | |
| 1 | LM2596 adjustable step-down module | set to 5 V for the servo. Arrived 2026-10-12, tested 2026-10-17. On 2 printed standoffs next to the Arduino. Header pins replaced by wires to the 12 V input on 2026-10-27 | | |
| 1 | Servo Tower Pro MG90S (metal gear) | pen lift, 180°. Arrived 2026-10-12, tested 2026-10-17 | | |
| 2 | GT2 pulley, 20 teeth, 6 mm belt | 5 mm bore, fits the motor shaft | | |
| 2 | GT2 idler, 20 teeth, with bearings | 5 mm bore in the model. Each turns on an M5 axle between the 2 tabs of a printed fork: Y on its own support ([2026-10-22](../docs/journal/2026-10-22.md)), X on top of the idler upright ([2026-10-26](../docs/journal/2026-10-26.md)) | | |
| 2 | M5 × 25 screw, M5 nut and washer | idler axles | | |
| – | GT2 belt tensioner springs | already have them. Y: on one end of the belt, next to the clamp under the bed, since 2026-11-06. X: one next to the clamp on the carriage, to fit | | |
| – | GT2 belt, 6 mm | Y: about 780 mm around the pulleys, plus the ends in the clamp ([2026-10-23](../docs/journal/2026-10-23.md#the-model-today)). X: about 880 mm, plus the ends in the clamp ([2026-10-26](../docs/journal/2026-10-26.md#the-model-on-this-day)). Y fitted on 2026-11-06, both ends clamped under the bed ([journal](../docs/journal/2026-11-06.md)). X: its clamp on the carriage plate drawn on 2026-11-10 and sent to print ([journal](../docs/journal/2026-11-10.md#x-belt-clamp)) | | |
| 4 | Steel rod Ø8 × 400 mm | 2 for the bed (Y), 2 for the gantry (X) | | |
| 10 | Linear bearing LM8SUU (short LM8UU, Ø8 × Ø15 × 16 mm) | 2 per rod: 4 on the bed, 4 on the X carriage, 2 spare (they could go on the pen carriage, one per Z rod) | | |
| 1 | MDF 15 mm (base) | 600 × 600 mm sheet. The 500 × 500 mm base was machined from it on a CNC router on 2026-10-23 | | |
| – | MDF 6 mm | bed 350 × 250 × 6 mm, R5 corners, cut on the CNC router on 2026-11-06 ([journal](../docs/journal/2026-11-06.md#machining-the-bed-on-the-cnc)). X carriage plate 144 × 70 × 6 mm, holes and counterbores fixed on 2026-11-10 ([journal](../docs/journal/2026-11-10.md#x-carriage-plate)) and 4 counterbores removed on 2026-11-12, still to make (probably 3D printed instead) | | |
| 1 | M3 screw kit (screws and nuts) | 74 screws and 66 nuts so far: M3 × 8 (8), × 12 (12), × 14 (8), × 20 (24), × 25 (22). The counterbores are 3.3 mm deep since 2026-10-19, so socket heads fit under a plate or the base. Lists in the journal: [2026-10-12](../docs/journal/2026-10-12.md#screws), [2026-10-13 to 17](../docs/journal/2026-10-13_to_2026-10-17.md#screws-for-the-new-parts), [2026-10-20](../docs/journal/2026-10-20.md#screws-for-the-new-parts), [2026-10-23](../docs/journal/2026-10-23.md#screws-for-the-new-parts), [2026-11-06](../docs/journal/2026-11-06.md#screws-for-the-new-parts), [2026-11-10](../docs/journal/2026-11-10.md#screws-for-the-new-parts) and [2026-11-12](../docs/journal/2026-11-12.md#screws-for-the-new-parts). Bought 2026-10-11 | | |
| – | Hot glue | over solder joints and screw terminals | | |
| – | Super glue | the broken fan support (v3), until the fan box replaces it | | |
| – | Double-sided tape | holds the fan in its box, on the side of the fan (2026-11-10) | | |
| – | PLA filament | printed parts, on a Bambu Lab X1 Carbon, on a P2S for the fan supports and the belt clamp, and on an A1 mini for the parts of 2026-11-10 (4 walls, 20% infill). Settings in the [2026-10-20 entry](../docs/journal/2026-10-20.md#print-settings) and the [2026-11-10 entry](../docs/journal/2026-11-10.md#the-print-of-the-evening) | | |
| 1 | Writing sheet, 3 mm acrylic | 350 × 250 × 3 mm, R5 corners, on top of the bed, 4 screws near the corners. Cut on the laser cutter on 2026-11-10 ([journal](../docs/journal/2026-11-10.md#the-writing-sheet), file [writing-sheet.dxf](cad/writing-sheet.dxf)) | | |
| – | Pen lift: steel rods and small linear bearings | 2 vertical rods and the linear bearings of the pen carriage. Chosen on 2026-11-10 ([journal](../docs/journal/2026-11-10.md#pen-lift-z-the-plan)). Rods: 2 × Ø8 × 45 mm, to cut from steel rod, in the Z support drawn on 2026-11-12 ([journal](../docs/journal/2026-11-12.md#pen-lift-z-support)). Bearings not chosen yet | | |
