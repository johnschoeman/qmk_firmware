# Quantum Mechanical Keyboard Firmware

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/qmk)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](https://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](https://ergodox-ez.com) keyboard, and the Clueboard product line.

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are powered by [VitePress](https://vitepress.dev/). They are also viewable offline; see [Previewing the Documentation](https://docs.qmk.fm/#/contributing?id=previewing-the-documentation) for more details.

You can request changes by making a fork and opening a [pull request](https://github.com/qmk/qmk_firmware/pulls).

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [ZSA Technology Labs](https://github.com/zsa), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.


# My Keyboards

## Dependencies

https://github.com/qmk/qmk_firmware/pull/25652

```
nix-shell -p qmk --run "qmk clone"
cd qmk_firmware
# Link .envrc file
ln -s ./util/nix/envrc ./.envrc
direnv allow
```

## Configure qmk

```
qmk
qmk config
qmk setup
qmk config user.keyboard=planck/ez
qmk config user.keymap=johnschoeman
```

## Compile and flash

```
qmk compile
qmk flash
```

# Planck drop rev 7 (48)

```
qmk config user.keyboard=planck/rev7
```

/keyboards/planck/keymaps/johnschoeman/keymap.c

---

# Planck EZ (47)

```
qmk config user.keyboard=planck/ez  
```
/keyboards/zsa/planck_ez/keymaps/keymap.c

# Keymap

## BASE

,-----------------------------------------------------------------------------------.
| Esc  |   Q  |   W  |   E  |   R  |   T  |   Y  |   U  |   I  |   O  |   P  | Bksp |
|------+------+------+------+------+------+------+------+------+------+------+------|
| LCtr |   A  |   S  |   D  |   F  |   G  |   H  |   J  |   K  |   L  |   ;  |Enter |
|------+------+------+------+------+------+------+------+------+------+------+------|
|LShift|   Z  |   X  |   C  |   V  |   B  |   N  |   M  |   ,  |   .  |   /  |RShift|
|------+------+------+------+------+------+------+------+------+------+------+------|
| Tab  |      | Alt  | CMD  |Lower |    Space    |Raise | Alt  |      |      |      |
`-----------------------------------------------------------------------------------'

## Lower

,-----------------------------------------------------------------------------------.
| Del  |      |      |   -  |  +   |      |      |  [   |  ]   |      |      | Bksp |
|------+------+------+------+------+------+------+------+------+------+------+------|
|  `   |      |      |   -  |  =   |      |  ;   |  {   |  }   |      |      |      |
|------+------+------+------+------+------+------+------+------+------+------+------|
|LShift|      |      |      |      |      |  '   |  (   |  )   |      |      |RShift|
|------+------+------+------+------+------+------+------+------+------+------+------|
| Tab  |      |      |      |      |             |      | Left | Down |  Up  | Right|
`-----------------------------------------------------------------------------------'

## Raise

,-----------------------------------------------------------------------------------.
|      |      |      |  -   |  +   |      |      |  [{  |  ]}  |      |      | Del  |
|------+------+------+------+------+------+------+------+------+------+------+------|
|   `  |  1!  |  2@  |  3#  |  4$  |  5%  |  6^  |  7&  |  8*  |  9(  |  0)  |  \   |
|------+------+------+------+------+------+------+------+------+------+------+------|
|LShift|      |      |      |      |      |  '   |  ;   |      |      |      |RShift|
|------+------+------+------+------+------+------+------+------+------+------+------|
| Tab  |      |      |      |      |             |      |      |      |      |      |
`-----------------------------------------------------------------------------------'

## Adjust (Lower + Raise)

,-----------------------------------------------------------------------------------.
| Sleep|  F1  |  F2  |  F3  |  F4  |      | Mute | VolDn| VolUp|      | Debug| Reset|
|------+------+------+------+------+------+------+------+------+------+------+------|
| PwrDn|  F5  |  F6  |  F7  |  F8  |      |      | PgDn | PgUp |Qwerty|Plover|      |
|------+------+------+------+------+------+------+------+------+------+------+------|
|      |  F9  |  F10 |  F11 |  F12 |      |      |BrigDn|BrigUp|      |      |      |
|------+------+------+------+------+------+------+------+------+------+------+------|
| Wake |      |      |      |      |             |      |      |      |      |      |
`-----------------------------------------------------------------------------------'

