
###Validating rpc and rpc replies

####configurations:

Download ietf-netconf.yang from [here](http://dld.netconfcentral.org/src/). (The version included in this repo is ietf-netconf@2011-06-01.yang)

Do `$ yang2dsdl -t rpc ietf-netconf.yang` to generate `ietf-netconf-rpc.rng`.


```
yang2dsdl -t config alto-service.yang
yang2dsdl -s -j -b alto-service -t rpc -v ird-request-example.xml

```