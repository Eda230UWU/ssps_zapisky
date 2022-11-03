CAM (content addressable memory) table - pamět a tabulka mac adres
kdyz nema destinaci v CAM tabulce, posle všem kromě odesílatele

je schopen poznat i switch

efektivnější než broadcast/multicast

"Switch Learn and Forward Method"

#### Learn
přidává MAC adresy do tabulky, pokud ji nezná
po pěti minutách se vymaže když se host neozve (neodesílá)

#### Forward
Forward pokud je v MAC (CAM) tabulce
pokud není tak multicast na všechny kromě hosta, od kterého rámec přišel

### Metody forwardování
Store and forward - přečte a pošle
Cut and forward - přečte destinaci a hned odešle  (rychlejší, bez checku integrity dat)

---

## Collision Domains
Switche se snaží zamezit kolizím

Full duplex na všech zařízeních -> žádné kolize

Jedno či více na half duplexu, je kolize možná 
Vetšina cisco a ms používá automatickou domluvu

---




