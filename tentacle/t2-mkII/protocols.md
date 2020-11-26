# How to switch to I2C

All EZO devices come with two protocols: `UART` and `I2C`. Factory default is `UART`, at a baudrate of `9600`.

?> The Whitebox T2 Mini MkII is compatible with the `I2C` protocol only.

## Distinguish the protocols

[filename](../common/ezo-protocols.md ':include')


## Set Protocol Manually

[filename](../common/ezo-protocols-manually.md ':include')


## Set Protocol With Whitebox I2C Toggler
[I2C Toggler Video](https://www.youtube.com/embed/W-arD9e24OI ':include :type=iframe width=560 height=315')

## Set Protocol By Code

!> On the Whitebox T2 Mini MkII, only the switch from `I2C` to `UART` can be done in code. After the switch to `UART` you can't use the EZO Circuit with the Whitebox T2 until switched back to `I2C` using another method.

[filename](../common/ezo-protocols-code.md ':include')

##  Protocol Lock

[filename](../common/ezo-protocols-lock.md ':include')
