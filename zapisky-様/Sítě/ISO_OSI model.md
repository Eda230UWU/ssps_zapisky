---

# Data link layer
#### LLC
komunikace s ostatními vrstvami
#### MAC
kontrola přístupu k médiu
enkapsulace
adresace pomocí MAC adres
(Ethernet IEEE 802.3, WLAN IEEE 802.11, WPAN IEEE ...)
### Logická a fyzická topologie
fyzická topologie- fyzické připojení, jak jsou spojené zařízení
logická topologie- 

## Frame
### HEADER
Frame start
Adresace
Typ
Control (quality of service)


Data

### Trailer
Error detection
Frame stop

# Ethernet (Spojová a fyzická vrstva)
## Frame
SFD
Destination MAC Adress
Source MAC Adress
Type/Lenght
Data
FCS/CRC check

## MAC adress a Hexadecimální soustava
OUI - organization unique 
Vendor

## MAC tabulka

# ARP protokol
Address resolution
počítače a routery (na třetí vrstvě)

ARP request - 
Vygeneruje počítač
broadcast (ff:ff:ff:ff:ff:ff) - who is 102.168.10.4


ARP reply -
vygeneruje cíl ARP requestu
unicast zpráva, oznamuje svojí MAC adresu k IP adrese


ARP table
IP adresy a MAC adresy
arp -a = zobrazení tabulky ve windows
show ip arp = ARP tabulka cisco routeru


ARP spoofing - man in the middle útok


# TCP 
TCP handshake = three way handshake

Navazuje a ukončuje spojení
Transmission Control Protocol
spolehlivost spojení
trackování odeslaných a přijatých paketů
Data mohou přijít ve špatném pořadí -> seřazení


# UDP
Nic neumí
jak přijdou tak přijdou
nenavazuje protokol
Nespolehlivost

# ports
Well known ports
Registered ports
Private and dynamic ports



---

data na segmenty na header na packet na frame