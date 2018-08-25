# Frequently Asked Questions

## Did you read the datasheets of your EZO Circuits?
[filename](../common/faq-ezo-datasheets.md ':include')
.
[filename](../common/ezo-datasheets.md ':include')

## My Circutit cant' be detected
Try connecting to your sensor circuit after each of these steps:

1. Have you tried the Tentacle Setup sketch from the [Quickstart tutorial](quickstart.md)? There’s a good chance it can auto-detect your circuit.
1. Check if your Jumper Settings are correct. Set them to `serial` if the LED is green. If the LED is blue, set them to `I2C`. Also see [Jumper Settings](jumpers.md)
1. Try a putting your circuit into a different channel slot on the shield
1. [Manually switch](protocols.md#set-protocol-manually) your circuit to the other protocol and back.

## My readings are not correct
[filename](../common/faq-readings-not-correct.md ':include')
