# Firmware

- **Firmware:** GRBL 1.1f with servo PWM (grbl-servo fork). Downloaded ZIP: `grbl-servo-eggbot`.
- **Board:** Arduino UNO + CNC Shield V3.
- **Sender:** Universal G-code Sender (UGS) Platform 2.1.26, Windows, 115200 baud.

## Flashing

1. Unzip the fork and copy **only the inner `grbl` folder** to `Documents\Arduino\libraries\grbl`
   (Arduino IDE 2 fails with *Sketch → Include Library → Add .ZIP*).
2. Open *File → Examples → grbl → grblUpload*, select **Arduino Uno** and the COM port, upload.
3. A "low memory" warning is normal for GRBL.
4. Connect with UGS: the console must show `Grbl 1.1f`.

## Settings

Current values are in [grbl_config.txt](grbl_config.txt) (output of `$$`).

> **Send one `$` command at a time and wait for `ok`.** GRBL stops listening to serial while it writes to EEPROM, so commands sent together get corrupted.

## Pen servo

Tested on 2026-10-17 with the Tower Pro MG90S and the LM2596 ([journal](../docs/journal/2026-10-13_to_2026-10-17.md#servo-and-lm2596-test)).

- Signal on **Z+** limit pin (D11), power from the LM2596 set to **5 V before connecting**, GND common through the supply ([wiring](../hardware/electronics/README.md)).
- Settings, one at a time: `$30=255`, `$31=0`, `$32=0` (laser mode off: with it on, the servo only moves while the axes move).
- Pen up `M5`, pen down `M3 S…`. The S values for pen up and pen down are set with the servo mounted on the carriage.
- No homing needed: the MG90S (about 180°) goes straight to the angle it is sent. Fit the arm after an `M5`.
