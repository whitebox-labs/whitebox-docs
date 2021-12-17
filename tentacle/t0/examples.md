
# <i class="fas fa-code-branch"></i> Application Examples <!-- {docsify-ignore} -->

## Minimal Circuit
The operating voltage is applied to VIN, VSIG and EN to fully power up the T0.
![Minimal Example Schematic](_media/whitebox-t0-minimal-circuit.svg)

## Enable Functionality
By pulling the EN pin HIGH or LOW, the T0 can be powered on and off using the microcontrollers GPIO. This example also implements a power indication LED.
![Enable Example Schematic](_media/whitebox-t0-enable-circuit.svg)

## Mixed Voltages
The T0 can have different voltage supplies for the signal and power isolator. This is useful in mixed 3.3V/5V setups or when the MCU internal regulator can not provide enough power for the (potentially many) power isolators. VSIG must be lower than or equal to VIN.

* VSIG powers the signal isolator and is the I/O reference voltage that defines I2C voltage levels
* VIN powers the power isolator.

![Mixed Voltages Schematic](_media/whitebox-t0-voltages-circuit.svg)
