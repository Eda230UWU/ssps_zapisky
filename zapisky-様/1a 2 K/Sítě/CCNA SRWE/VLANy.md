
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

### DTP (Dynamic Trunking Protocol)

switchport mode trunk
switchport nonegotiate <<

statický trunk (nezapne se automaticky na trunk, když je switch na druhé straně na trunk (pouze na jednom portu))

![[Pasted image 20221103182726.png]]

chceme vypnout z důvodu bezpečnosti dynamic auto a dynamic desirable

show dtp ``interface



---


## Sítě zápisky

`switch(config)vlan 10` - vlan 10
`(config)interface range f 0/1-2` vyber interfaceu od 1 do 2
`(config-interface-rng)switchport access vlan 20` nastavit vlan 20 pro porty 1 a 2


```
nastaveni DHCP pro jednotlive VLANy
+ pro tip: psát komandy do bloku 
```

---

#### Cvičení
enable
config t
interface g0/1
switchport mode trunk
exit

vlan 10
ex
vlan 20
ex
vlan 30
ex

interface range f 0/1-2

switchport access vlan 10
exit

interface range f 0/2-3

switchport access vlan 20
exit

interface range f 0/4-5

switchport access vlan 30
exit

ip dhcp excluded-address 172.160.96.1 172.160.96.5

ip dhcp pool vlan10
network 192.168.0.0 255.255.255.0
default-router 192.168.0.1
dns-server 1.1.1.1
exit

ip dhcp pool vlan20
network 192.168.1.0 255.255.255.0
default-router 192.168.1.1
dns-server 1.1.1.1
exit

ip dhcp pool vlan30
network 192.168.2.0 255.255.255.0
default-router 192.168.2.1
dns-server 1.1.1.1
exit

int vlan 10
ip add 192.168.0.1 255.255.255.0
exit

int vlan 20
ip add 192.168.1.1 255.255.255.0
exit

int vlan 30
ip add 192.168.2.1 255.255.255.0
exit


routr

int g0/0/0.10
encapsulation dot1Q 10
ip add 192.168.0.1 255.255.255.0
exit

int g0/0/0.20
encapsulation dot1Q 20
ip add 192.168.1.1 255.255.255.0
exit

int g0/0/0.30
encapsulation dot1Q 30
ip add 192.168.2.1 255.255.255.0
exit



---