
## VLAN

Create Vlan 
```
vlan {vlan-id}
(confi­g-vlan) # name {vlan-­name}
```
assign voice vlan
```
(confi­g-vlan) # switchport voice vlan
```
assign access vlan
```
interface {inter­fac­e_id}
(confi­g-if) #switchport mode access
(confi­g-if) #switchport access vlan
```
assign truk vlan
```
(confi­g-if) # switchport mode trunk
(confi­g-if) # switchport trunk native vlan #
```
verify :
```
show vlan brief
```


clear vlan
```
(config) # erase startu­p-c­onfig
(config) # elete vlan.dat
```

