# <i class="fas fa-question-circle"></i> Frequently Asked Questions

## Did you read the datasheets of your EZO Circuits?
Atlas Scientific has done a great job in documenting their products in beautiful datasheets.

Please download and read the datasheets of your Circuits:

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-datasheets.md ':include')

## Can the Tentacle T3 be stacked?
Yes, we designed the T3 specifically for stacking. You can stack other HATs or pHats on top of the Tentacle T3 - even those that normally don't support stacking. The Tentacle T3 has a stackable header, just like your Pi. The Tentacle only uses the `I2C` and power pins, so it’s very unlikely to interfere with other HATs.

You can also stack two Tentacle T3 to the same Raspberry Pi. Make sure you select [a suitable power supply](power.md#select-a-suitable-power-supply).

## My Circutit cant' be detected
Is your EZO circuit in I2C mode? It should have a blue light. If it has a green light, flashing to Cyan every second, your EZO circuit is still in UART mode. You have to switch it to I2C before it can be detected with the Tentacle T3. * [How to switch EZO Circuits to I2C](protocols.md)

## My readings are not correct
[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/faq-readings-not-correct.md ':include')
