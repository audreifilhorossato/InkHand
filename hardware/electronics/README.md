# Wiring

| Item | Connection |
|---|---|
| Power | 12 V supply → shield blue terminal (check polarity, no reverse protection) |
| X driver | X slot, EN pin aligned with EN on the shield, M0/M1/M2 jumpers on |
| Y driver | Y slot, same as X |
| X motor | 4-pin header next to the X driver. Coils: red+green / blue+black |
| Y motor | 4-pin header next to the Y driver |
| Servo signal | Yellow wire (orange on most MG90S) → signal pin of Z+ on the END STOPS header (D11), the last pair on the right. Tested 2026-10-17 |
| Servo power | Red wire → LM2596 OUT+ (5 V). LM2596 IN+/IN− on the 12 V supply, in parallel with the shield. Never from the Arduino's 5 V. Tested 2026-10-17 |
| Fan | 40 mm, 12 V 0.04 A. Red → +, black → − of the 12 V input (the DC jack terminal), in parallel with the shield and the LM2596. Never on the 5 V output. Sticker side towards the board ([2026-10-27](../../docs/journal/2026-10-27.md#the-fan)) |
| Servo GND | Brown wire → LM2596 OUT−. The ground is common through the supply: its V− goes to the shield and to IN−, and IN− and OUT− are joined inside the module. If the servo jitters, add a jumper from OUT− to the GND pin of Z+ (not fitted for the test) |

⚠️ Never plug or unplug a motor with the 12 V supply on: it kills the DRV8825.

Servo test wiring, 2026-10-17: [F008](../../docs/photos/F008.jpg).

On the base (Fusion 360 model, since 2026-10-19): the Arduino with the shield on 4 printed standoffs and the LM2596 on 2 more, about 6 mm from the Arduino. Each board is screwed from under the base with M3 × 25 and a nut on top ([journal](../../docs/journal/2026-10-19.md#the-model-on-this-day)).

Fitted on 2026-10-27 ([journal](../../docs/journal/2026-10-27.md), photo [F019](../../docs/photos/F019.jpg)): the Arduino with the shield, the LM2596 and the DC jack adapter, screwed to the base. The LM2596's header pins were replaced by wires soldered straight to the 12 V terminal of the DC jack. Solder joints and the terminal are covered with hot glue. One of the Arduino's 4 holes is too close to the components for a nut on top, so its standoff is shorter (2.7 mm) and the board is held by the other 3 for now. The fan sits on a printed support over the shield, about 5 mm above the heatsinks.

Being redone since 2026-11-06 ([journal](../../docs/journal/2026-11-06.md), photo [F026](../../docs/photos/F026.jpg)): the first wiring was weak, with poor cables, so it is being done again with better ones. The fan support broke twice and is glued for now; the fan isn't fixed on it yet.

Fan box, drawn on 2026-11-10 and sent to print ([journal](../../docs/journal/2026-11-10.md#fan-box)): it replaces the fan support. A bracket stands across the end of the Arduino, on 2 of its holes, with the board's own screws through its feet. The box hooks onto the edges of the CNC Shield at the far end and is screwed to the bracket with 2 × M3 × 8. The fan sits inside the box, over a 30 × 36 mm opening above the drivers, held by double-sided tape on its side.

Fan box, 2026-11-13 ([journal](../../docs/journal/2026-11-13.md#fan-box)): the loose leg on the far end is now held by 2 × M3 × 8, with their nuts in pockets on the outside of the box wall, under the leg. In the model the box is back on the Arduino's holes.

Motor wires, 2026-11-13: more of them connected, run up along the upright and held with double-sided tape. There's no cable path in the model yet.

TODO: add a wiring diagram (Fritzing or hand drawing) as `wiring.png`.
