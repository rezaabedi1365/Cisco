## DHCP

```
# Creates named DHCP pool
(config) # ip dhcp pool {name}

      # Define Range of Addresses
      (dhcp-­config) #net {ipv4net} {subnet}
      (dhcp-­config) #default-r {gateway}
      (dhcp-­config) #dns-s {DNS}
      (dhcp-­config) #domain-n {Axyz.com}
# Excludes ip ranges, or single IP's.
 (config) #ip dhcp exclud­ed-­address {low ip range} {high ip range} | {single ip}
```

Sets DHCP Relay
```
(config) #ip helper­-ad­dress {ipv4net}
```
