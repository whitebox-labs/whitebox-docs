# <i class="fas fa-microchip"></i> Pinout

The Whitebox T1 connects to Arduino pins GND, IOREF, SCL, SDA. No other I/O pins are used.

## Port 1
* Isolation: **No**
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe connection: SMA (female)
* Best suited for:
 * `EZO RTD`
* VCC: `5V` (power: EXTERNAL) | `IOREF` (power: ARDUINO)
* I2C: `IOREF`

## Ports 2 - 5

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
* Voltages on the **non-isolated** (Arduino) side:
* VCC: `5V` (power: EXTERNAL) | `IOREF` (power: ARDUINO)
* I2C: `IOREF`
* Voltages on the **isolated** (EZO) side:
 * Vcc: `3.9V`
 * I2C: `3.9V`

## Ports 6 - 9
 * Isolation: **No**
 * Footprint: EZO Data Connector
 * Protocol: `I2C` only
 * Best suited for:
  * `EZO CO2` Embedded NDIR CO2 Sensor
  * `EZO O2` Embedded Oxygen Sensor
  * `EZO HUM` Embedded Humidity sensor
  * `EZO PRS` Embedded Pressure Sensor
  * `EZO PMP` Embedded Dosing Pump
  * `EZO RGB` Embedded Color Sensor
  * 3rd-party I2C devices like the I2C Soil Moisture Sensor
* VCC: `5V` (power: EXTERNAL) | `IOREF` (power: ARDUINO)
* I2C: `IOREF`

### Pinout Channel 6 - 9
 * `AUX` (Blue): ALM pin used by some EZO devices for alarm functions.
 * `VCC` (Red): 5V
 * `GND` (Black): GND
 * `SDA` (Green): I2C SDA
 * `SCL` (White): I2C SCL


## Configuration pins
Connect port configuration pins to your circuits or Arduino GPIO pins.


### Disable
The isolators in ports 2 - 5 can be disabled. If disabled, the EZO circuit is cut from power.
* `2`: LOW/GND = port 2 is disabled. HIGH/3.3V = port 2 is enabled. NC = port 2 is on
* `3`: LOW/GND = port 3 is disabled. HIGH/3.3V = port 3 is enabled. NC = port 3 is on
* `4`: LOW/GND = port 4 is disabled. HIGH/3.3V = port 4 is enabled. NC = port 4 is on
* `5`: LOW/GND = port 5 is disabled. HIGH/3.3V = port 5 is enabled. NC = port 5 is on

### AUX
* `6`: port 2 AUX pin
* `7`: port 3 AUX pin
* `8`: port 4 AUX pin
* `9`: port 5 AUX pin

![Whitebox T1 port config](/_media/whitebox-t1-config.jpg)

?> **Tip with EZO-PMP**: You can use the ALM pin to know whether the pump is currently running or not. Connect the ALM pin to a Raspberry GPIO and read the pin state: if it's HIGH, the pump is running, if it's LOW, the pump is off.
