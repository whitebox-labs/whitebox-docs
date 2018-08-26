# How to switch to I2C

Most EZO Circuits come with two protocols: `UART` and `I2C`. Factory default is `UART`, at a baudrate of `9600`.

?> The Tentacle Mini is compatible with the `I2C` protocol only.

## Distinguish the protocols

[filename](../common/ezo-protocols.md ':include')


## Set Protocol Manually

[filename](../common/ezo-protocols-manually.md ':include')


## Set Protocol With Whitebox I2C Toggler
_(coming soon)_

## Set Protocol By Code

!> On the Tentacle Mini, only the switch from `I2C` to `UART` can be done in code. After the switch to `UART` you can't use the EZO Circuit with the Tentacle Mini until switched back to `I2C` using another method.

[filename](../common/ezo-protocols-code.md ':include')

##  Protocol Lock

[filename](../common/ezo-protocols-lock.md ':include')
