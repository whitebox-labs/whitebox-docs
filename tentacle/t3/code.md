# <i class="fas fa-code"></i> Code

Download the Atlas Scientifics I2C example for Raspberry Pi. It gives you an console to interact with all attached EZO devices:

https://github.com/AtlasScientific/Raspberry-Pi-sample-code

or get the complete (incl USB etc) documentation: `git clone https://github.com/AtlasScientific/Raspberry-Pi-sample-code.git`

With the Tentacle T3 for Raspberry Pi, only the `I2C` part of the above repository is relevant. Run the I2C code:

```
sudo python i2c.py
```

You’ll be presented with an interactive console:

![raspi-config](_media/i2c-py.png)

To list attached EZO devices, type:

```
List_addr
```

**Factroy default addresses**
* `EZO DO`: **97** _(0x61)_
* `EZO ORP`: **98** _(0x62)_
* `EZO pH`: **99** _(0x63)_
* `EZO EC`: **100** _(0x64)_
* `EZO RTD`: **102** _(0x66)_
* `EZO PMP`: **103** _(0x67)_

To directly connect to a certain circuit, type `ADDRESS,xx` (xx is the address of the circuit):

```
ADDRESS,99
```

You’re now connected to the circuit at address `99`. To take a reading, type `r`. To get information about the circuit, type `i`.

Grab the datasheet of your circuit and try out some other commands:

[filename](../common/ezo-datasheets.md ':include')


To continuously poll the reading of a circuit, use the command `Poll`. Its parameter is the polling frequency - here 1.5 seconds:

```
Poll,1.50
```

## 3rd-party Code
### Python 3
Thanks to Jef Roosens for translating the example code to Python 3!

https://github.com/OriginalJef/AtlasScientificI2C
