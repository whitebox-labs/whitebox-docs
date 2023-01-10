# <i class="fas fa-angle-double-right"></i> Quickstart Tutorial

## Prerequisites
For this quickstart tutorial you need:
* One or more EZO Circuits by Atlas Scientific, protocol set to `I2C`
* A Raspberry Pi (2, 3, 4, Zero - see [Compatibility](compatibility.md) for a full list)
* A [Whitebox T5 for Raspberry Pi](https://www.whiteboxes.ch/shop/whitebox-t5/)

!> **I2C only** The Whitebox T3 works with EZO circuits in `I2C` mode only. Before using your EZO Circuits with the Whitebox T3, switch them to `I2C`. [How to switch EZO Circuits to I2C](protocols.md)

## Preparing the Raspberry Pi

?> Don't mount the Whitebox T5 to the Raspberry Pi yet

1. Download a recent version of Raspbian _(this Tutorial was made with Jessie, Release 2017-03-02, but any later version should work)_:
https://www.raspberrypi.org/downloads/raspbian/
1. Burn the img-file to an SD card, e.g. using [Etcher](https://etcher.io/) (for Windows, OSX, Linux)
1. Boot your Pi (the Whitebox T5 still **not connected**)
1. Use the terminal to start the `raspi-config` tool:
```
sudo raspi-config
```
1. In the menu, find the option to activate `I2C`.
 ![raspi-config](_media/raspi-config2.png)
 * At the time of writing this is under `5 Interfacing Options` > `P5 I2C`
1. Enable `I2C`
1. Reboot your Pi
1. Upgrade the system packages:
```
sudo apt-get update
sudo apt-get upgrade
```
1. Install the I2C tools:
```
sudo apt-get install python-smbus
sudo apt-get install i2c-tools
```
1. Reboot your Pi

## Prepare the hardware
?> Your Raspberry Pi is powered **off**

1. All your EZO devices must be in I2C mode. [How to switch EZO Circuits to I2C](protocols.md)
1. If you have a Raspberry Pi Zero, mount the supplied pcb standoffs to the Whitebox T5 for stability
1. Mount the stacking pin header to the T5 from the bottom side
1. Plug your EZO circuits into the Whitebox T5
1. **<i class="fas fa-exclamation-triangle"></i> Double-check the correct circuit orientation**
1. Power up the Raspberry Pi

## Test I2C

In the terminal, type
```
sudo i2cdetect -y 1
```
you will see all your I2C devices in the table.

![raspi-config](_media/i2cdetect.png)

_When the screenshot was taken, an EZO pH Circuit (0x63), an EZO DO Circuit (0x61) and a HDC1008 humidity sensor (0x42) have been connected to the Raspbyerry Pi._

## Ready {docsify-ignore}
to run some [code](code.md)!
