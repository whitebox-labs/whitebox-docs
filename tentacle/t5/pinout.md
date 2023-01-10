# <i class="fas fa-microchip"></i> Pinout

The Whitebox T5 connects to these Raspberry Pi pins

| Physical Pin | BCM pin | Name       | on the Whitebox T3             |
|-------------:|:---------|:----------|:-------------------------------|
| 1            | 3V3     | 3.3V Power | Power ports 1 + 2              |
| 9            | GND     | GND        | GND                            |
| 3            | BCM 2   | SDA        | I2C SDA                        |
| 5            | BCM 3   | SCL        | I2C SCL                        |

The Whitebox T5 does not "occupy" any pin exclusively. The T5 is mostly transparent to other HATs - they can even be stacked on top and will work as usual.

![Whitebox T5](/_media/whitebox-t5.jpg)


## Port 1

* Isolation: **Yes**, full power and data isolation
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe Connection: SMA (female)
* Best suited for:
  * `EZO pH`
  * `EZO ORP`
  * `EZO EC`
  * `EZO DO`
  * `EZO RTD` (no isolation needed)
* Voltages on the **non-isolated** (Raspberry Pi) side:
 * Vcc: `3.3V `
 * I2C: `3.3V `
* Voltages on the **isolated** (EZO) side:
 * Vcc: `3.9`
 * I2C: `3.9`

## Port 2

* Isolation: **No**
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe Connection: SMA (female)
* Best suited for:
 * `EZO RTD`
 * `EZO Humidity`
* VCC: `3.3V`
* I2C: `3.3V`


## Configuration pins
Using solder jumpers, you can select what Raspberry GPIO pin is used to disable port 1. The solder jumpers can be closed by soldering a bridge between the 2 pads of the jumper.

The solder jumpers can be found on the bottom side of the T5:
![Whitebox T5 back](/_media/whitebox-t5-back.jpg)

?> Only ever close one solder jumper at a time. If you need to change the GPIO used for disabling port 1, de-solder the other jumper first.

![Whitebox T5 enable pin config](/_media/whitebox-t5-pin-config.jpg)

### Disable
The isolator of port 1 can be disabled. If disabled, the EZO circuit is cut from power.
* `closed solder jumper pin`: LOW/GND = port 1 is disabled. HIGH/3.3V = port 1 is enabled. NC = port 1 is on
