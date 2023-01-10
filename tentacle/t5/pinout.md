# <i class="fas fa-microchip"></i> Pinout

The Whitebox T5 connects to these Raspberry Pi pins

| Physical Pin | BCM pin | Name       | on the Whitebox T3             |
|-------------:|:---------|:----------|:-------------------------------|
| 1            | 3V3     | 3.3V Power | Power ports 1 + 2              |
| 9            | GND     | GND        | GND                            |
| 3            | BCM 2   | SDA        | I2C SDA                        |
| 5            | BCM 3   | SCL        | I2C SCL                        |

The Whitebox T5 does not "occupy" any pin exclusively. The T5 is mostly transparent to other HATs - they can even be stacked on top and will work as usual.

![Whitebox T3](/_media/whitebox-t3-ports-4-5.jpg)


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
Connect port configuration pins to your circuits or Raspberry GPIO pins.



### Disable
The isolators in port 1 and 2 can be disabled. If disabled, the EZO circuit is cut from power.
* `1`: LOW/GND = port 1 is disabled. HIGH/3.3V = port 1 is enabled. NC = port 1 is on
* `2`: LOW/GND = port 2 is disabled. HIGH/3.3V = port 2 is enabled. NC = port 2 is on


![Whitebox T3 port config](/_media/whitebox-t3-port-config.jpg)
