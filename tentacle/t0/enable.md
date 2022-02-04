
# <i class="fas fa-power-off"></i> Enable / disable <!-- {docsify-ignore} -->

The EN pin controls the T0 power state to switch it on and off. The EN pin is compatible with standard GPIO logic thresholds and can be used with any microcontroller with 3.3-V, or 5.5-V GPIO.

* EN pin HIGH = T0 is on
* EN pin LOW = T0 is off

**Don't leave EN floating**

If your design allows user control of the enable pin, it's advisable to use a 1M pull-up or pull-down resistor to make sure EN isn't left floating.

Turning the T0 off will cut power to the attached EZO Circuit.
