# Frequently Asked Questions

## Did you read the datasheets of your EZO Circuits?
Atlas Scientific has done a great job in documenting their products in beautiful datasheets.

Please download and read the datasheets of your Circuits:

[filename](../common/ezo-datasheets.md ':include')

## My EZO device can't be detected
Try connecting to your sensor circuit after each of these steps:

1. Have you tried the Tentacle Setup sketch from the [Quickstart tutorial](quickstart.md)? There’s a good chance it can auto-detect your circuit.
1. Try a putting your circuit into a different channel slot on the shield
1. [Manually switch](protocols.md#set-protocol-manually) your circuit to the other protocol and back.

## My readings are not correct
[filename](../common/faq-readings-not-correct.md ':include')

## Can I use the Tentacle Mini with another microcontroller (not Arduino)?

Yes. Make sure to check out the [Electronic Specs](power.md).

If you wanted to connect the Mini to a Raspberry Pi, Connect pins

* Tentacle 5V -> RPi 5V
* Tentacle IOREF -> RPi 3.3V
* Tentacle GND -> RPi GND
* Tentacle SCL -> RPi SCL
* Tentacle SDA -> RPi SDA

?> Don't forget to connect the IOREF pin
