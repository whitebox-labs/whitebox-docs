# <i class="fas fa-code-branch"></i> How to switch to I2C

Most EZO Circuits come with two protocols: `UART` and `I2C`. Factory default is `UART`, at a baudrate of `9600`.

?> The Whitebox T3 for Raspberry Pi is compatible with the `I2C` protocol only.

## Distinguish the protocols

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols.md ':include')


## Set Protocol Manually

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols-manually.md ':include')


## Set Protocol With Whitebox I2C Toggler

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols-toggler.md ':include')

## Set Protocol By Code

!> On the Whitebox T3, only the switch from `I2C` to `UART` can be done in code. After the switch to `UART` you can't use the EZO Circuit with the Whitebox T3 until switched back to `I2C` using another method.

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols-code.md ':include')

##  Protocol Lock

[filename](https://raw.githubusercontent.com/whitebox-labs/whitebox-docs/master/tentacle/common/ezo-protocols-lock.md ':include')
