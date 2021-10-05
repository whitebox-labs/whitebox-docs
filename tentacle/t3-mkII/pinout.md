# <i class="fas fa-microchip"></i> Pinout

The Whitebox T3 connects to these Raspberry Pi pins

| Physical Pin | BCM pin | Name       | on the Tentacle T3             |
|-------------:|:---------|:----------|:-------------------------------|
| 1            | 3V3     | 3.3V Power | Power the I2C signal isolators |
| 2            | 5V      | 5V Power   | Power the DC isolators         |
| 9            | GND     | GND        | GND                            |
| 3            | BCM 2   | SDA        | I2C SDA                        |
| 5            | BCM 3   | SCL        | I2C SCL                        |

The Whitebox T3 does not "occupy" any pin exclusively. The T3 is mostly transparent to other HATs - they can even be stacked on top and will work as usual.

![Whitebox T3](/_media/whitebox-t3-channels.png)


## Channel 1 + 2

* Isolation: **Yes**, full power and data isolation
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe Connector: BNC
* Best suited for:
 * `EZO pH`
 * `EZO ORP`
 * `EZO EC`
 * `EZO DO`
 * `EZO RTD` (no isolation needed)
* Voltages on the **non-isolated** (Raspberry Pi) side:
 * Vcc: `5V `
 * I2C: `3.3V `
* Voltages on the **isolated** (EZO) side:
 * Vcc: `5V`
 * I2C: `5V`

## Channel 3
* Isolation: **No**
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe Connector: BNC
* Best suited for:
 * `EZO RTD`
 * `EZO Flow`
* VCC: `3.3V`
* I2C: `3.3V`

## Channel 4 + 5
* Isolation: **No**
* Footprint: EZO Data Connector (e.g. to connect a Molex connector)
* Protocol: `I2C` only
* Best suited for:
 * 5pin EZO-Data devices like the EZO-PMP, EZO-CO2 or EZO-PRS
 * 3rd-party I2C devices like the I2C Soil Moisture Sensor
* VCC: `3.3V`
* I2C: `3.3V`

### Pinout Channel 4 + 5
![Whitebox T3](/_media/channels4-5.png)
* `3V3`: 3.3V
* `GND`: GND
* `SDA`: I2C SDA
* `SCL`: I2C SCL
* `ALM`: Some devices from Atlas Scientific provide additional functionality (e.g. Alarms) to this pin. Both channel 4 and 5 ALM pins are exposed in the [configuration pins](#configuration-pins).



## Configuration pins
The configuration pins allow to connect channel configuration pins to your circuits or Raspberry GPIO pins.



### Disable
The isolators in channel 1 and 2 can be disabled. If disabled, the EZO circuit is cut from power.
* `1`: LOW/GND = channel 1 is disabled. HIGH/3.3V = channel 1 is enabled. NC = channel 1 is on
* `2`: LOW/GND = channel 2 is disabled. HIGH/3.3V = channel 2 is enabled. NC = channel 2 is on

### ALM
* `4`: Channel 4 ALM pin
* `5`: Channel 5 ALM pin

?> **Tip with EZO-PMP**: You can use the ALM pin to know whether the pump is currently running or not. Connect the ALM pin to a Raspberry GPIO and read the pin state: if it's HIGH, the pump is running, if it's LOW, the pump is off.
