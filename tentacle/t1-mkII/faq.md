# <i class="fas fa-question-circle"></i> Frequently Asked Questions

## Did you read the datasheets of your EZO Circuits?
Atlas Scientific has done a great job in documenting their products in beautiful datasheets.

Please download and read the datasheets of your EZO device:

[filename](../common/ezo-datasheets.md ':include')

## My EZO device can't be detected
Try connecting to your EZO device after each of these steps:

1. Have you tried the Whitebox Interactive EZO Console from the [Quickstart tutorial](quickstart.md)? There’s a good chance it can auto-detect your circuit.
1. Try putting your circuit into a different channel on the shield
1. [Manually switch](protocols.md#set-protocol-manually) your device to the other UART and to I2C.

## My readings are not correct
[filename](../common/faq-readings-not-correct.md ':include')

## Can I use the Whitebox T1 with another microcontroller (not Arduino)?

Yes. Make sure to check out the [Electronic Specs](power.md).

?> Don't forget to connect the IOREF pin
