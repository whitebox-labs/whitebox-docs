# <i class="fas fa-code"></i> Temperature Compensation

For this project you need:
* Arduino
* 1 or 2 Whitebox T2
* EZO RTD Temperature Circuit + EZO pH Circuit
* Computer with Arduino IDE installed
* Installed [<i class="fas fa-file-download"></i> EZO I2C Library](https://github.com/Atlas-Scientific/Ezo_I2c_lib/archive/master.zip)

## Install the EZO I2C Library
1. Download the [<i class="fas fa-file-download"></i> EZO I2C Library](https://github.com/Atlas-Scientific/Ezo_I2c_lib/archive/master.zip)
1. Install the EZO I2C library by adding it via Arduino IDE -> Sketch -> Include Library -> Add .ZIP Library...

## Run the code
?> With the Whitebox T2, all your EZO Circuits must be in `I2C` mode.

1. Make sure all your EZO devices are in `I2C` mode. [How to switch to I2C](protocols.md)
1. Copy the code below to to your Arduino sketch
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. See the stream of data coming in

[](https://raw.githubusercontent.com/whitebox-labs/whitebox-arduino-example-code/main/temperature-compensation/temperature-compensation.ino ':include :type=code arduino')

[<i class="fab fa-github"></i> View on GitHub](https://github.com/whitebox-labs/whitebox-arduino-example-code/blob/main/temperature-compensation/temperature-compensation.ino)
