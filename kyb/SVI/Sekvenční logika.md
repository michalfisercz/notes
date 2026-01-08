Základním principem je zapojení, které má paměť.
To znamená, že výstupy v pravdivostní tabulce závisí na předchozích stavech.
Např. za stavu kdy oba vstupy jsou nula, nelze určit výstup, bez znalosti předchozího stavu. 

### Základní zapojení (klopný obvod R-S, S-R lath)

<img src=Images/SRlatch.jpg>

S - Set (stačí zapnout impulzem, neboť nastavením na 1 dochází k aktivaci paměti)
R - Reset (prohazuje stavy Q a Qnot, tedy prohazuje výstup z nula na jedna a naopak)
1-1 je zakázaný stav, neboť není možné určit v jakém stavu je Q (nestabilní poloha, stav závisí na perturbacích a nestabilitách)

Toto zapojení umožňuje vytvoření datové buňky (Klopný obvod typu D)

<img src=Images/SRlatchD.jpg>

V případě Kdy vstup (C), tj. (enabled) je nastaveno na hodnotu 1, pak zapojení ukládá hodnotu D do hodnoty Q. Po tomto nastavení SR latche (tj. uložení hodnoty) je možné (enabled) vstup vypnout, a hodnota Q zůstane stejná, a nebude reagovat na D (datový vstup), tj. hodnota Q bude nadále ukládat uloženou hodnotu, dokud se opět nezapne vstup (enabled, C) pro nový proces uložení vstupu D do paměti (Q). 

Toto zapojení ukládá informaci 1 bit. Pomocí sekvence takových datových buněk lze uložit větší množství dat.

Jak funguje kondenzátor a vstup C?
