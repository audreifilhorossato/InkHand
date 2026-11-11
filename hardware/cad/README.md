# CAD

Exports from the Fusion 360 model. A new export replaces the file with the same name; older versions stay in the Git history (`git log -- hardware/cad`).

| File | Date | Contents |
|---|---|---|
| [Plotter_Pen_InkHand.f3z](Plotter_Pen_InkHand.f3z) | 2026-11-10 | Fusion 360 archive (editable, design version 55), with the linked NEMA 17, LM8SUU, GT2 pulley and idler, Arduino + CNC Shield, LM2596 and MG90S models, and the CNC setups for the base and the bed |
| [Plotter_Pen_InkHand.step](Plotter_Pen_InkHand.step) | 2026-11-10 | Y axis: base, 4 rod supports, 2 Y rods, 4 bearing blocks, bed and writing sheet (both with R5 corners), Y motor in its mount with a GT2 pulley, idler support with a GT2 idler, belt support under the bed with its 2 clamp plates. X axis: 2 uprights (one with the X motor plate, one with the X idler fork), the X motor with a GT2 pulley, 2 X rods side by side, carriage (4 bearing blocks and a plate) with the X belt clamp. 8 × LM8SUU. Electronics: Arduino UNO + CNC Shield V3 and LM2596 on 6 standoffs, fan box over the shield. Not placed yet: the X idler, the fan and the MG90S servo. `Suporte_Roldana (1)` is empty. The bed and the X carriage are at one end of their travel |
| [writing-sheet.dxf](writing-sheet.dxf) | 2026-11-10 | Laser file of the writing sheet, exported from Fusion as `mesamovel.dxf`: 250 × 350 mm outline with R5 corners and 4 × Ø3.4 holes 20 mm from the edges, in millimetres. Cut in 3 mm acrylic ([journal](../../docs/journal/2026-11-10.md#the-writing-sheet)) |

Units are millimetres and the model is Y-up (the Fusion default). To edit it, open the `.f3z` in Fusion 360 with *File → Open → Open from my computer*.

The `.f3z` also holds the CNC setup for the base, in the Manufacture workspace: a 600 × 600 × 15 mm MDF sheet, a Ø3.5 mm drill and a Ø4 mm flat end mill, and the Mach3 post processor. Details in the [2026-10-23 journal entry](../../docs/journal/2026-10-23.md#machining-the-base-on-the-cnc).

Since 2026-11-05 it also holds the CNC setup for the bed (6 mm MDF, a Ø3.5 mm drill and a Ø3 mm flat end mill, Mach3 post, origin on a corner of the bed, work offset G54). Details in the [2026-11-06 journal entry](../../docs/journal/2026-11-06.md#machining-the-bed-on-the-cnc). Fusion marks these toolpaths as out of date in this export, because the model changed after them: generate them again before cutting another bed.

The NEMA 17, LM8SUU, GT2 pulley and idler, Arduino UNO, CNC Shield, LM2596 and MG90S models were downloaded from GrabCAD and belong to their authors. They are most of the STEP's size (about 17 MB on 2026-10-17, about 36 MB since 2026-10-20 with the LM2596 and the servo).

## Component names

The components have Portuguese names:

| Component | Part |
|---|---|
| Base | Base |
| Suportes / Suporte | Rod supports (Y axis) |
| Hastes / Haste | Rods |
| Rolamentos | LM8SUU bearings |
| Carrinhos / Carrinho | Bed bearing blocks (Parte Alta = upper half, Parte Baixa = lower half) |
| Carrinhos / CarrinhoAlto | X carriage bearing blocks |
| Mesa_Movel | Bed |
| Base_escrita | Writing sheet |
| Suporte_alto_mptpr | Gantry upright with the X motor plate |
| Suporte_alto_mptpr(Mirror) | Gantry upright with the X idler fork |
| Mesa_superior | X carriage plate |
| Suporte_Motor / Suporte (2) | Y motor mount |
| GT2 20T5B_dz2020 | GT2 pulleys, 20 teeth, 5 mm bore |
| Arduino_CNC_Assembly | Arduino UNO + CNC Shield V3 |
| LM2596_5V | LM2596 step-down module |
| Assembly Micro Servo MG90S | Pen lift servo |
| Eletrica / Suportes_eletrica | Standoffs for the Arduino and the LM2596 |
| Suporte Fan / FAN1 | Fan box over the CNC Shield (since 2026-11-10; before, a one-piece fan support) |
| Suporte Fan / FAN2 | Bracket of the fan box, on the Arduino |
| Suporte_correia | Belt support under the bed: holds both ends of the Y belt |
| Encaixe | The 2 clamp plates that press the ends of the Y belt against the belt support |
| suportecorreiasuperior / Suportebaixo, Suportebaixo(Mirror) | X belt clamp on the carriage plate: the 2 lower blocks |
| suportecorreiasuperior / PRESILHA, PRESILHA(Mirror) | X belt clamp: the 2 clamp plates on top of the blocks |
| Suporte_Roldana / Parte1, Parte1(Mirror) (2) | Idler support (Y axis), the two halves of the fork |
| Suporte_Roldana (1) | Copy of the idler support, empty |
| GT2_20T_kladka_dz | GT2 idler, 20 teeth, 5 mm bore |

## History

| Date | Commit | Contents |
|---|---|---|
| 2026-10-10 | 43bfe0b | First parts: base, 4 rods, 10 × LM8SUU bearings, 2 × NEMA 17 (STEP only) |
| 2026-10-11 | 3e2a26e | Y axis: 4 rod supports, 2 Y rods, 4 bearing blocks, bed (not placed yet) |
| 2026-10-12 | 1fe5347 | Holes and joints fixed, writing sheet, X axis: 2 uprights, 2 X rods side by side, carriage |
| 2026-10-17 | b1fb3a7 | Rod holes Ø8.0, 3 mm counterbores, 2 motor mounts, GT2 pulleys, Arduino UNO + CNC Shield V3 on 4 standoffs |
| 2026-10-20 | b98b5eb | 3.3 mm counterbores, LM2596 and MG90S, Y motor placed with a reinforced mount, lighter rod supports and upright |
| 2026-10-24 | 5d40c58 | Idler support (fork) with a GT2 idler and its holes in the base, X motor mount started, CNC setup for the base |
| 2026-10-28 | 6502bf6 | Uprights redrawn: one with the X motor plate, one with the X idler fork. Fan support, shorter Arduino standoff |
| 2026-11-06 | 3de4aa3 | Belt support under the bed with its 4 holes in the bed, Y belt clamp plates, bed with R5 corners, fan support v2 and v3, CNC setup for the bed |
