# Wiring

| Item | Connection |
|---|---|
| Power | 12 V supply → shield blue terminal (check polarity, no reverse protection) |
| X driver | X slot, EN pin aligned with EN on the shield, M0/M1/M2 jumpers on |
| Y driver | Y slot, same as X |
| X motor | 4-pin header next to the X driver. Coils: red+green / blue+black |
| Y motor | 4-pin header next to the Y driver |
| Servo signal | Z+ limit pin (D11) — pending (servo arrived 2026-10-12) |
| Servo power | LM2596 OUT (5.0 V), IN in parallel with the 12 V supply — pending (LM2596 arrived 2026-10-12) |
| Servo GND | LM2596 OUT−, plus a wire from OUT− to the GND pin next to Z+ (common ground) — pending |

⚠️ Never plug or unplug a motor with the 12 V supply on: it kills the DRV8825.

TODO: add a wiring diagram (Fritzing or hand drawing) as `wiring.png`.
