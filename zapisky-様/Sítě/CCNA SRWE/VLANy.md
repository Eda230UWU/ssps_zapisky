
---

VLAN se identifikuje s IEEE 802.1Q headerama (4 byty)
2 byty jsou TPID
3 bity User Priority
CFI 1 bit
VLAN ID 12 bit (4096 limit)
DST MAC>SRC MAC> IEEE802.1Q Header > ...
---

![[Pasted image 20221103180026.png]]


### Typy VLAN:

#### Voice VLAN:
Assured bandwith
high QoS priorita


### VLAN trunk



---


# Configurace VLAN

přes 4000 VLAN

```
enable
conf t
vlan 20
name student
end
```

```
#show vlan
```

delete VLAN <
```
no vlan vlan_id
```

![[Pasted image 20221103182312.png]]
*Trunk configurace*

### DTP Dynamic Trunking Protoco;