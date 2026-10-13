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

## Pen servo (pending)

The servo and the LM2596 arrived on 2026-10-12. Test pending.

- Signal on **Z+** limit pin (D11), power from LM2596 set to **5.0 V before connecting**, common GND.
- `$30=255`, pen down `M3 S30` (to calibrate), pen up `M5`.
