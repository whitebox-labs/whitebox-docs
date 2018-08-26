# EZO Circuit Protocols

Most EZO Circuits come with two protocols: `UART` and `I2C`. Factory default is `UART`, at a baudrate of `9600`.


## Distinguish the protocols

[filename](../common/ezo-protocols.md ':include')



## Set Protocol Manually

[filename](../common/ezo-protocols-manually.md ':include')

## Set Protocol With Whitebox I2C Toggler

## Set Protocol By Code

[filename](../common/ezo-protocols-code.md ':include')

### Using the Tentacle for Arduino and the Setup Sketch
1. Load the [Tentacle Setup Sketch](https://raw.githubusercontent.com/whitebox-labs/tentacle-examples/master/arduino/tentacle-setup/tentacle_setup/tentacle_setup.ino ':target=_blank') to your Arduino
1. open the serial monitor `@9600`
1. Type the ID of the circuit and press enter. Try ‘scan’, if you don’t know the ID of your circuit.
 * to switch to `I2C` mode, type `i2c,111`
 * to switch to `UART` mode, type `baud,9600`
1. Change both `protocol jumpers` for this channel to the new protocol
1. you are able to connect to the new channel ID immediately, no need  to restart the Arduino



##  Protocol Lock (Plock)

[filename](../common/ezo-protocols-lock.md ':include')
