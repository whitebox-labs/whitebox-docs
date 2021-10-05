# <i class="fas fa-bolt"></i> Power

## Schematic
* <i class="far fa-file-pdf"></i> Schematic
* <i class="fab fa-github"></i> All Source Files on GitHub

## Power Consumption

To estimate the total power consumption of your setup, **add the consumption of each of your EZO Circuits**

On the Whitebox T3, the EZO devices are powered either by `3.3V` or `5V`. The voltage depends on which port is used. See [Pinout](pinout.md) for all port information.

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-power-consumption.md ':include')

### Estimate power consumption
Let's assume we have an `EZO pH` circuit, an `EZO Conductivity` circuit, an `EZO RTD` circuit and two `EZO PMP` dosing pumps. We can estimate the total power consumption like this:

| Device      	| Ch# 	| Voltage 	| Max Power	| Standby 	| Sleep   	|
|:-------------	|-----------	|---------	|---------:	|---------:	|--------:	|
| `Whitebox T3`	|           	| 5V      	|   70mA 	| 70mA  	| 70mA  	|
| `EZO pH`    	| 1         	| 5V      	| 18.3mA 	| 16.0mA 	| 1.16mA 	|
| `EZO Conductivity`	| 2   	| 5V      	| 50.0mA 	| 18.2mA	| 0.7mA 	|
| `EZO RTD`   	| 3         	| 3.3V    	| 14.3mA 	| 15.4mA 	| 0.4mA 	|
| `EZO PMP`   	| 4         	| 3.3V    	| 12.5mA 	| 12.4mA 	| 0.13mA 	|
| `EZO PMP`   	| 5         	| 3.3V    	| 12.5mA 	| 12.4mA 	| 0.13mA 	|
|             	|           	|         	|         	|         	|         	|
| **Total**   	|           	|         	| **177.6mA** 	| **144.4mA**  	| **72.52mA**  	|

!> This is an estimation. Numbers in reality will vary.

### Select a suitable power supply
To make the Whitebox T3 and the EZO devices work well, they must be properly powered. A junky or under-powered power supply will ruin your day <i class="fas fa-skull"></i> .

?> We recommend to power your Pi-T3 stack using a dedicated power supply (_not from a computer USB port_)

To find a suitable power supply for your Pi-T3 stack, you need to add all other devices in the setup:
* Raspberry Pi power consumption
 * Raspberry Pi 3 B+ under full load: **980mA**
  * [Official Raspberry Pi Documentation: Power Supply](https://www.raspberrypi.org/documentation/computers/raspberry-pi.html#power-supply)
  * [Raspberry Pi Power Consumption Benchmarks](https://www.pidramble.com/wiki/benchmarks/power-consumption)
* Other boards / HATs
* Peripherals - Displays, SSDs, etc.

Using the numbers from our example estimation above, peak can be _177mA + 980mA =_ **1157mA**.

* As a safety margin, we recommend to double the estimate mA to get to the required power supply wattage  _1157mA *2 =_ 2314mA  = **2.314A**
* In this example, a standard **5V 2.5A** DC power supply is suitable. Buy it from a well known supplier  - and your day is saved <i class="fas fa-thumbs-up"></i>.
