Motherboard nebo mainboard

## Funkce

deska plošných spojů s elektronickými obvody (PCB)
části jsou propojeny soubory vodiču (sběrnicemi)
vícevrstvé plošné spoje 

laminátová deska ze skelné tkaniny sycená epoxidovou pryskyřicí, na níž jsou vytvořeny vodivé cesty z mědi

ATX - Advanced techonology extended

veškerá komunikace mezi jednotilivými díly počítače
napájí jednotlivé komponenty
obstarává komunikaci periferií s CPU
výběr rozhoduje o další možnosti upgrade celého počítače


---
## Severní můstek
Procesor, RAM, Grafická karta

Rychlé přesuny dat mezi klíčovými perifériemi
- grafická karta
- paměti



## Jižní můstek
Obsahuje ostatní periférie

- Pevné disky 
- USB
- Zajišťuje služby BIOSu

---

# BIOS

Basic input output system
Je uložen na čipu na základní desce
Startuje vždy při zapnutí počítače

Rozpoznává a aktivuje komunikace všeho hardwaru na motherboardu
testuje funkčnost součástí PC, POST (Power on self test)
Zavádí operační systém ze spouštěcího oddílu pevného disku
"Tlumočník" mezi HW a OS

```ad-note
title: UEFI
color: 200, 0, 0
nový standard BIOSu

podpora secure boot
-  kontrola certifikovaných SW komponentů
- při zavádění OS jsou kontrolovány elektronické klíče (certifikáty)

 ukončení zpětné kompatibility s 16bitovými procesory 8086
 lepší využití schopností nových procesorů
 
mohou zavádět OS z pevných disků větších než 2TB
```


## Tři vrstvy BIOS
1. 
Je z výroby uložena do ROM paměti
(Dnes už Flash ROM -> Jednoduší aktualizace)
musí být automaticky k dispozici ihned po startu OS
jsou v ní uložené neměnitelné vlastnosti a nastavení PC
detekuje připojení HW

2. 
tvoří čip CMOS, energeticky zavislá pamět (potřebuje baterii na MB)
ukládá se do ní nastavení programu SETUP (konfigurace volitelných vlastností BIOS resp. HW)

3. 
Ovladače jádra OS
zavádějí se v průběhu spouštení systému
ovladače jsou uloženy
- na základní desce
- v rozšiřujících kartách
- v pamětech
- v procesoru

## POST (Power on self test)
testuje config systému
hledá přídavné karty (jejich ROM-BIOS)
porovnává zjištěnou konfiguraci s CMOS pamětí
v případě shody pokračuje v zavádění OS
chyby hlásí výpisem či zvukem (tzv. Beep Code)


### Příklady chybových hlášení
No CPU installed
System failed CPU
System failed memory test
No keyboard detected
CPU temperature too high
CPU fan failed
CPU voltage out of range
Address Line short
CMOS battery state low

-> Beep codes -> Vypípáva chyby

---

## Chipset
 #### Hlavní  řídící obvod zíkladní desky
 Vnitřní hodiny počítače
 Generátor pracovního cyklu
 je zdrojem taktovacího signálu pro CPU
 udává takt procesoru, sběrnici i perifériím
 řídí komunikaci na základní desce

 Northbrdige a South Bridge

## Sběrnice

sbírá data a příkazy a drstribuuje je mezi perifériemi a vnitřníkomponenty ZD

nesdílená sběrnice -> přenáší pouze jistý typ informace
sdílené sběrnice -> stejné adresové a datové vodiče pro přenos různých typů informace (nutnost režie, ovykle pmocí řadiče)

#### Řadiče sběrnic
řídí přenosy dat po sběrnicích
periférie s vyšší prioritou má přednost



soustava měděných vodičů
vzájemně propojuje jednotlivé komponenty
přenáší se data a adresy dat (datová a adresová sběrnice)
datová propustnost ovlivňuje výkon systému

	Parametry ovlivňující výkon sběrnic
	- šířka přenosu dat
	- rychlost přenosu dat
	- datová propustnost

