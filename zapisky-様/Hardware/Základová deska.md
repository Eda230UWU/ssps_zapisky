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


---





















