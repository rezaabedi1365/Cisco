## RIP
```
(config) # router rip
(confi­g-r­outer) #version 2
(confi­g-r­outer) # no auto-s­ummary

# prevent the transm­ission of routing updates through a router interface, but still allow that network to be advertised to other routers.
(config) #passiv­e-i­nte­rface

# propagate a default route in RIP
(confi­g-r­outer) #ip route 0.0.0.0 0.0.0.0

# This instructs R1 to originate default inform­ation, by propag­ating the static default route in RIP updates.
confi­g-r­outer) #defaul­t-i­nfo­rmation originate

```

```
(config) #show ip protocols
(config) #network ip-address
```
