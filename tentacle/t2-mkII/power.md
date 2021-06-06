# <i class="fas fa-bolt"></i> Power



## Power Consumption
* ~70mA @ 5V
 * (that's ~35mA per channel)

**Add the consumption of each of your EZO Circuits**

max. power @5V:

[filename](../common/ezo-power-consumption.md ':include')

## Two power rails
If you’re using a standard Arduino, you don’t need to worry about this, because **it just works**.

If you're using the Whitebox T2 Mini on a non-Arduino microcontroller (or mount it in a non-standard way), you have to power two separate power rails:

### 5V rail
The 5V-rail is used to power the Whitebox T0 isolators. Most Arduinos will provide the expected 5V from the 5V pin.

!> 5V must be applied to the 5V pin. _every Arduino will do this for you automatically_

### IOREF rail
The IO-reference voltage pin of an Arduino is either 3.3V or 5V, depending on the Arduino model. It's the voltage that this particular Arduino expects at its I/O pins. The Whitebox T2 Mini uses this voltage to power the isolated I2C lines and the SCL/SDA pins.

!> A voltage of 3.3V or 5V must be applied to the IOREF pin. _every Arduino will do this for you automatically_

## Schematic
* <i class="far fa-file-pdf"></i> [Schematic](https://github.com/whitebox-labs/whitebox-t2-oshw/raw/main/whitebox-t2-mkII-schematic.pdf)
* <i class="fab fa-github"></i> [Hardware source files on GitHub](https://github.com/whitebox-labs/whitebox-t2-oshw)
