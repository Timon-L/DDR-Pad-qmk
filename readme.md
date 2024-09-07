# DDR Controller - QMK Firmware

This repository contains the QMK firmware for the DDR Controller, designed for use with the RP2040 microcontroller. This controller is specifically designed for use in Dance Dance Revolution (DDR) setups, allowing for custom key mappings and easy configuration using QMK.
Features

    5-button setup for DDR use.
    RP2040 microcontroller (Pro Micro RP2040).
    Full QMK support for custom key mapping and firmware updates.
    Backlight support for visual feedback.
    NKRO (N-Key Rollover) support.
    Bootmagic enabled for easy bootloader access.

### Hardware Configuration

    Microcontroller: RP2040 (Pro Micro RP2040)
    Diode Direction: ROW2COL (ensure diodes are installed correctly for this configuration).
    Matrix Layout: 5-row, 1-column matrix
    Matrix Pins:
        Column Pin: GP4
        Row Pins: GP0, GP1, GP2, GP3, GP5
    Backlight Pin: GP28 for optional LED backlighting.

### Flashing the Firmware

To flash the firmware to your DDR Controller, follow these steps:
1. Install QMK CLI
If you haven't already, install the QMK CLI by following the QMK CLI installation guide.
2. Flash the Firmware
Once QMK is installed, navigate to your QMK directory, and use the following command to flash the firmware to the DDR Controller:

```
bash
qmk flash -kb ddrcontroller -km default
```

This command will compile and flash the default keymap to your DDR Controller. Make sure your controller is in bootloader mode by pressing the reset button or using Bootmagic.
3. Custom Keymaps
To create a custom keymap, you can edit the keymap.c file located in the keyboards/ddrcontroller/keymaps/ folder. After modifying the keymap, compile and flash the firmware using the same command:

```
bash
qmk flash -kb ddrcontroller -km <your_custom_keymap>
Layout
```

The current layout uses a simple 5-button matrix:
	Column 1 (GP4)
Row 1 (GP0)	DDR Button 1 (Up)
Row 2 (GP1)	DDR Button 2 (Down)
Row 3 (GP2)	DDR Button 3 (Left)
Row 4 (GP3)	DDR Button 4 (Right)
Row 5 (GP5)	DDR Button 5 (Center)

#### License
This project is licensed under the GPLv2 License as per the QMK firmware.
