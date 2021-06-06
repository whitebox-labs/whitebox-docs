# <i class="fas fa-exchange-alt"></i> GPIO

Near the Arduino's digital I/O pins there is a row of 4 GPIO pins. You can use simple jumper cables to patch these pins to your Arduino's digital I/O pins.
 ![Whitebox T2 ch 4+5](/_media/gpio.jpeg)


## ENABLE / DISABLE Channels 2 + 3

To save power, the isolators and EZO circuits of channels 2 + 3 can be completely disabled.

* `ENABLE 3` Pull this pin low disable channel 3
* `ENABLE 2` Pull this pin low disable channel 2

Connect the pin to an Arduino digital I/O pin using a jumper cable. Set the respective pin to LOW to disable the channel. Pull it HIGH to enable it again. All channels are enabled by default.

## AUX for Channels 4+5

* `INT 4` This pin is connected to the "INT" or "ALM" pin of the EZO device on channel 4
* `INT 5` This pin is connected to the "INT" or "ALM" pin of the EZO device on channel 5

EZO Data devices come with an ALM pin. EZO devices can indicate states and alarms on this pin. For example, the EZO-PMP pulls this line HIGH when pumping, and LOW when not pumping. You can connect this pin to an Arduino digital I/O pin to use this information in code.
