# Flashing Firmware

## Overview

My 'central' is a dongle (usb bluetooth), so:

1. Build the firmware using the keymap configurator.
2. Plug in the USB dongle.
3. Place the dongle in bootloader mode. The user LED should pulse slowly while in bootloader mode.
4. Ensure that it has been at least 15 seconds since resetting both peripherals halves (the final step in Peripheral Flashing section).
5. Copy zmk-dongle.uf2 to the dongle virtual drive. The user LED will flash very quickly while it's flashing. The user LED will turn off when flashing is complete.
6. Unplug the dongle and plug it back in.
7. Press a few keys on the keyboard halves. Give it a couple of seconds for them to bond with the dongle. Both halves should work after this is complete.

## 1. Build the firmware using the keymap configurator.

After building firmware on https://config.slicemk.com/zmk/build/53IfPGaW-hXQich_QJZOucYPoiTb7kTA/, downloading, and unzipping the file, you have:

- slicemk_ergodox_dongle.conf
- slicemk_ergodox.keymap
- slicemk_keymap.json
- zmk-dongle.uf2

## 2. Plug in the USB dongle.

## 3. Place the dongle in bootloader mode. The user LED should pulse slowly while in bootloader mode.

> To update the firmware running on a dongle or keyboard half, it should be connected via USB and put into bootloader mode. All dongles/keyboards are shipped with an UF2 bootloader. While in bootloader mode, you will see a virtual flash drive on your computer.

> On dongles, the user button is equivalent to the &bootloader key. Pressing it once will place the device in bootloader mode.
https://docs.slicemk.com/firmware/zmk/wireless/button-led/

## 4. Ensure that it has been at least 15 seconds since resetting both peripherals halves (the final step in Peripheral Flashing section).

## 5. Copy zmk-dongle.uf2 to the dongle virtual drive. The user LED will flash very quickly while it's flashing. The user LED will turn off when flashing is complete.

`cp zmk-dongle.uf2 /media/$USER/MDBT50QBOOT/`

## 6. Unplug the dongle and plug it back in.

## 7. Press a few keys on the keyboard halves. Give it a couple of seconds for them to bond with the dongle. Both halves should work after this is complete.
