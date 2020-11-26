# Quickstart Tutorial

## Prerequisites
For this quickstart tutorial you need:
* One or more EZO Devices by Atlas Scientific, protocol set to `I2C`
* An Arduino (also see [Compatibility](compatibility.md))
* A [Whitebox T2 Mini MkII for Arduino](https://www.whiteboxes.ch/shop/t2-mini-mk2/)
* The * [Whitebox Interactive EZO Console](https://github.com/whitebox-labs/whitebox-ezo-console/archive/main.zip ':target=_blank')

!> **I2C only** The Whitebox T2 Mini MkII works with EZO devices in `I2C` mode only. Before using your EZO devices with the Whitebox T2 Mini, switch them to `I2C`. [How to switch EZO Circuits to I2C](protocols.md)

## Setup Procedure

?> Your Arduino should be **off** and the Whitebox T2 Mini not yet plugged into the Arduino.

1. Switch your EZO devices to `I2C`. [How to switch EZO Circuits to I2C](protocols.md)
1. Plug your Atlas Scientific devices into the Whitebox T2 Mini. See [Pinout](pinout.md) to learn what devices are suited for which ports.
 * Double-check the correct orientation of the EZO devices
1. Mount the Whitebox T2 Mini to your Arduino
1. Power up the Arduino
1. Load the [Whitebox Interactive EZO Console](https://github.com/whitebox-labs/whitebox-ezo-console/archive/main.zip ':target=_blank')
1. Open the Arduino IDE serial monitor `@9600 baud` ![Tentacle Interactive Prompt Setup](_media/tentacle_setup_prompt.png)
1. Your EZO devices are listed.

```
------------------
-- I2C CHANNEL 99
--
-- Type: EZO pH

SCAN COMPLETE
1 circuits found
```

You will see all your circuits appearing. In this example, only one EZO pH circuit is mounted and it has the `I2C` address `99`


## Interact with the EZO Circuits
Connect to a circuit by typing it’s channel number: `0<ENTER>`

```
changing channel to 99
-------------------------------------
ACTIVE channel : 99
Type: EZO ORP, Version: 1.0, COM: I2C
```

What you type now, is directly sent to the active EZO device at address 99. For example, type `r` to get the newest reading.

![Tentacle Interactive Command](_media/tentacle_setup.gif)

Congratulations, you’re all set to configure and use your Atlas Scientific EZO deivces! Grab the datasheet of your EZO device and start exploring all the available commands.

## EZO Circuit Datasheets
[filename](../common/ezo-datasheets.md ':include')
