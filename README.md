# openconnect on linux for vpn instead of pulse secure
pulse secure does not support ubuntu 18 yet. But we can use openconnect, because support for Pulse Connect Secure was added to OpenConnect in June 2019, for the 8.04 release[[Openconnect](http://www.infradead.org/openconnect/pulse.html)]

This is for how to connect vpn through openconnect.
---

Download openconnect source code on version 8.04 (or later) from [openconnect website](http://www.infradead.org/openconnect/download.html). 
You may downloaded openconnect-[version].tar.gz file, so decompress the file
``` bash
  $ tar -xvzf openconnect-[version].tar.gz
  # ex) tar -xvzf openconnect-8.05.tar.gz
```
Go to root of the openconnect package, then `make` the package
``` bash
  $ cd openconnect-[version]
  # ex) cd openconnect-8.05
  $ ./configure && make check
```
Now you can use openconnect with `pulse` protocol.
``` bash
  $ ./openconnect --protocol=pulse vpn.example.com
```

Enjoy your vpn :)
