# Latest source of official WCH OpenOCD (2024-11-26 version)

This repo is the latest source of WCH OpenOCD **(2024-11-26 version)**.

- support WCH-Link / LinkE / LinkS / LinkW debuggers with latest firmware.
- support program / debug all WCH ch32v/x/l series MCUs and some MCU models in future.

Up to 2024-11-26, the laste firmware version:

- WCH-Link (CH549): v2.12
- WCH-LinkE (CH32V305FBP6): v2.15

**To update to latest firmware, read "[how to update firmware of WCH-Link/LinkE](https://github.com/cjacker/opensource-toolchain-ch32v#how-to-update-firmware-of-wch-linke)". If you didn't update firmware of WCH-Link/E, you may have to use [old version WCH OpenOCD](https://github.com/cjacker/wch-openocd-2022).**

## Installation

```
./bootstrap
./configure --prefix=/opt/wch-openocd --enable-wlinke --disable-ch347 --disable-linuxgpiod --disable-werror --program-prefix=wch-
make
sudo make install
```

After installation successfully, please add `/opt/wch-openocd/bin` to your PATH env.

## Usage

```
wch-openocd -f /opt/wch-openocd/share/openocd/scripts/target/wch-riscv.cfg

```

You may copy `wch-riscv.cfg` to your project dir to avoid such long file path.

