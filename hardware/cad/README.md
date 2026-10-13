# CAD

Exports from the Fusion 360 model. A new export replaces the file with the same name; older versions stay in the Git history (`git log -- hardware/cad`).

| File | Date | Contents |
|---|---|---|
| [Plotter_Pen_InkHand.f3z](Plotter_Pen_InkHand.f3z) | 2026-10-12 | Fusion 360 archive (editable), with the linked NEMA 17 and LM8SUU models |
| [Plotter_Pen_InkHand.step](Plotter_Pen_InkHand.step) | 2026-10-12 | Y axis: base, 4 rod supports, 2 Y rods, 4 bearing blocks, bed and writing sheet. X axis: 2 uprights, 2 X rods side by side, carriage (4 bearing blocks and a plate). 8 × LM8SUU. Not placed yet: 2 × NEMA 17 |

Units are millimetres and the model is Y-up (the Fusion default). To edit it, open the `.f3z` in Fusion 360 with *File → Open → Open from my computer*.

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

## History

| Date | Commit | Contents |
|---|---|---|
| 2026-10-10 | 43bfe0b | First parts: base, 4 rods, 10 × LM8SUU bearings, 2 × NEMA 17 (STEP only) |
| 2026-10-11 | 3e2a26e | Y axis: 4 rod supports, 2 Y rods, 4 bearing blocks, bed (not placed yet) |
