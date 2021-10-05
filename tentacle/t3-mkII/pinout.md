# <i class="fas fa-microchip"></i> Pinout

The Whitebox T3 connects to these Raspberry Pi pins

| Physical Pin | BCM pin | Name       | on the Whitebox T3             |
|-------------:|:---------|:----------|:-------------------------------|
| 1            | 3V3     | 3.3V Power | Power ports 4 + 5            |
| 2            | 5V      | 5V Power   | Power ports 1 + 2           |
| 9            | GND     | GND        | GND                            |
| 3            | BCM 2   | SDA        | I2C SDA                        |
| 5            | BCM 3   | SCL        | I2C SCL                        |

The Whitebox T3 does not "occupy" any pin exclusively. The T3 is mostly transparent to other HATs - they can even be stacked on top and will work as usual.

![Whitebox T3](/_media/whitebox-t3-ports-4-5.jpg)


## Port 1 + 2

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
 * Vcc: `5V `
 * I2C: `3.3V `
* Voltages on the **isolated** (EZO) side:
 * Vcc: `3.9`
 * I2C: `3.9`

## Port 3
* Isolation: **No**
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe Connection: SMA (female)
* Best suited for:
 * `EZO RTD`
 * `EZO Flow`
* VCC: `3.3V`
* I2C: `3.3V`

### Port 3 Flow Connector

When using the EZO Flow Meter Totalizer Circuit, the actual flow meter must be attached to the flow connector on the side. Solder the Atlas Flow connector board or your own custom connector to the T3.
![Whitebox T3 Flow connector](/_media/whitebox-t3-flow.jpg)
* `R`: Red
* `W`: White
* `B`: Black

?> **IMPORTANT**: When using port 3 with EZO Flow, the Port 3 SMA connector must not be connected to anything

## Port 4 + 5
* Isolation: **No**
* Footprint: EZO Data Connector (standard male 5 pin header, 2.54mm/0.1" spacing)
* Protocol: `I2C` only
* Best suited for:
 * 5pin EZO-Data devices like the EZO-PMP, EZO-CO2 or EZO-PRS
 * 3rd-party I2C devices like the I2C Soil Moisture Sensor
* VCC: `3.3V`
* I2C: `3.3V`

### Pinout Port 4 + 5
![Whitebox T3 port 4 + 5](/_media/whitebox-t3-ports-4-5-2.jpg)
* `3V3`: 3.3V
* `GND`: GND
* `SDA`: I2C SDA
* `SCL`: I2C SCL
* `ALM`: Some devices from Atlas Scientific provide additional functionality (e.g. Alarms) to this pin. Both port 4 and 5 ALM pins are exposed in the [configuration pins](#configuration-pins).



## Configuration pins
Connect port configuration pins to your circuits or Raspberry GPIO pins.



### Disable
The isolators in port 1 and 2 can be disabled. If disabled, the EZO circuit is cut from power.
* `1`: LOW/GND = port 1 is disabled. HIGH/3.3V = port 1 is enabled. NC = port 1 is on
* `2`: LOW/GND = port 2 is disabled. HIGH/3.3V = port 2 is enabled. NC = port 2 is on

### ALM
* `4`: port 4 ALM pin
* `5`: port 5 ALM pin

![Whitebox T3 port config](/_media/whitebox-t3-port-config.jpg)

?> **Tip with EZO-PMP**: You can use the ALM pin to know whether the pump is currently running or not. Connect the ALM pin to a Raspberry GPIO and read the pin state: if it's HIGH, the pump is running, if it's LOW, the pump is off.
