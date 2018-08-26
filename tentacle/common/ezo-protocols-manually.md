This procedure toggles the protocol between `UART` and `I2C`. If the EZO Circuit is in `UART` mode, this procedure will switch it to `I2C`. If it is in `I2C` mode, it will switch it to `UART`.

!> Before starting the procedure, remove the EZO Circuit from the Tentacle (or other carrier boards). Remove power and all connections.

?> This procedure is easiest using a breadboard and a set of jumper wires

1. Connect (shortcut) these two pins:
 * **PGND pin to the TX pin** if your circuit is `EZO pH`, `EZO DO`, `EZO ORP` or `EZO EC`
 * Only exception is `EZO RTD`: Short the **PRB pin to the TX pin** instead.
1. Power the EZO Circuit (GND, +5V)
 * Wait for LED to change from green to blue (`UART`->`I2C`) or from blue to green (`I2C`->`UART`).
 ![EZO Manual Toggle](_media/manual_toggle.png)
 _(The Arduino is used as a power source only. You can connect any other power source (3.3V-5V))_
1. **Remove** the jumper wire from the PGND (or PRB respectively) pin to the TX pin
1. **Remove** power (GND, 5V)

?> The device is now using the new protocol (repeat above steps to toggle back to the other protocol)

### Factory defaults
If the EZO Circuit is manually switched to `I2C`, its ID is reset to the factory default:

* `EZO DO`: **97** _(0x60)_
* `EZO ORP`: **98** _(0x61)_
* `EZO pH`: **99** _(0x63)_
* `EZO EC`: **100** _(0x64)_
* `EZO RTD`: **102** _(0x66)_

If the EZO Circuit is manually switched to `UART`, its baudrate is reset to the factory default of `9600`.
