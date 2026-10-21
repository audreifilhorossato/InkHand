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
| Servo GND | Brown wire → LM2596 OUT−. The ground is common through the supply: its V− goes to the shield and to IN−, and IN− and OUT− are joined inside the module. If the servo jitters, add a jumper from OUT− to the GND pin of Z+ (not fitted for the test) |

⚠️ Never plug or unplug a motor with the 12 V supply on: it kills the DRV8825.

Servo test wiring, 2026-10-17: [F008](../../docs/photos/F008.jpg).

On the base (Fusion 360 model, since 2026-10-19): the Arduino with the shield on 4 printed standoffs and the LM2596 on 2 more, about 6 mm from the Arduino. Each board is screwed from under the base with M3 × 25 and a nut on top ([journal](../../docs/journal/2026-10-19.md#the-model-on-this-day)).

TODO: add a wiring diagram (Fritzing or hand drawing) as `wiring.png`.
