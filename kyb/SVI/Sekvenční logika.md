Základním principem je zapojení, které má paměť.
To znamená, že výstupy v pravdivostní tabulce závisí na předchozích stavech.
Např. za stavu kdy oba vstupy jsou nula, nelze určit výstup, bez znalosti předchozího stavu. 

### Základní zapojení (klopný obvod R-S, S-R latch)

<img src=Images/SRlatch.jpg>

S - Set (stačí zapnout impulzem, neboť nastavením na 1 dochází k aktivaci paměti)
R - Reset (prohazuje stavy Q a Qnot, tedy prohazuje výstup z nula na jedna a naopak)
1-1 je zakázaný stav, neboť není možné určit v jakém stavu je Q (nestabilní poloha, stav závisí na perturbacích a nestabilitách)

Toto zapojení umožňuje vytvoření datové buňky 
### Klopný obvod typu D

<img src=Images/SRlatchD.jpg>

V případě Kdy vstup (C), tj. (enabled) je nastaveno na hodnotu 1, pak zapojení ukládá hodnotu D do hodnoty Q. Po tomto nastavení SR latche (tj. uložení hodnoty) je možné (enabled) vstup vypnout, a hodnota Q zůstane stejná, a nebude reagovat na D (datový vstup), tj. hodnota Q bude nadále ukládat uloženou hodnotu, dokud se opět nezapne vstup (enabled, C) pro nový proces uložení vstupu D do paměti (Q). 

Toto zapojení ukládá informaci 1 bit. Pomocí sekvence takových datových buněk lze uložit větší množství dat.

Jak funguje kondenzátor a vstup C? (jak funguje derivační článek?)

### J-K klopný obvod
J, K = S, R, ale vstupy jsou spojené (zkratované), a tedy obvod se buď nenastavuje, nebo přehazuje svou hodnotu. Obvod pracuje pokud JK je nastaveno na jedna, a při každém tiku hodin (zapnutí na hodnotu 1) dochází k prohození výstupu z nuly na jedna a naopak. Výsledkem je, že výstup kmitá mezi 1 a 0 stejně jako CLK, avšak s poloviční frekvencí. 
J-K klopný obvod lze využít pro půlení frekvence signálu (např. využití v hodinářství pro zpřesnění.)

### Shrnutí klopných obvodů
<img src=Images/klopne_obvody.jpg>


### Příklad zapojení které sčítá hodnoty

<img src=Images/calculator.jpg>


### Paralelní vs. Sériové zapojení registrů.
Registr slouží k ukládání hodnot do paměti, a je složen z klopných obvodů.
Posuvní registr (viz obrázek), postupně ukládá postupné hodnoty, které si můžeme najednou zpřístupnit (sériové -> paralelní zapojení)

<img src=Images/registers.jpg>
<img src=Images/registrs1.jpg>


