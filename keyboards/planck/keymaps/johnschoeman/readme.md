# John's Planck Layout

## Dependencies

```
git clone git@github.com:johnschoeman/qmk_firmware.git
cd qmk_firmware
python3 -m pip install --user qmk
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
