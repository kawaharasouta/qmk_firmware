# Quantum Mechanical Keyboard Firmware

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Build Status](https://travis-ci.org/qmk/qmk_firmware.svg?branch=master)](https://travis-ci.org/qmk/qmk_firmware)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/Uq7gcHh)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](http://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](http://www.ergodox-ez.com) keyboard, and the [Clueboard product line](http://clueboard.co/).

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are hosted on [Gitbook](https://www.gitbook.com/book/qmk/firmware/details) and [GitHub](/docs/) (they are synced). You can request changes by making a fork and [pull request](https://github.com/qmk/qmk_firmware/pulls), or by clicking the "suggest an edit" link on any page of the docs.

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [Erez Zukerman](https://github.com/ezuk), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official website

[http://qmk.fm](http://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.


# my info

### changing keymap

#### env
```
$ git clone https://github.com/qmk/qmk_firmware
$ cd qmk_firmware
$ ./util/qmk_install.sh
```

#### build
```
make <keybord>:<keymap>
```
*mint60 mymap*
```
make mint60:custom
```

#### write firmware on Micro
*mint60 mymap*
``` 
make mint60:custom:avrdude
```

#### My zinc keymap

**def key**
```
    ,-----------------------------------------.             ,-----------------------------------------.
    | Tab  |   Q  |   W  |   E  |   R  |   T  |             |   Y  |   U  |   I  |   O  |   P  |  [   |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    | Ctrl |   A  |   S  |   D  |   F  |   G  |             |   H  |   J  |   K  |   L  |   ;  |  '   |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    | Shift|   Z  |   X  |   C  |   V  |   B  |             |   N  |   M  |   ,  |   .  |   /  |Enter |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    | Esc  |ADJUST|  Alt |  Win |LOWER |Space |             | Bksp | RAISE| Left | Down |  Up  | Right|
    `-----------------------------------------'             `-----------------------------------------'
```

**right**
```
    ,-----------------------------------------.             ,-----------------------------------------.
    |   `  |   1  |   2  |   3  |   4  |   5  |             |   6  |   7  |   8  |   9  |   0  | Del  |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |  F1  |  F2  |  F3  |  F4  |  F5  |             |  F6  |   -  |   =  |   [  |   ]  |  \   |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |  F7  |  F8  |  F9  |  F10 |  F11 |             |  F12 |      |      |      |      |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |      |      |      |      |      |             |      |      | Next | Vol- | Vol+ | Play |
    `-----------------------------------------'             `-----------------------------------------'
```

**left**
```
    ,-----------------------------------------.             ,-----------------------------------------.
    |   ~  |   !  |   @  |   #  |   $  |   %  |             |   ^  |   &  |   *  |   (  |   )  |      |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |      |      |      |      |      |             |   -  |   _  |   +  |   {  |   }  |  |   |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |      |      |      |      |      |             |      |      |      | Home | End  |      |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |      |      |      |      |      |             |      |      | Next | Vol- | Vol+ | Play |
    `-----------------------------------------'             `-----------------------------------------'
```

**both**
```
    ,-----------------------------------------.             ,-----------------------------------------.
    |      | Reset|RGBRST|Aud on|Audoff|      |             |      |Qwerty|Colemk|Dvorak|      | Ins  |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |RGB ON| HUE+ | SAT+ | VAL+ | Mac  |             | Win  |  -   |   =  |Print |ScLock|Pause |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      | MODE | HUE- | SAT- | VAL- |      |             |      |      |      |      |      |      |
    |------+------+------+------+------+------|             |------+------+------+------+------+------|
    |      |      |      | EISU | EISU | EISU |             | KANA | KANA | Home |PageDn|PageUp| End  |
    `-----------------------------------------'             `-----------------------------------------'
```





