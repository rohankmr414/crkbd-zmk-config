# Corne / Acorn ZMK layout

A 42-key QWERTY split layout for macOS, Linux, and Windows, with plain Space on the right thumb, dedicated modifiers, and separate navigation, symbol, and settings layers.

The keymap lives in [config/acorn.keymap](config/acorn.keymap). These diagrams show each layer's explicit bindings. Transparent positions are marked `TRNS` instead of repeating the inherited keys. The thumb keys are shown left to right as they appear in the keymap; spacing is schematic.

## Key labels

| Label | Meaning |
| --- | --- |
| Ctrl | Ctrl / Control (⌃) |
| Alt | Alt / Option (⌥) |
| GUI | Command (⌘) / Windows / Super |
| LShift / RShift | Left / right Shift (⇧) |
| Bksp | Backspace; the backward-delete key often labeled Delete on a Mac |
| Del | Forward Delete (⌦) |
| Esc/Rse | Tap for Escape; hold for Raise |
| TRNS | Transparent: use the next active layer below, ultimately Base |
| --- | Disabled key; sends nothing |

Symbols assume a US host keyboard layout. Native navigation and modifier keys are shared across operating systems; applications and the host OS determine their exact effects.

## Base — typing

```text
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  Tab  |   Q   |   W   |   E   |   R   |   T   |   |   Y   |   U   |   I   |   O   |   P   |  Bksp |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  Ctrl |   A   |   S   |   D   |   F   |   G   |   |   H   |   J   |   K   |   L   |   ;   |   '   |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
| LShift|   Z   |   X   |   C   |   V   |   B   |   |   N   |   M   |   ,   |   .   |   /   | RShift|
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
                        |  Alt  |  GUI  | Enter |   | Space | Lower |Esc/Rse|
                        +-------+-------+-------+   +-------+-------+-------+
```

Space and Enter are ordinary single-purpose keys. Ctrl occupies the usual Caps Lock position. Caps Lock and F1–F12 are not currently mapped.

- Hold **Lower** for numbers and navigation.
- Tap **Esc/Rse** for Escape, or hold it for symbols.
- Hold **Lower + Esc/Rse** to enter Settings once Raise activates.

Escape/Raise uses a 200 ms `balanced` hold-tap: a short tap produces Escape; holding for 200 ms activates Raise. Pressing and releasing another key while Escape/Raise remains held can activate Raise sooner. Releasing Escape/Raise first during a quick roll can still resolve as Escape.

## Lower — numbers and navigation

```text
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  Tab  |   1   |   2   |   3   |   4   |   5   |   |   6   |   7   |   8   |   9   |   0   |  Del  |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  TRNS |  TRNS |  TRNS |  TRNS |  TRNS |  TRNS |   |  Left |  Down |   Up  | Right |  TRNS |  TRNS |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
| LShift|  TRNS |  TRNS |  TRNS |  TRNS |  TRNS |   |  Home |  PgDn |  PgUp |  End  |  TRNS |  TRNS |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
                        |  TRNS |  TRNS | Enter |   | Space |  TRNS |  TRNS |
                        +-------+-------+-------+   +-------+-------+-------+
```

The left-hand home-row and bottom-row letters remain available, so editing shortcuts such as Ctrl/Control or Command + A, Z, X, C, and V can be used while Lower is held. Both Shift keys, Alt/Option, and GUI/Command/Windows/Super retain their base positions.

| Hold Lower and press | Action |
| --- | --- |
| Q through P | Numbers 1 through 0 |
| H / J / K / L | Left / Down / Up / Right |
| N / M / comma / period | Home / Page Down / Page Up / End |
| Backspace | Forward Delete |

## Raise — symbols

```text
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  Tab  |   !   |   @   |   #   |   $   |   %   |   |   ^   |   &   |   *   |   (   |   )   |  Bksp |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  Ctrl |  TRNS |  TRNS |  TRNS |  TRNS |  TRNS |   |   -   |   =   |   [   |   ]   |   \   |   `   |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
| LShift|  TRNS |  TRNS |  TRNS |  TRNS |  TRNS |   |   _   |   +   |   {   |   }   |   |   |  TRNS |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
                        |  TRNS |  TRNS | Enter |   | Space |  TRNS |  TRNS |
                        +-------+-------+-------+   +-------+-------+-------+
```

Right Shift stays available. To type a tilde (`~`), hold **Raise + Left Shift**, then press the base-layer apostrophe key, which becomes backtick on Raise. Alt/Option and GUI/Command/Windows/Super also stay in their usual thumb positions.

## Settings — hold Lower + Raise

```text
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  ---  |  BT1  |  BT2  |  BT3  |  BT4  |  BT5  |   |  ---  |  ---  |  ---  |  ---  |  ---  |  ---  |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  ---  |  ---  |  ---  |  ---  |  ---  |  ---  |   |  ---  |  ---  |  ---  |  ---  |  ---  |  ---  |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
|  ---  | Studio|  ---  |  ---  |  ---  | BTCLR |   |  ---  |  ---  |  ---  |  ---  |  ---  |  ---  |
+-------+-------+-------+-------+-------+-------+   +-------+-------+-------+-------+-------+-------+
                        |  ---  |  ---  |  ---  |   |  ---  |  TRNS |  TRNS |
                        +-------+-------+-------+   +-------+-------+-------+
```

Settings takes priority when Lower and Raise are both active. Releasing either layer key exits Settings, leaving whichever individual layer is still held. All unused Settings keys are disabled; the two layer-access positions are transparent so their existing behavior is preserved.

| While Settings is active | Action |
| --- | --- |
| Q / W / E / R / T | Select Bluetooth profile 1 / 2 / 3 / 4 / 5 |
| B, held for one second | Clear the selected Bluetooth profile's pairing |
| Z | Unlock ZMK Studio for keymap editing |

A short tap of B does nothing. Other keypresses cannot shorten the one-second hold. Select the intended profile before holding B. After clearing an existing pairing, forget the keyboard on that host and pair again. Profile labels BT1–BT5 correspond to firmware indices 0–4. See [ZMK's Bluetooth behavior documentation](https://zmk.dev/docs/keymaps/behaviors/bluetooth).

The Settings layer uses [ZMK conditional layers](https://zmk.dev/docs/keymaps/conditional-layers). Two additional layers remain reserved for Studio use.

## Building and using the configuration

[build.yaml](build.yaml) defines two firmware targets:

| Half | Board | Shield |
| --- | --- | --- |
| Left / central | `nice_nano_v2` | `acorn_central_left` |
| Right / peripheral | `nice_nano_v2` | `acorn_peripheral_right` |

The [GitHub Actions workflow](.github/workflows/build.yml) runs on pushes, pull requests, and manual dispatch. Push changes, check that both firmware targets build successfully, then download the resulting firmware artifact. Use the matching firmware for each half when flashing.

ZMK and the external keyboard module currently track `main` in [config/west.yml](config/west.yml), so upstream changes can affect future builds even when this keymap is unchanged.

If you have saved keymap changes in **ZMK Studio**, they can override the compiled keymap after flashing. To use this repository's layout, use **Restore Stock Settings** in Studio; this replaces the saved Studio customization. See [ZMK Studio's keymap documentation](https://zmk.dev/docs/features/studio#keymap-changes).

After flashing, check Escape/Raise timing, both layer activation orders, modifier-plus-navigation shortcuts, and the Settings bindings on your intended operating systems. To test the destructive pairing-clear action, use a profile you are prepared to pair again.
