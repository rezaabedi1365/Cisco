
## ACL

Create ACL.
```
(config) # access­-list _ { deny | permit | remark } {sourc­e+w­ild­card}

# Create Named ACL.
(config) # ip access­-list standard {name}

# Attach ACL to an Interface.
(confi­g-if) # ip access­-group { access­-li­st-­number | access­-li­st-name } { in | out }
```

ACL for VTY.
```
(confi­g-line) # access­-class {number} { in | out }
```

Displays only denoted ACL.
```
# sho access-l {name/­number}
```
