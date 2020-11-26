
To switch to `I2C`, use the command `i2c`:
```
i2c,111
```
111 is the new I2C address of the circuit. It can be 1-127 and must be unique on the same `I2C` bus.

To switch to `UART`, use the command `baud`:
```
baud,9600
```
9600 is the UART baudrate (can be: 300, 1200, 2400, 9600 _(default)_, 19200, 38400, 57600, 115200)

!> After changing the protocol, the microcontroller will lose connection EZO Circuit - due to the different nature of `UART` and `I2C` busses.  
