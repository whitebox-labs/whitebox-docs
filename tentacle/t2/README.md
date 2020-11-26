# LEGACY <!-- {docsify-ignore} -->

The Tentacle Mini has been discontinued in 2020 and was replaced by the [Whitebox T2 Mini MkII](https://www.whiteboxes.ch/docs/tentacle/t2-mkII/)

This documentation will remain online. We'll continue support for the Tetnacle Mini.  

# Introduction

This documentation is for **Tentacle Mini for Arduino**, model `T2.16` (disconinued)



![Tentacle Mini](/_media/tentacle-t2.jpg)

_Atlas Scientific EZO-class devices are not included_

<small>Made by</small>

![Whitebox Logo](_media/whitebox_logo.png)

## What's the Tentacle Mini?
An Arduino shield to host and individually isolate up to 2 sensor circuits from [Atlas Scientific](https://www.atlas-scientific.com) to measure PH, Dissolved Oxygen, Electric Conductivity (E.C.) and Oxidation-Reduction Potential (ORP), RTD (Temperature).

* 2 fully isolated channels for _Atlas Scientific EZO Circuits_
* `3.3V` and `5V` compatible
* `I2C` only
* stackable

?> **Built in electrical isolation** means that sensors won’t interfere with each other. It also removes outside electrical noise that can interfere with readings.

_Works with_

![Arduino Atlas Logo](_media/designed-for-arduino-atlas.png)

## Getting Started
* [Quick Start Tutorial](quickstart.md)
* [How to switch EZO Circuits to I2C](protocols.md)

## Code Examples
* [Continuous Readings](continuous-example.md)
* [Continuous, Asynchronous Readings](asynchronous-example.md)
* [Interactive, Bidirectional Communications](interactive-example.md)
* [Download all examples (zip)](https://github.com/whitebox-labs/tentacle-examples/archive/master.zip)
* [Examples repository on GitHub](https://github.com/whitebox-labs/tentacle-examples)
`git clone https://github.com/whitebox-labs/tentacle-examples.git`


## Downloads
* [Tentacle Setup Sketch](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/tentacle-setup/tentacle_setup/tentacle_setup.ino ':target=_blank')
* [T2.16 Mechanical Drawing (PDF)](https://github.com/whitebox-labs/tentacle-mini-oshw/raw/master/hardware/mechanical/tentacle_t2_mechanical.pdf)
* [BNC Connector Mechanical Drawing (PDF)](https://github.com/whitebox-labs/tentacle/raw/master/hardware/mechanical/bnc_mechanical.pdf)
* [T2.16 Schematic (PDF)](https://github.com/whitebox-labs/tentacle-mini-oshw/raw/master/hardware/T2_mini_schematic.pdf)
* [T2.16 3D-Model (STL)](https://github.com/whitebox-labs/tentacle-mini-oshw/raw/master/hardware/mechanical/tentacle_t2.STL) ([view online](https://github.com/whitebox-labs/tentacle-mini-oshw/blob/master/hardware/mechanical/tentacle_t2.STL))
* [T2.16 3D-Model (STEP)](https://github.com/whitebox-labs/tentacle-mini-oshw/raw/master/hardware/mechanical/tentacle_t2.STEP.zip)

## Support
For customer support, please use the [contact form](https://www.whiteboxes.ch/contact/) on our website.

If you find bug in the documentation, examples or the schematic, feel free to create an issue or even a pull request here on GitHub.


## Open Source
The Tentacle Shield is [certified](http://certificate.oshwa.org/certification-directory/) Open Source Hardware with UID CH000002. Schematics and layout are licensed under [Creative Commons BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/). Silkscreen graphics and the trade mark “Tentacle” are intellectual property of Whitebox Labs

* [Hardware source files on GitHub](https://github.com/whitebox-labs/tentacle-mini-oshw) `git clone https://github.com/whitebox-labs/tentacle-mini-oswh.git`

Made with [![KiCAD logo](_media/kicad_logo_small.png)](http://kicad-pcb.org/)

## Buy
* From [our store](https://www.whiteboxes.ch/shop/tentacle-mini/) – we ship worldwide
* or from one of our [Distributors](https://www.whiteboxes.ch/distributors)

*Made in Switzerland* ![Switzerland](_media/its-flag-is-a-big-plus.png)
