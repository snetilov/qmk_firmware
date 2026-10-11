# Lily58 Pro Custom version ( mechboards.co.uk board settings were taken as a base )

A refreshed Lily58 PCB with RGB, battery, power switch and without encoder. (Aliexpress)

* Hardware Supported: RP2040

Base QMK checkout is needed befory checking out this repo. https://github.com/qmk/qmk_firmware
Then add this keyabord settings by hand.
Not forking QMK as I have no intention to make a pull request.

Make example for this keyboard (after setting up your build environment):

    qmk compile -kb custom/lily58/pro -km default

Flashing example for this keyboard:

    qmk flash -kb custom/lily58/pro -km default

## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down the top left key (for left half) or top right key (for right half) when plugging in USB.
* **Physical reset button**: Briefly double press the button below the TRRS socket.
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available

## Build instructions

### In QMK checkout directory
    RUNTIME="docker" SKIP_FLASHING_SUPPORT=true util/docker_cmd.sh

### Inside docker container
    qmk compile -kb=custom/lily58/pro -km=default

Then copy the compiled uf2 file from QMK repository checkout root folder onto P2040
