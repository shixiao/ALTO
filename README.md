
###Validating rpc and rpc replies

####configuration:

Download `ietf-netconf.yang` and `ietf-netconf-acm.yang` from [here](http://dld.netconfcentral.org/src/).

The version included in this repo is [ietf-netconf@2011-06-01.yang](http://dld.netconfcentral.org/src/ietf-netconf@2011-06-01.yang) and [ietf-netconf-acm@2012-02-22.yang](http://dld.netconfcentral.org/src/ietf-netconf-acm@2012-02-22.yang).

To generate the netconf rpc schemas (`ietf-netconf-rpc.rng` in particular):
```
yang2dsdl -t rpc ietf-netconf.yang
```

####validation of rpc request:


```
yang2dsdl -t rpc alto-service.yang
yang2dsdl -s -j -b alto-service -t rpc -v ird-request-example.xml
```

####validation of rpc reply:

```
yang2dsdl -t rpc-reply alto-service.yang
yang2dsdl -s -j -b alto-service -t rpc-reply -v ird-request-example.xml
```

[Conversion between XML and JSON](https://code.google.com/p/pyang/wiki/XmlJson)

