SimpleSNIProxy
==============

Replace of https://github.com/dlundquist/sniproxy . written with Go Language.
sniproxy is well works. but It's written with C/C++. so It's hard to modify.
Go Language's Performanace is not bad for network server, so written in Go Language.

This code is came from the sub-product of Macadamia(L4/L7 Loadbanacer with Go).

* This code can avoid korean HTTP SNI censorship.
  * Tested: 2019-02-18 (with SK Broadband)

Installation
============

Just build run.

or Use Dockerfile to build and run

```
docker build -t sniproxy .
docker run -d -p 80:80 -p 443:443 sniproxy
```


or Use Docker hub's pre-built version

```
docker run -d -p 80:80 -p 443:443 ziozzang/simplesniproxy
```

Issue
=====

There's no security options. so, you must use firewall(ex:iptables..).

You can build your own Smart-DNS Proxy with this SimpleSNIProxy and PyDNSProxy (it has HTTPS SNIProxy Feature, but slow and buggy. so you can disable it's Proxy Server.).

Special Thanks
==============

SNIProxy(HTTPS) code came from 'stupid-proxy' https://github.com/gpjt/stupid-proxy/


