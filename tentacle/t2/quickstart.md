# Quickstart Tutorial

## Prerequisites
For this quickstart tutorial you need:
* One or more EZO Circuits by Atlas Scientific, protocol set to `I2C`
* An Arduino (also see [Compatibility](compatibility.md))
* A [Tentacle Mini for Arduino](https://www.whiteboxes.ch/shop/tentacle-mini/)
* The [Tentacle Setup Sketch](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/tentacle-setup/tentacle_setup/tentacle_setup.ino ':target=_blank')

!> **I2C only** The Tentacle Mini works with EZO circuits in `I2C` mode only. Before using your EZO Circuits with the Tentacle Mini, switch them to `I2C`. [How to switch EZO Circuits to I2C](protocols.md)

## Setup Procedure

?> Your Arduino should be **off** and the Tentacle Shield not yet plugged into the Arduino.

1. Switch your EZO Circuits to `I2C`. [How to switch EZO Circuits to I2C](protocols.md)
1. Plug your Atlas Scientific circuits into the Tentacle Shield
 * There’s no predefined order for the circuits, you can put them in arbitrary order.
 * Double-check the correct orientation of the EZO circuits
1. Mount the Tentacle Mini to your Arduino
1. Power up the Arduino
1. Load the [Tentacle Setup Sketch](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/tentacle-setup/tentacle_setup/tentacle_setup.ino ':target=_blank') to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud` ![Tentacle Interactive Prompt Setup](_media/tentacle_setup_prompt.png)
1. type `scani2c` and press ENTER.

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

What you type now, is directly sent to the circuit on serial channel 0. For example, type `r` to get the newest reading.

![Tentacle Interactive Command](_media/tentacle_setup.gif)

Congratulations, you’re all set to configure and use your Atlas Scientific circuits! Grab the datasheet of your EZO circuit and start exploring all the available commands.

## EZO Circuit Datasheets
[filename](../common/ezo-datasheets.md ':include')
