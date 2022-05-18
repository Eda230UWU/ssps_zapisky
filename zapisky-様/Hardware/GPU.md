# GPU
Grafické karty

Výpočet grafického obrazu a jeho zobrazení na monitoru, displeji, projektoru, nebo televizní obrazovce

Výrobci procesorů - AMD a Nvidia
Výrobci karet - ASUS, Gygabyte a další

Graphics processing unit
Výpočetní jádro grafické karty
Řadič paměti = přenos informací mezi GPU a grafickou pamětí


### FLOPS
Floating point operations per second



---

#### karta do sběrnice (Dedikovaná) x integrovaná
Dedikovaná - sběrnice -> PCI-E 16x, AGP, PCI

integrovaná jako grafické jádro procáku, dříve v chipsetu (severní můstek)

### Integrovaná
- Omezený počet
- součást základní desky
- nižší výkon
- levnější

### Dedikovaná
- Rychlejší
- vyšší výkon
- sloty na základní desce
- vlastní BIOS, paměť procesor
- dražší

---

### Základní části karty
- GPU
- VRAM
- DAC
- BIOS
- Rozhraní == konektory

---

 ### VRAM 
 - paměť - potřebné informace pro GPU k výpočtům
 - integrovaná karta - operační paměť
 - rožšiřující karta - vlastní paměť

### Firmware
BIOS
taktovací frekvence GPU a pamětí
napětí GPU
informace o modelu karty

### DAC
Digital to Analog Converter
Převod digitalního obrazu na analogový

### Potřebný SW
ovladače grafické karty
kontrolní panel (např. ATI catalyst center)
DirectX - zpracování 2D a 3D grafiky
Open GL

---

## princip funkce GPU
1. data od CPU do VRAM
2. GPU čte data ve VRAM
3. zpracování dat
4. převod na digitální obraz
5. převodníkk - zpracování signálu pro monitor

---

## Chlazení grafické karty
#### Chlazení vzduchem
aktvní chlazení, kovový chladič s ventilátorem
kombinace s heatpipes
pasivní chlazení
- správné proudění vzduchu ve skříni

#### Chlazení vodou
Nejvýkonnější grafické karty
kvalitní chlazení
kombinace s chlazením procesoru nebo pamětí

---

### Propojení více grafických karet
funkcejako jedna
zvýšení výpočetního výkonu
více monitorů
PCI-E16x

##### nVidia - SLI
Scalable link interface
stejný druh karet
speciální kabel

##### ATI - crossfire
DVI kabel
vyšší datová propustnost
karty nemusí být stejné

---

### DB-15 (VGA, D-sub)
D-subminiature
analogový elektrický signál
DB-15
15 vodičů

---

### DVI
Digital visual interface
Digital/analog signál
Částenčne kompatibilní s HDMI
DVI-D
DVI-I
single link a dual link

---

#### HDMI
High definition multimedia interface

nekoprimovaný digitalní signál - obraz i zvuk v HD
zvuk až 32 kanálů
Full HD + 4K obraz
zpětně kompatibilní s DVI
zatížen licenčními poplatky

---

#### DisplayPort (1.0)
Datováá propustnost až 10,8 Gb/s

Do 3 metrů 2560x1600
Do 15 Metrů 1920x1080

---

## Parametry obrazu
rozlišení = počet pixelů (vodorovně x svisle)
rozlišení tiskáren: dpi (počet pixelů na 25,4mm)

FHD - full high-definiton
VGA - Video Graphics array
XGA - extended  graphics array
