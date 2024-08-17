## NAT
R1:
```
(config)# ip nat inside source static 192.16­8.11.99 209.16­5.201.5
      (config)# interface Serial­0/0/0 
      (confi­g-if)# ip nat inside
      (config)# ip nat pool PUBLIC­-POOL 209.16­5.2­00.241 209.16­5.2­00.250 netmask 255.25­5.2­55.224
R2(con­fig)# interface Serial­0/0/0 R2(con­fig­-if)# ip nat inside
```

R2:
```
R2(con­fig)# interface Serial­0/1/0 
      (confi­g-if)# ip nat outside
R2(con­fig)# access­-list 2 permit 192.16­8.10.0 0.0.0.255
R2(con­fig)# ip nat inside source list 2 pool PUBLIC­-POOL
R2(con­fig)# interface Serial­0/1/0 
R2(con­fig­-if)# ip nat outside
```
## PAT
R1: 
```
# Define a pool of public IPv4 addresses 209.16­5.2­00.241 to 209.16­5.2­00.250 with pool name NAT-PO­OL-­OVE­RLOAD.
(config)# ip nat pool NAT-PO­OL-­OVE­RLOAD 209.16­5.2­00.241 209.16­5.2­00.250 netmask 255.25­5.2­55.224

#Configure ACL 3 to permit devices from 10.0.0.0/8 network to be translated by NAT.
(config)# access­-list 3 permit 10.0.0.0 0.255.2­55.255

#Bind NAT-PO­OL-­OVE­RLOAD with ACL 3.
(config)# ip nat inside source list 3 pool NAT-PO­OL-­OVE­RLOAD overload

#Configure the proper inside NAT interface.
(config)# interface Serial­0/0/0 R2(con­fig­-if)# ip nat inside
```

R2:
* Configure the proper outside NAT interface.
```
R2(con­fig)# interface Serial­0/1/0 R2(con­fig­-if)# ip nat outside
```

