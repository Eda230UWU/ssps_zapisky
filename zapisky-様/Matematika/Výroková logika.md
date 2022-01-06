## Konjunkce
logický výrok a $\land$ b 

| a |---| b |---| a $\land$ b |
| 1 |---| 1 |-----| 1 |
| 1 |---| 0 |-----| 0 |
| 0 |---| 1 |-----| 0 |
| 0 |---| 0 |-----| 0 |

---
## Disjunkce

logický výrok  a $\lor$ b 

| a |---| b |---| a $\lor$ b |
| 1 |---| 1 |-----| 1 |
| 1 |---| 0 |-----| 1 |
| 0 |---| 1 |-----| 1 |
| 0 |---| 0 |-----| 0 |

---

## Ekvivalence
$$ a \iff b $$
$$ a \Rightarrow b $$ $$ b \Rightarrow a $$

## Kvantifikované výroky

### Všeobecný kvantifikátor
$\forall$ / pro všechny platí že
### Existenční kvantifikátor
$\exists$ pro aspoň jednoho platí že
$\exists!$ právě pro jednoho platí že

---
· Když prší, jsou mokré chodníky.
Prší - A
mokré chodníky - B
$$ a \land \neg b$$

---
· František pojede na hory, nebo k moři.
pojede na hory - a
k moři - b
$$ \neg a \land \neg b \iff \neg (a \lor b)$$ 

---
· Nebude-li pršet, nezmoknem´.
nebude pršet - a
nezmoknem - b

$$ a \land \neg b \iff \neg ( a \Rightarrow b )$$

---
· Na víkend pojedeme do Jizerských hor a do Krkonoš.
pojedeme do Jiz. hor - a
pojedeme do Krkonoš - b
$$ \neg a \lor \neg b \iff \neg (a \land b)$$

---
· Ve středu pršelo a foukal silný vítr.
pršelo - a
foukal silný vítr - b
$$ \neg a \lor \neg b \iff \neg (a \land b)$$

---
· Kdy přijdeš?
není výrok

---
· Posadíme se do křesla, nebo na pohovku.
do křesla - a
na pohovku - b
$$ \neg a \land \neg b \iff (a \lor b)$$

---
· Posadíme se do křesla, nebo na pohovku?
není výrok

---
· Když bude sněžit a foukat silný vítr, nedostaneme se na horskou chatu.
snežit - a
foukat - b
nedostaneme se - c
$$ (\neg a \lor \neg b) \land \neg c \iff \neg ((a \land b) \Rightarrow c)$$

---

![[Pasted image 20211119083950.png]]
Pro všechna reálná x platí, že když je x dělené 7, zbytek bude 0
$\forall x \in \mathbb{R}; x mod 7 = 0$
