# Continuously read multiple sensors

For this project you'll need:
* Arduino
* 1 or 2 Whitebox T2
* 2 or more Atlas Scientific circuits
* Computer with Arduino IDE installed

?> With the Whitebox T2, all your EZO Circuits must be in `I2C` mode.

1. Set all your circuits to `I2C` mode. [How to switch to I2C](protocols.md)
1. Set all circuits to a unique I2C address - this is important in case you have multiples of the same circuit type, like 2x EZO pH circuits
1. Download the [<i class="fas fa-cube"></i>EZO I2C Lib](https://github.com/Atlas-Scientific/Ezo_I2c_lib/archive/master.zip)
1. Install the EZO I2C library by adding it via Arduino IDE -> Sketch -> Include Library -> Add .ZIP Library...
1. Copy the code below to to your Arduino sketch
1. The example code assumes an EZO pH and an EZO RTD circuit. Adjust the I2C addresses and names if you have different EZO devices
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. See the stream of data coming in

[](https://raw.githubusercontent.com/whitebox-labs/whitebox-arduino-example-code/main/continuous/continuous.ino ':include :type=code arduino')

[<i class="fab fa-github"></i> View on GitHub](https://raw.githubusercontent.com/whitebox-labs/whitebox-arduino-example-code/main/continuous/continuous.ino)
