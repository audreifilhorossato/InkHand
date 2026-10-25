# CAD

Exports from the Fusion 360 model. A new export replaces the file with the same name; older versions stay in the Git history (`git log -- hardware/cad`).

| File | Date | Contents |
|---|---|---|
| [Plotter_Pen_InkHand.f3z](Plotter_Pen_InkHand.f3z) | 2026-10-24 | Fusion 360 archive (editable, design version 38), with the linked NEMA 17, LM8SUU, GT2 pulley and idler, Arduino + CNC Shield, LM2596 and MG90S models, and the CNC setup for the base |
| [Plotter_Pen_InkHand.step](Plotter_Pen_InkHand.step) | 2026-10-24 | Y axis: base, 4 rod supports, 2 Y rods, 4 bearing blocks, bed and writing sheet, Y motor in its mount with a GT2 pulley, idler support with a GT2 idler. X axis: 1 upright (the second one is being redone), 2 X rods side by side, carriage (4 bearing blocks and a plate). 8 × LM8SUU. Electronics: Arduino UNO + CNC Shield V3 and LM2596 on 6 standoffs. Not placed yet: the X motor with its pulley, its new mount and the MG90S servo |

Units are millimetres and the model is Y-up (the Fusion default). To edit it, open the `.f3z` in Fusion 360 with *File → Open → Open from my computer*.

The `.f3z` also holds the CNC setup for the base, in the Manufacture workspace: a 600 × 600 × 15 mm MDF sheet, a Ø3.5 mm drill and a Ø4 mm flat end mill, and the Mach3 post processor. Details in the [2026-10-23 journal entry](../../docs/journal/2026-10-23.md#machining-the-base-on-the-cnc).

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
| Suportes_Altos | Gantry uprights |
| Mesa_superior | X carriage plate |
| Suporte_Motor / Suporte (2) | Y motor mount |
| Suporte_Motor / Suporte (2) (1) | X motor mount (not fitted yet) |
| GT2 20T5B_dz2020 | GT2 pulleys, 20 teeth, 5 mm bore |
| Arduino_CNC_Assembly | Arduino UNO + CNC Shield V3 |
| LM2596_5V | LM2596 step-down module |
| Assembly Micro Servo MG90S | Pen lift servo |
| Eletrica / Suportes_eletrica | Standoffs for the Arduino and the LM2596 |
| Suporte_Roldana / Parte1, Parte1(Mirror) (2) | Idler support (Y axis), the two halves of the fork |
| GT2_20T_kladka_dz | GT2 idler, 20 teeth, 5 mm bore |

## History

| Date | Commit | Contents |
|---|---|---|
| 2026-10-10 | 43bfe0b | First parts: base, 4 rods, 10 × LM8SUU bearings, 2 × NEMA 17 (STEP only) |
| 2026-10-11 | 3e2a26e | Y axis: 4 rod supports, 2 Y rods, 4 bearing blocks, bed (not placed yet) |
| 2026-10-12 | 1fe5347 | Holes and joints fixed, writing sheet, X axis: 2 uprights, 2 X rods side by side, carriage |
| 2026-10-17 | b1fb3a7 | Rod holes Ø8.0, 3 mm counterbores, 2 motor mounts, GT2 pulleys, Arduino UNO + CNC Shield V3 on 4 standoffs |
| 2026-10-20 | b98b5eb | 3.3 mm counterbores, LM2596 and MG90S, Y motor placed with a reinforced mount, lighter rod supports and upright |
