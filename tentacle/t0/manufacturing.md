
# <i class="fas fa-industry"></i> Manufacturing <!-- {docsify-ignore} -->

## Assembly
* Coming soon

## Soldering
* Coming soon

## High Impedance Shorts
Flux residue on the PCB can create high impedance shorts, making accurate readings impossible. Signs of a high impedance short are locked values to a certain value, slowly drifting values even in calibration solution and others.

Flux residue should be removed - especially if you can measure a short with the technique described below. Remove the flux with a flux remover chemical matching the solder you use. Alternatively soak the board 20mins in alcohol.


## Testing
The most important test after assembly is to find high impedance shorts. The pins sensitive to these shorts are
* Pin 8 (GND_ISO)
* Pin 9 (PRB_GND)
* Pin 10 (PRB)
* Pin 11 (PRB_GND)

Test Pin 9 against Pin 10 and Pin 9 against Pin 8. If either test fails, clean the T0 solder points from flux residue, grease, etc.

### Testing procedure

A simple way to find high impedance shorts is by applying a voltage across the the two pins with inline a voltmeter. Your voltmeter should read less than 1mV for the test to pass.a 9V battery (or any other 9V power source). Apply the voltage across the 2 signals you want to test and inline a Voltmeter in the mV setting.

* isolate the device under test on a silicone mat or any other non-conductive surface. The test setup must be isolated from your antistatic mat.
* Use a 9V battery or other 9V power source - connect the positive battery pole (+) to Pin A
* Connect the positive test lead (red) of your voltmeter to Pin B
* Connect the negative (black) test lead of your voltmeter to the negative Battery pole (-).

If your Voltmeter can detect a voltage >1mV, there is a high impedance short that can prevent good sensor readings. Remove fingerprints, dust, solder flux residue from the respective pad and pins.

## Re-usable Component Tray
We provide a set of wooden, re-usable trays to be used in pick & place machines to OEM customers.

The tray pictured below is for 54 T0s, measures 135mm x 224mm. We can adapt the size of the tray to your machine and production workflow.
![Re-usable tray](_media/whitebox-t0-tray.jpg)
