I bought this ergodox low-profile keyboard from slicemk.com.

https://docs.slicemk.com/firmware/zmk/wireless/guide/


# Keymap config

I configure the keymap using https://config.slicemk.com/zmk/keymap/?keyboard=ergodox&layout=QWERTY.

Build Target (where you will run ZMK):
_To identify the correct "Build Target" for Raytac dongles, please check the "Model" value within the INFO_UF2.TXT file on the dongle's MDBT50QBOOT virtual drive. Make sure to choose the corresponding "Green" build target if the "Model" contains "Green"._
```bash
cat /media/$USER/MDBT50QBOOT/INFO_UF2.TXT
# UF2 Bootloader 0.6.4-20-gdf1fddf lib/nrfx (v2.0.0) lib/tinyusb (0.12.0-145-g9775e769) lib/uf2 (remotes/origin/configupdate-9-gadbb8c7)
# Model: Raytac MDBT50Q-RX Green
# Board-ID: nRF52833-MDBT50Q_RX-green
# Date: Aug 26 2022
# SoftDevice: not found
```

Firmware Version (leave unchanged if you are not sure):
v20250120 (69de44c)
