
1. Use the [Whitebox Interactive EZO Console](https://github.com/whitebox-labs/whitebox-ezo-console/archive/main.zip ':target=_blank')
 to calibrate your circuit, following the procedure described in the circuits datasheet.
1. Don’t touch the Atlas Scientific EZO device, the carrier board and the metal BNC/SMA connectors. Touching these can make the readings inaccurate for several minutes. Wait a moment and see if the issue persists.
1. The first couple of readings are inaccurate after waking the circuits from sleep. This is an expected behaviour of some Atlas Scientific devices and you should account for it in your code.
1. Make sure your probe is clean and in good condition. If your probe is dirty, check the probes datasheet to learn how to clean your probe.
1. Use good quality probes.
1. Ensure that the Whitebox T(x) boards solder joints are free of dirt, dust, humps of flux residue. This is most important around the BNC or SMA connectors and the pin headers for the EZO circuits, top and bottom side. Make sure the Arduino does not touch anything conductive. Note that antistatic mats are conductive. Don't place your Arduino directly on it.
1. Read the troubleshooting sections of your EZO devices datasheet
