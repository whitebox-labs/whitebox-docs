# <i class="fas fa-bolt"></i> Power

## Schematic
* <i class="far fa-file-pdf"></i> Schematic
* <i class="fab fa-github"></i> All Source Files on GitHub

## Power Consumption

To estimate the total power consumption of your setup, **add the consumption of each of your EZO Circuits**

On the Whitebox T5, the EZO devices are powered by the Pi's `3.3V` line. Make sure the total power consumption does not exceed the cabability of your Pi's on-board 3.3V power supply.

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-power-consumption.md ':include')

### Estimate power consumption
Let's assume we have an `EZO pH` circuit and an `EZO RTD`. We can estimate the total power consumption like this:

| Device      	| Ch# 	| Voltage 	| Max Power	| Standby 	| Sleep   	|
|:-------------	|-----------	|---------	|---------:	|---------:	|--------:	|
| `Whitebox T5`	|           	| 3.3V     	|   35mA 	| 35mA  	| 35mA  	|
| `EZO pH`    	| 1         	| 3.3V     	| 18.3mA 	| 16.0mA 	| 1.16mA 	|
| `EZO RTD`   	| 2         	| 3.3V    	| 15.4mA 	| 14.3mA 	| 0.4mA 	|
|             	|           	|         	|         	|         	|         	|
| **Total**   	|           	|         	| **68.7mA** 	| **65.3mA**  	| **36.56mA**  	|

!> This is an estimation. Numbers in reality will vary.

### Select a suitable power supply
To make the Whitebox T5 and the EZO devices work well, they must be properly powered. A junky or under-powered power supply will ruin your day <i class="fas fa-skull"></i> .

?> We recommend to power your Pi-T5 stack using a dedicated power supply (_not from a computer USB port_)

To find a suitable power supply for your Pi-T3 stack, you need to add all other devices in the setup:
* Raspberry Pi power consumption
 * Raspberry Pi 3 B+ under full load: **980mA**
  * [Official Raspberry Pi Documentation: Power Supply](https://www.raspberrypi.org/documentation/computers/raspberry-pi.html#power-supply)
  * [Raspberry Pi Power Consumption Benchmarks](https://www.pidramble.com/wiki/benchmarks/power-consumption)
* Other boards / HATs
* Peripherals - Displays, SSDs, etc.

Using the numbers from our example estimation above, peak can be _68.7mA + 980mA =_ **1048.7mA**.

* As a safety margin, we recommend to double the estimate mA to get to the required power supply wattage  _1048.7mA *2 =_ 2314mA  = **2097.4mA**
* In this example, a standard **5V 2.5A** DC power supply is suitable. Buy it from a well known supplier  - and your day is saved <i class="fas fa-thumbs-up"></i>.
