# Power

## 5V only
* The Tentacle for Arduino is powered solely from the Arduino 5V line.
* The isolated communication lines (RX/TX, SCL/SDA) are pulled to 5V - ** use a 5V-tolerant Arduino** (most are)
* The EZO circuits on the isolated side are powered by 5V.

## Schematic
* [Download Schematic (PDF)](https://github.com/whitebox-labs/tentacle/raw/master/hardware/tentacle_schematic.pdf)
* [All Source Files (GitHub)](https://github.com/whitebox-labs/tentacle/)

## Power Consumption
* ~140mA @ 5V
 * (~35mA per isolated channel)

**Add the consumption of each of your EZO Circuits**

max. power @5V:

[filename](../common/ezo-power-consumption.md ':include')
