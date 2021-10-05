# <i class="fas fa-code-branch"></i> How to switch to I2C

All EZO devices come with two protocols: `UART` and `I2C`. Factory default is `UART`, at a baudrate of `9600`.

?> The Whitebox T1 is compatible with the `I2C` protocol only.

## Distinguish the protocols

[filename](../common/ezo-protocols.md ':include')


## Set Protocol With Whitebox I2C Toggler

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols-toggler.md ':include')


## Set Protocol Manually

[filename](../common/ezo-protocols-manually.md ':include')


## Set Protocol By Code

!> On the Whitebox T1, you can only switch from `I2C` to `UART` in code, but not back to `I2C`. After the switch to `UART` you can't use the EZO Circuit with the Whitebox T1 until switched back to `I2C` using another method.

[filename](../common/ezo-protocols-code.md ':include')

##  Protocol Lock

[filename](../common/ezo-protocols-lock.md ':include')
