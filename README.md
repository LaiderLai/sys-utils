# System Utilities Snap Package for Diagnostics

To build system utilities' snap pakcage for diagnostics.

## Setup the build environment

1. A device working with the Ubuntu desktop 24.04 (noble) or later versions

2. Install snapcraft and lxd

    ```
    sudo snap install snapcraft --channel=9.x/stable --classic
    sudo snap install lxd --channel=5.21/stable
    ```

    **Tip**
    * `lxd init --auto` to initial the LXD settings.

## Build the snap package

1. Build with the snapcraft tool.
    ```
    cd core26
    snapcraft pack
    ```

    **Tip**
    * Building on an amd64 host targets amd64, whereas building on an arm64 host targets arm64.

## Install the snap package

1. A device working with the Ubuntu Core 24 or later versions' [dangerous grade](https://documentation.ubuntu.com/core/reference/assertions/model/) version

    `sudo snap install sys-utils_<VER>_<ARCH>.snap --dangerous --devmode`

    **Tip**
    * <ARCH> supports `amd64` and `arm64`.
    * `--dangerous` to make the system accept installing unsigned snap package.
    * `--devmode` to make the system (AppArmor) allow all operation permissions.

## The includes system utilities

1. `sys-utils.lspci`
2. `sys-utils.lsusb`
3. `sys-utils.usb-devices`
4. `sys-utils.lshw`
5. `sys-utils.i2cdetect`
6. `sys-utils.i2cdump`
7. `sys-utils.i2cget`
8. `sys-utils.i2cset`
9. `sys-utils.i2ctransfer`
10. `sys-utils.sensors`
