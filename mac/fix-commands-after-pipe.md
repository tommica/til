# Fix commands after pipe character

Using "AltGr+I" to create the pipe and pressing space afterwards creates a non-breaking space, which gets interpeted as part of the commands name, thus it will never be found.

To fix it, just do this:

```bash
vim ~/.inputrc
"\xC2\xA0": " "
```

[source](https://relativkreativ.at/articles/why-chaining-commands-with-pipes-in-mac-os-x-does-not-always-work)
