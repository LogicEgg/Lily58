# Lily58 handwired - ZMK config (SuperMini nRF52840)

1. Push this folder to a new GitHub repo (it must include the hidden .github folder).
2. Actions tab -> wait for the build -> download the "firmware" artifact.
3. For each half: short RST to GND twice quickly -> a USB drive (NICENANO) appears -> copy the matching .uf2 onto it.
   - left half:  lily58hw_left-nice_nano_v2-zmk.uf2  (central; pairs with your computer)
   - right half: lily58hw_right-nice_nano_v2-zmk.uf2
4. Pair "Lily58" over Bluetooth.

If the halves won't connect: flash settings_reset-nice_nano_v2-zmk.uf2 to BOTH halves, then re-flash the
normal firmware, then reset both halves at the same time.

## Firmware builds

Download firmware from the Actions run that matches what you want:

| Build | Keymap |
|---|---|
| [Reserve extra layers](https://github.com/LogicEgg/zmk-config-lily58hw/actions/runs/41030529386) | Default keymap (stock starter layout) |
| **Back up Studio layout to keymap** | My keybinds (exported from ZMK Studio) |

The keymap only loads after `settings_reset` or **Restore Stock Settings** in ZMK Studio.
Until then, the keyboard keeps whatever layout was last saved in Studio.
