# Continuous Readings

For this project you'll need:
* Arduino, 5V tolerant
* 1 or 2 Tentacle Shield(s)
* 1-8 Atlas Scientific circuits
* Computer with Arduino IDE installed

You can find all code mentioned on this page, including a special Arduino Yún version of each sketch on [GitHub](https://github.com/whitebox-labs/tentacle-examples/tree/master/arduino).


## UART mode
1. Set all your circuits to `UART` mode. This is the circuits factory setting.
1. Copy the code below to to your Arduino sketch
1. Adjust the variables in the code to resemble your setup (see the in-code comments for an explanation on how these work):
 * `TOTAL_CIRCUITS`
 * `channel_ids`
 * `channel_names`
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. See the stream of data coming in

[](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/continuous/uart_continuous/uart_continuous.ino ':include :type=code arduino')

[(View on GitHub)](https://github.com/whitebox-labs/tentacle-examples/blob/master/arduino/continuous/uart_continuous/uart_continuous.ino)

## I2C mode

[filename](../common/continuous-example-i2c.md ':include')

[](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/continuous/i2c_continuous/i2c_continuous.ino ':include :type=code arduino')

[(View on GitHub)](https://github.com/whitebox-labs/tentacle-examples/blob/master/arduino/continuous/i2c_continuous/i2c_continuous.ino)
