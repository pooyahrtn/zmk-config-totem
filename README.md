# zmk-config-totem

ZMK config for the official GEIST Totem (38-key low-profile split, Choc v1, SEEED XIAO BLE).
Ported from `zmk-config-sofle59` — homerow-mod tuning carried over; key positions remapped
for the Totem's 10/10/12/6 row layout.

## Build

GitHub Actions builds firmware on push via `.github/workflows/build.yml`.
Outputs: `totem_left`, `totem_right`, `settings_reset` UF2s.

## Module

Uses community ZMK module `BildermanKawasaki/zmk-keyboard-TOTEM` (pinned to `main`).
ZMK pinned to `v0.3` — newer ZMK `main` has Zephyr 4.1 breaking changes the shield
doesn't account for.

## Layout

```
 0  1  2  3  4     5  6  7  8  9
10 11 12 13 14    15 16 17 18 19
20 21 22 23 24 25 26 27 28 29 30 31
         32 33 34    35 36 37
```

- Homerow mods on positions 10–13 (left: A S D F) and 16–19 (right: J K L ;)
- Combos: backspace (16+17), delete (12+18), esc (10+25)
- ZMK Studio is not supported by the shield yet (upstream issue GEIGEIGEIST/TOTEM#51)
