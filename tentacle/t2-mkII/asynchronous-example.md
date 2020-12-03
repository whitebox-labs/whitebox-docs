# <i class="fas fa-code"></i> Continuous, Asynchronous Readings

Often the Arduino should do several things at the same time - reading a pH value and updating a display. Or reading the temperature and sending it to a web API.

This example shows how to do several things asynchronously, without waiting and without using `delay()`. This means while waiting for new data from the EZO Circuit, the Arduino can do other things. In this example we're blinking a LED, implemented without wait or delay.

For this project you'll need:
* Arduino
* 1 or 2 Whitebox T2 Mini
* 1-6 Atlas Scientific EZO devices
* Computer with Arduino IDE installed
* An LED on Arduino pin 13
* Installed [<i class="fas fa-file-download"></i> EZO I2C Library](https://github.com/Atlas-Scientific/Ezo_I2c_lib/archive/master.zip)


## Install the EZO I2C Library
[filename](../common/install-ezo-i2c-lib.md ':include')

## Run the code
?> With the Whitebox T2, all your EZO Circuits must be in `I2C` mode.

1. Make sure all your EZO devices are in `I2C` mode. [How to switch to I2C](protocols.md)
1. Copy the code below to to your Arduino sketch
1. The example code assumes an EZO pH and an EZO RTD circuit. Adjust the I2C addresses and names if you have different EZO devices
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. See the stream of data coming in

[](https://raw.githubusercontent.com/whitebox-labs/whitebox-arduino-example-code/main/asynchronous/asynchronous.ino ':include :type=code arduino')

[<i class="fab fa-github"></i> View on GitHub](https://github.com/whitebox-labs/whitebox-arduino-example-code/blob/main/asynchronous/asynchronous.ino)
