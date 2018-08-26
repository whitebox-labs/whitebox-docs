1. Set all your circuits to `I2C` mode. [How to switch to I2C](protocols.md)
1. Set all circuits to a unique I2C address - this is important in case you have multiple of the same circuit type, e.g. 2x EZO pH circuit
1. Copy the code below to to your Arduino sketch
1. Adjust the variables in the code to resemble your setup  (see the in-code comments for an explanation on how these work):
 * `TOTAL_CIRCUITS`
 * `channel_ids`
 * `channel_names`
1. Upload the code to your Arduino
1. Open the Arduino IDE serial monitor `@9600 baud`
1. See the stream of data coming in
