
# <i class="fas fa-power-off"></i> Enable / disable <!-- {docsify-ignore} -->

The EN pin turns the power and signal isolators on and off. The EN pin is compatible with standard GPIO logic threshold. It can
be used with any microcontroller with 2.5-V, 3.3-V, or 5.5-V GPIO.

* EN pin HIGH = T0 is on
* EN pin LOW = T0 is off

**Don't leave EN floating**

Turning the T0 off will cut power to the attached EZO Circuit.
