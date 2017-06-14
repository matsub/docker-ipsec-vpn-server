# IPsec VPN Server on Docker

This is a fork of [hwdsl2/ipsec-vpn-server](https://hub.docker.com/r/hwdsl2/ipsec-vpn-server)
that allows to set the IKE port in environment variable.


## Featrues

In addition to the original, this image provides following features.


### Environment variables

2 more variables can be declared in environment variables.

- `IKE_PORT` for the IKE port to listen on. The default is 500.
- `IKE_NAT_PORT` for the IKE NAT Traversal port to listen on. The default is 4500.

```
IKE_PORT=27001
IKE_NAT_PORT=27002
```


## Note

Note that expose the ports you declared for this container.
The default are *500/udp* for the IKE and *4500/udp* for the IKE NAT Traversal.
See [the documentation of libreswan](https://libreswan.org/man/ipsec.conf.5.html)
for detail.


## Original License

Copyright (C) 2016-2017 [Lin Song](https://www.linkedin.com/in/linsongui) [![View my profile on LinkedIn](https://static.licdn.com/scds/common/u/img/webpromo/btn_viewmy_160x25.png)](https://www.linkedin.com/in/linsongui)   
Based on [the work of Thomas Sarlandie](https://github.com/sarfata/voodooprivacy) (Copyright 2012)

This work is licensed under the [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/)   
Attribution required: please include my name in any derivative and let me know how you have improved it!
