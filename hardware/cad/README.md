# CAD

Exports from the Fusion 360 model. A new export replaces the file with the same name; older versions stay in the Git history (`git log -- hardware/cad`).

| File | Date | Contents |
|---|---|---|
| [Plotter_Pen_InkHand.f3z](Plotter_Pen_InkHand.f3z) | 2026-10-17 | Fusion 360 archive (editable), with the linked NEMA 17, LM8SUU, GT2 pulley and Arduino + CNC Shield models |
| [Plotter_Pen_InkHand.step](Plotter_Pen_InkHand.step) | 2026-10-17 | Y axis: base, 4 rod supports, 2 Y rods, 4 bearing blocks, bed and writing sheet. X axis: 2 uprights, 2 X rods side by side, carriage (4 bearing blocks and a plate). 8 × LM8SUU. Electronics: Arduino UNO + CNC Shield V3 on 4 standoffs. 2 motor mounts and 2 GT2 pulleys. Not placed yet: 2 × NEMA 17 with their mounts |

Units are millimetres and the model is Y-up (the Fusion default). To edit it, open the `.f3z` in Fusion 360 with *File → Open → Open from my computer*.

The NEMA 17, LM8SUU, GT2 pulley, Arduino UNO and CNC Shield models were downloaded from GrabCAD and belong to their authors. The Arduino and the shield are most of the STEP's size (about 17 MB since 2026-10-17).

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
| Suporte_Motor / Suporte (2) | Motor mounts |
| GT2 20T5B_dz2020 | GT2 pulleys, 20 teeth, 5 mm bore |
| Arduino_CNC_Assembly | Arduino UNO + CNC Shield V3 |
| Eletrica / Suportes_eletrica | Standoffs for the Arduino |

## History

| Date | Commit | Contents |
|---|---|---|
| 2026-10-10 | 43bfe0b | First parts: base, 4 rods, 10 × LM8SUU bearings, 2 × NEMA 17 (STEP only) |
| 2026-10-11 | 3e2a26e | Y axis: 4 rod supports, 2 Y rods, 4 bearing blocks, bed (not placed yet) |
| 2026-10-12 | 1fe5347 | Holes and joints fixed, writing sheet, X axis: 2 uprights, 2 X rods side by side, carriage |