další rozdělení:

podle přenosu:
- sériově
- paralérní

podle směru:
- jednosměrné
- obousměrné

podle synchronizace:

### Synchroní
- funguje na základě stanovených pravidel (návaznost na CLK)
- komunikace probíhá v reálném čase
- mimo datový kanál existuje ještě synchronizační kanál -> řídící sběrnice
- při komunikaci na sebe zařízení vzájemně čekají
- pomalejší technologicky náročnější ale jistější způsob komunikace

### Asynchorní
- komunikace není závislá na čase
- zařízení spolu komunikují pouze v případě potřeby, potvrzují si jen přijetí dat
- jednoduchý aa rychlý systém přenosu dat

### Multimastering
- možnosti, kdy provoz sběrnice může řídit některá z rozširujících karet
- karta vykonává část práce za CPU, který nemusí provozem sběrnice zdržovat
- režim je velmi výhodný v případě, kdy si mezi sebou vyměňuji data dvě periferie

#### PCI
Peripheral component interconnect

- Používá paralelní přenos dat (šířka 32 nebo 64 bitů u verze PCI-X)
- rychlost sběrnice je 33MHz pro 32bit resp. 66MHz a 133MHz pro 64bit
- v jednom počítači může být více na sobě závislých PCI sběrnic
- synchronní sběrnice, možno použít nejen v PC ale např i v Macintosh
- nejvyšší teoretická datová propustnost je 1066MB/s

#### AGP
accelerated graphics port

- nízká propustnost PCI sběrnice vedla k vytvoření specializovaného portu AGP určeného pro grafické karty
- AGP slot není klasická sběrnice, protože lze připojit pouze jedno zařízení

## Typy sběrnic
- systémová CPU -- chipset
- paměťová CPU -- RAM
- rozšiřující PCI, PCIe 1x, 2x, 4x
- grafická pro grafické karty typu PCIe 16x



### PCI express
PCIE-E
- vytvořena jako náhrada za starší standardy PCI (PCI-X) a AGP
- označení sběrnice není zcela správné, protože se jedná o dvoubodové spoje
- data jsou přenášena bez potřeby adresy (adresace zařízení)
- používá sériový přenos  dat (na rozdíl od svých předchůdců)
- full duplex, komunikace oběma směry najednou skrze dva vodiče (linka)
- verze jsou označovány podle počtu těchto linek (x1, x2, x4, x8, x16)
- nezávislá komunikace mezi jednotlivými zařízeními
- nemusí se čekat na uvolnění sběrnice pro jiné zařízení
- nejvyšší teoretická datová propustnost verze 3.0 je 16GB/s v každém směru



---

## Standarty a formáty

#### Co se skrývá pod pojem "standart formátu PC"?
- všechny součásti v počítači musí být mezi sebou kompatibilní
- rozměry a rozmístění jednotlivých komponent, sběrnic a jejich výstupů
- elektrické napětí
- pro každý stadard existuje několik variant

#### Standart PC/AT (advanced technology)
starý dnes již nepoužívaný formát
formát uvedla dva roky po začátku sériové výroby procesorů 80286 firma IVM)změnil se napájecí zdroj -> Vyšší výkon
přímo spínatelný zdroj

#### Standard PC/ATX (advanced technology extended)

- aktuální standard od roku 1995
- nová napěťová větev 3,3V a počítač je napájen i po vypnutí (Standby mode)
- SW řízení napájení i spínání (wake on Lan), dále pomocí speciálních obvodů na základní desce
- změnily se rozměry a uspořádání prakticky všech komponent počítače
- vysoký výkon napájecích zdrojů


#### Standard BTX (Balanced Technology Extended)
- slepá vývojová větev firmy intel z roku 2004/05
- i když je v ohledech lepší tak se nikdy neprosadil



---











