 Základní úlohou procesoru je pracovat podle pokynů určitého programu nebo hardwaru v počítači či jiném podobném zařízení (tablet, smartphone...)

Využívá různě složitých programových instrukcí, které jsou zpracovávány na základně jednoduchých logických operací

Je mozkem počítače, kavlita CPU zásadně ovlivňuje výkon celého počítače

## Z čeho se skládá
hlavní částí procesoru je jádro (integrovaný obvod)
je pripevněno na základnu s piny
jádro cpu je v pouzdře (kov, keramické sloučeniny), které odvádí zbytokové teplo a také poskytuje ochranu jemným obvodům jádra

## Z čeho se skládá jádro CPU
arithmetic logic unit -> všechny aritmetické a logické výpočty
floating point unit -> matematický koprocesor vykonávající operace s čísly s pohyblivou řadovou čátkou
graphic processing unit -> dostačující pro bežnou práci a multimédia
řadič CPU controller -> elektronická řídící jednotka, realizovaná sekvenčním obvodem, která řídí činnost všech částí počítače
registy -> malá úložiště dat umístěná v mikroprocesoru, jejichž obsah lze načíst mnohem rychleji, než kdekoliv jinde v počítači
vyrovnávací paměť (cache) -> překladiště dat mezi rychlejším a pomalejším zařízením v počítači, slouží i jako dočaasná pamět

## Jak funguje procesor?
Přečte posloupnost vstupního registru (jedniček a nul)
dékoduje na řetězec intrukcí
tuto instrukci  nalezne v instrukční sadě ("kuchařka") a provede
výsledek uloží do výstupního registru

## Nejdůležitější parametry
vnitřní frekvence
počet fyzických jader
Šířka datové sběrnice
Šířka adresové směrnice
Typ použité instrukční sady (CISC a RISC)
kapacita a typ vyrovnávací paměti
kapacita a typ použitých registrů
patice (socket) -> podpora čipové sady na motherboardu
podpora modulů operační paměti
výrobce

---

## Architektura CPU
MCU (micro controller unit) -> Nejjednoduší procesory (žehlička na vlasy, lednička, mikrovlnka) malá možnost rozšíření -> nízká cena a výkon

GPU (Graphic processor unit) 
speciální procesory, které jsou součástí grafických karet, zpracovává hlavně obrazová data a výpočty fyziky ve 3D

CPU (Central processor unit)
Základní řídící jednotka počítače

APU (Accelerated processing Unit)
Čip, do kterého je v jednom pouzdře integrováno jádro/jádra CPU a GPU (dva v jednom)

DSP (Digital signal processor)
Vysoký výkon
zpracovává velké objemy dat v konkrétních specifikacích

NPU (Network processor Unit)
součást switchů, směrovačů a dalších síťových zařízení

---

## Architektura CPU
bez ohledu na výrobe, architektura je pojem, který označují šířku datové a adresové směrnice (kolika bitový procesor je)

vnitřní stavba procesoru, souvisí s instrukční sadou

###  Instrukční sady a strojový kód
instrukční sada je vnitřní programové vybavení procesoru
strojový kód (101010000011011011011100110)
skládá se ze složitějších instrukcí  které jsou řadičem CPU dekódovány na tzv. mikroinstrukce
těmi se řídí zbytek počítače i části samotné CPU
Intrukční sada jsou intrukce kterým CPU rozumí

###  CISC
Complete instruction set of Computer

snaha o co nejkoplexnější vnitřní program CPU
 příliš mnoho instrukcí vyžaduje víceúroňový dekódér -> zpomalení práce
 Instrukce nemají jednotný formát, potřebuji složitý řadič -> zpomalení práce
 CISC složitější adresování
 
 ###  RISC
 Reduced Intruction set of Computer
 
 80% programů používa pouze čtvrťinu CISC -> důvod vytvoření RISC
 Často jednotný formát -> jednoduše se adresují
 minimální instrukční repertoár
 Většina instrukcí se provádí během jednoho strojového cyklu
 nevýhoda jsou složitější resp. komplexnější programy a především nutnost použité velkého množství rýchlých a drahých pamětí - registrů
 
 Výrobce se rozhoduje CISC a RISC podle využití CPU (který typ intrukcí bude mít majoritní zastoupení v instrukční sadě)
 
 ### Architektura 86x
 navazující architektury nové generace, mimo jiné kombinující a rozšiřující podle vývojových větví instrukčních sad CISC a RISC
 
 
 ## Rozšiřující instrukční sady
 více instrukcí z konkrétní oblasti
 urychlují zpracovávání dat
 nejsou nutně povinné k použití
 
 MMX - multimediální instrukce
 3DNow (AMD procesory pro 3D grafiku)
 KNI pro 3D aplikace
 SSE (Intel verze 3DNow, pro SIMD zpracování)
 
 ---
 
 ## Pipelining
 Proudové zpracování instrukcí
 rozdělení zpracování jedné instrukce mezi různé části procesu, čímž získáte možnost zpracování více instrukcí najednou v jednom cyklu
 
 je rozdělena do posloupnosti
 4-5 fází

1. Výběr intrukce IF instruc. fetch
2. Dekódování ID instruc. decode
3. Výběr operadnů, provedení operace EX execute
4. čtení zápis do paměti MEM memory acces
5. zápis výsledku WB writeback

---

#### sekvenční zpracování
dříve se intrukce zpracovávali jednotliově

#### Skalární zpracování
Všechny operace probíhají součastně v n různých sekcích
během každého taktu se načítá nová instrukce

#### Superskalární zpracování
dvě a více jednotek provádí pipelining

#### Hyperpipelining
Až dvě desítky fází v jedné pipelině
problém s datovými závislostmi, což může částečně řešit hyper threading

---

#### nevýhody pipeliningu
jedna instrukce potřebuje data, která jsouvýsledkem předchozí instrukce

intrukce nezná adresu paměti, odkud má přečíst data

delší pipeline znamená více datových i adresových závislostí

vznikají prázdná místa "bubliny" -> snížení výkonu



---

