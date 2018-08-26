1. Set all your circuits to `I2C` mode. [How to switch EZO Circuits to I2C](switch-to-i2c.md)
1. Set all circuits to a unique I2C address - this is important in case you have multiple of the same circuit type, e.g. 2x EZO pH circuit
1. Copy the code below to to your Arduino sketch
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. Type the channel number, a colon and the command into the serial monitor like so:
`99:r` or `99:i`
