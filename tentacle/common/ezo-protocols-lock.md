To prevent accidental change of protocol in production, the protocol can be locked. While `Protocol Lock` is enabled, attempts to change the protocol by code or the manual method will fail. Only after disabling `Protocol Lock` the other methods will work again.
Using the `Plock` command:
```
Plock,1  // enable Plock
Plock,0  // disable Plock, default
Plock,?  // Plock on/off?
```
