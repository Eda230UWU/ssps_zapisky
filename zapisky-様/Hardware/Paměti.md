1 buňka = 1 bit
1 byte = 8 bitů
kapacita ovlivňuje množství dat, které můžeme uložit


---

#### Přenosová rychlost
faktory:
1. vybavovací doba
2. doba potřebná k zápisu dat
3. frekvence
4. kapacita vyrovnávací paměti

---

Lze si vybrat z jeden ze tří parametrů

1.  Nízká cena
2. Vysoká rychlost
3. Vysoká kapacita

---

cena klesá směrem od procesoru spolu s rychlostí
kapacita roste směrem od procesoru

---

### Rozdělení pamětí
## Vnitřní a Vnější pamět
Vnitřní jsou závislé na energii

### ROM (Read only memory)
jen pro čtení, většinou se programuje přímo u výrobce
nedá se přeprogramovat, je statická a energeticky nezávislá

PROM
programovatelná, energeticky nezávislá
programuje se na speciálním zařízení, princip destrukce vodivých cest

EPROM (Eraseable PROM)
přepisovatelná, vymazání informací se provádí ultrafialovým zařízením

EEPROM (Electrically Eraseable PROM)
dá se mazat a programovat elektrickým prodem

RWM (Read Write memory)

## RAM (Random acces memory)
hlavní součástka je unipolární tranzistor a kondenzátor
energeticky závislá (kondenzátor se vybíjí)

SRAM (statická RAM)
informaci nese bistabilní
nemusí se refreshovat je rychlejší
vyšší cena, používa se u vyrovnávacích pamětí

DRAM (dynamická RAM)
informaci nese stav kondenzátoru (nabitý x vybitý)
samovolné vybíjení, nutno obnovovat informace
menší počet tranzistorů == větší paměť
hlavní operační paměť

x

Vnější nejsou závislé na energii
polovodičové:
Flash
SSD

magnetické a hybridní:
HDD
SSHD

Optické:
CD
DVD
BD

---

Registry > Vyrovnávací paměti > Operační paměti > SSD a flash disky > HDD > Optické mechaniky > Magnetické pásky

Roste kapacita a klesá cena


---

Moduly operační paměti RAM
historické typy modulů

- DIPP
- SIPP
- SIMM 30-pin
- SIMM 72-pin
- DIMM SDRAM
- DIMM DDR

SIMM (single in-line memory module)
DIMM (dual in-line memory module)
SDR (single data rate) - využívá synchronní signál s kmitočtem základní desky
DDR (double data rate) - data jsou během jednoho cyklu přenášena dvakrát

---
# časování RAM

Kromě frekvence a kapacity nás zajímá časování

#### CL (CAS latency)
-RAS (Row Acces Strobe) = adresa řádku
-CAS (Column Access Strobe) = adresa sloupce
	chceme co nejmenší číslo
dáno technologickým možnostmi paměti/chipsetu/procesoru

## 9-9-9-27 (TCL - TRCD - TRP - TRAS)
TCL = TAS latency
TRCD = RAS to CAS delay - zpoždění mezi výběrem řádku a adresací sloupce
TRP = RAS Precharge - zpoždění po výběru řádky
TRAS = Row Acces - doba potřebná pro adresaci řádku

---

###### Vyrovnávací pamět CACHE
data se v cache uchovávají podle pravděpodobnosti použití
cache uvolnuje pamět podle různých algoritmů

###### CMOS RAM (Complementary Metal-Oxide Semiconductor RAM)
polovodičová pamět
používá se například k ukládání conf BIOS


---
## HDD
Hard disk drive
elektromagnetický princim, mechanický disk
náchylný na otřesy

### Základní části pevného disku
deky s magneticky citlivým povrchem (plotny)
Raménko se čtecí a záznavou hlavou
vychylovací cívky
hnací motor s ložisky
elektronika disku


### Plotny
rozměry, 2,5'' a 3,5''
HDD může mít několik ploten nad sebou
povrch musí být dokonale hladký
5400 - 15000 ot/min 
rychlejší určené pro servery

### Cache
stejný účel jako jinde
Kapacita kolem 64MB (max 256MB)


### SCSI (small computer system interface)
integrován na desce nebo jako přídavná karta do slotu
vytváří v PC samostatný systém, nezatěžuje hlavní sys
umožňuje připojit externí zařízení

### SATA
serial ATA
sériové rozhraní
rychlá komunikace (6GHz frekvence)
přímé připojení - každý disk má svůj port řadiče

liší se přeedvším maximální teoretickou rychlostí
3revize
SATA 1.0
SATA 2.0
SATA 3.0





---
## Připojení HDD
EIDE kabelem
konektory SCSI

---



