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

## Instrukční sady a strojový kód
instrukční sada je vnitřní programové vybavení procesoru
strojový kód (101010000011011011011100110)
skládá se ze složitějších instrukcí  které jsou řadičem CPU dekódovány na tzv. mikroinstrukce
těmi se řídí zbytek počítače i části samotné CPU
Intrukční sada jsou intrukce kterým CPU rozumí

## CISC
Complete instruction seet of Computer

snaha o co nejkoplexnější vnitřní program CPU
 příliš mnoho instrukcí vyžaduje víceúroňový dekódér -> zpomalení práce
 Instrukce nemají jednotný formát, potřebuji složitý řadič -> zpomalení práce
 CISC složitější adresování