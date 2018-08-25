# Frequently Asked Questions

## Did you read the datasheets of your EZO Circuits?
Atlas Scientific has done an incredible job in creating comprehensive and beautiful datasheets that are easy to understand.

Please download and read the datasheets of your Circuits:

[filename](ezo-datasheets.md ':include')

## My Circutit cant' be detected
Try connecting to your sensor circuit after each of these steps:

1. Have you tried the Tentacle Setup sketch from the [Quickstart tutorial](quickstart.md)? There’s a good chance it can auto-detect your circuit.
1. Check if your Jumper Settings are correct. Set them to `serial` if the LED is green. If the LED is blue, set them to `I2C`. Also see [Jumper Settings](jumpers.md)
1. Try a putting your circuit into a different channel slot on the shield
1. [Manually switch](protocols.md#set-protocol-manually) your circuit to the other protocol and back.

## My readings are not correct

1. Use the [Tentacle Setup Sketch](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/tentacle-setup/tentacle_setup/tentacle_setup.ino ':target=_blank') to calibrate your circuit, following the procedure described in the circuits datasheet.
1. Don’t touch the Atlas Scientific circuits, the Tentacle Shield and the metal BNC connectors. Touching these can make the readings inaccurate for several minutes. Wait a moment and see if the issue persists.
1. The first couple of readings are inaccurate after waking the circuits from sleep. This is an expected behaviour of some Atlas Scientific devices and you should account for it in your code.
1. Make sure your probe is clean and in good condition. If your probe is dirty, check the probes datasheet to learn how to clean your probe.
1. Use good quality probes.
1. Ensure that the Tentacle Shield solder joints are free of dirt, dust, humps of flux residue. This is most important around the BNC connectors and the pin headers for the circuits, top and bottom side. Make sure the Arduino and Tentacle Shield don’t touch anything conductive.
1. Read the troubleshooting sections of your circuits datasheet
