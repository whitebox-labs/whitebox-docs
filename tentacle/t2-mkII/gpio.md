# GPIO

Near the Arduino's digital IO pins there is a row of 4 GPIO:

## ENABLE / DISABLE Channels 2 + 3

To save power, the isolators of channels 2 + 3 can be completely disabled.

To disable a channel, pull the respective pin to LOW. For example, you can connect the pin to an Arduino digital IO pin using a jumper cable. Set the respective pin to LOW to disable the channel. Pull it HIGH to enable it again. All channels are enabled by default.

## AUX for Channels 4+5

EZO Data devices come with an auxiliary pin. Depending of the exact device, this pin can have different functions. For example interrupts, or indicators. The EZO-PMP pulls this line HIGH when pumping, and LOW when not pumping. You can connect this pin to an Arduino digial IO pin to use this information in code.
