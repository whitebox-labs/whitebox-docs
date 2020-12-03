# <i class="fas fa-microchip"></i> Pinout

The Whitebox T2 Mini connects to Arduino pins 5V, GND, IOREF, SCL, SDA. No other I/O pins are used.

## Channel 1
* Isolation: **No**
* Footprint: EZO Circuit
* Protocol: `I2C` only
* Probe connector: BNC
* Best suited for:
 * `EZO RTD`
* VCC: `5V`
* I2C: `IOREF`

## Channel 2 + 3

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
* Voltages on the **non-isolated** (Arduino) side:
 * Vcc: `5V `
 * I2C: `IOREF `
* Voltages on the **isolated** (EZO) side:
 * Vcc: `3.9V`
 * I2C: `3.9V`

## Channel 4 + 5
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
 * VCC: `IOREF`
 * I2C: `IOREF`

### Pinout Channel 4 + 5
 ![Tentacle T3](/_media/channels4-5.png)
 * `INT` (Blue): Auxiliary pin used by some EZO devices for interrupts or other function.
 * `3V3` (Red): IOREF
 * `GND` (Black): GND
 * `SDA` (Green): I2C SDA
 * `SCL` (White): I2C SCL
