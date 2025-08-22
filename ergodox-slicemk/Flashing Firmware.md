# Flashing Firmware

Dongle (usb bluetooth)
Model: Raytac MDBT50Q-RX Green
Board-ID: nRF52833-MDBT50Q_RX-green

Peripheral (keyboard halves)
Model: SliceMK
Board-ID: nRF52833-slicemk-ergodox-202207-green

## Overview

1. (First time only) Download the firmware for the keyboard halves from https://docs.slicemk.com/keyboard/ergodox/peripheral/.
2. (First time only) Install the specific half firmware on each half.
3. Build the firmware for the central on https://config.slicemk.com/zmk/. Download the zip file.
4. Install the central firmware on the dongle because I've chose the dongle (usb bluetooth) as my central.

## 1. Build the firmware using the keymap configurator.

After building firmware on https://config.slicemk.com/zmk/build/53IfPGaW-hXQich_QJZOucYPoiTb7kTA/, downloading, and unzipping the file, you have:

- slicemk_ergodox_dongle.conf
- slicemk_ergodox.keymap
- slicemk_keymap.json
- zmk-dongle.uf2

## 2. Plug in the USB dongle.

## 3. Place the dongle in bootloader mode. The user LED should pulse slowly while in bootloader mode.

1. Turn on both keyboard halves. (Press the reset button once (right).)
2. Press the button on the dongle once to enter bootloader mode. That should give you a device at `/media/$USER/MDBT50QBOOT` (or whatever matches your dongle).
3.

> To update the firmware running on a dongle or keyboard half, it should be connected via USB and put into bootloader mode. All dongles/keyboards are shipped with an UF2 bootloader. While in bootloader mode, you will see a virtual flash drive on your computer.

> On dongles, the user button is equivalent to the &bootloader key. Pressing it once will place the device in bootloader mode.
https://docs.slicemk.com/firmware/zmk/wireless/button-led/

## 4. Ensure that it has been at least 15 seconds since resetting both peripherals halves (the final step in Peripheral Flashing section).

## 5. Copy zmk-dongle.uf2 to the dongle virtual drive. The user LED will flash very quickly while it's flashing. The user LED will turn off when flashing is complete.

`cp zmk-dongle.uf2 /media/$USER/MDBT50QBOOT/`

## 6. Unplug the dongle and plug it back in.

## 7. Press a few keys on the keyboard halves. Give it a couple of seconds for them to bond with the dongle. Both halves should work after this is complete.
