# Continuous, Asynchronous Readings

For this project you'll need:
* Arduino
* 1 or 2 Tentacle Mini
* 1-4 Atlas Scientific circuits
* Computer with Arduino IDE installed
* An LED on Arduino pin 13

Often the Arduino should do several things at the same time - reading a pH value and updating a display. Or reading the temperature and sending it to a web API. This code shows how to do several things asynchronously, without waiting and without using `delay()`. This means while we're waiting for new data from the EZO Circuit, the Arduino can do other things during this time. This code demonstrates this using a blinking LED, implemented without wait or delay.

You can find all code mentioned on this page, including a special Arduino Yún version of each sketch on [GitHub](https://github.com/whitebox-labs/tentacle-examples/tree/master/arduino/asynchronous).

?> With the Tentacle Mini, all your EZO Circuits must be in `I2C` mode.

[filename](../common/asynchronous-example-i2c.md ':include')

[](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/asynchronous/i2c_asynchronous/i2c_asynchronous.ino ':include :type=code arduino')

[(View on GitHub)](https://github.com/whitebox-labs/tentacle-examples/blob/master/arduino/asynchronous/i2c_asynchronous/i2c_asynchronous.ino)
