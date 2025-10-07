# Logické funkce a jejich vlastnosti

Činnost logických obvodů lze popsat pomocí symbolického jazyka, který vychází z výrokové logiky.

**Výrokem** rozumíme tvrzení o kterém má smysl říci, že je pravdivé nebo nepravdivé.

- Pravdivému výroku přiřazujeme hodnotu *logické jedničky*.
- Nepravdivému výroku přiřazujeme hodnotu *logické nuly*.
- Jednotlivé výroky jsou reprezentovány *logickými proměnnými*.

**Logickou funkcí** nazveme funkční přiřazení mezi nezávislými logickými proměnnými.

Logickou funkci lze vyjádřit:

- algebraickým výrazem
- pravdivostní tabulkou
- mapou logické funkce
- logickým schématem

- Každá funkce může být vyjádřena pomocí úplného souboru funkcí (negace, konjunkce, disjunkce)
- Minimální soubor funkcí = negace + konjunkce, nebo negace + disjunkce
### Funkce dvou proměnných
- $f(A, B)$
- nulová funkce $f_0$ = 0
- jednotková funkce $f_1$ = 1
- logický součin ($\land$/and) $f_2 = A \cdot B$  
- logický součet ($\lor$/or) $f_3 = A + B$ 
- exkluzivní or (XOR) - OR, ale A nesmí být rovno B

Obor hodnot Booleovy algebry = 0, 1
Operace (+, $\cdot$, negace (bar))

### Zákony Booleovské algebry

1. Komutativnost $A + B = B + A$
2. Asociativnost $(A + B) + C = A + (B + C)$
3. Distributivní (násobeční sčítanců, ale i sčítání násobenců)
	1. Lze roznásobit a ROZČÍTAT závorku
	2. $A + (B \cdot C) = (A + B)\cdot (A + C)$
4. Zákon negace negace (negace negace A = A)
5. Agresivnost a neutrálnost 1 a 0
	1. 1 je agresivní při sčítání (neutrální při násobení)
	2. 0 je agresivní při násobení (neutrální při sčítání)
6. Zákon tautologie
	1. $x + x = x$
	2. $x \cdot x = x$
7. Zákon vyloučení třetího a logický rozpor
	1. $x + \bar{x} = 1$
	2. $x \cdot \bar{x} = 0$
8. Zákony absorpce
	1. Odvoditelné!
	2. Zákon absorpce negace: $a + \bar{a}b = a + b$
9. De Morganovy zákony
	1. $\bar{(x\cdot y)} = \bar{x} + \bar{y}$
	2. Prohazujeme vše, a výraz stále platí
	
	
### Karnaughova mapa (K-map)

- je grafická metoda používaná k minimalizaci logických výrazů v Booleově algebře. Pomáhá jednoduchým a přehledným způsobem redukovat složité logické funkce na jejich nejjednodušší podobu. Tato metoda je zvláště užitečná při návrhu logických obvodů.
- Karnaughova mapa je tabulka, kde každé pole odpovídá určité kombinaci hodnot vstupních proměnných. Pole jsou uspořádána tak, aby se sousední pole lišila vždy pouze v jedné proměnné (Grayův kód). Pro n proměnných má mapa 2n polí.

### Postup minimalizace pomocí Karnaughovy mapy

- Nakreslení Karnaughovy mapy odpovídající počtu proměnných.
- Zapsání hodnot logické funkce (0 nebo 1) do příslušných polí mapy podle hodnot vstupních proměnných.
- Seskupení jedniček (1) do co největších obdélníkových nebo čtvercových bloků.
  - Bloky musí mít velikost mocniny čísla 2 (1, 2, 4, 8 atd.).
  - Bloky mohou být vodorovné nebo svislé (nikoliv diagonální).
  - Karnaughova mapa je nekonečná, což znamená, že levý a pravý okraj, stejně jako horní a dolní okraj, jsou spojeny.
  - Bloky se mohou (částčně) překrývat. 
  - Každá jednička (1) musí být v nějakém bloku
  - Počet bloků musí být co nejmenší. (Bloky musí být co největší)
- Zapsání minimalizovaného výrazu na základě seskupených bloků.

> Poznámka:
> pokud seskupujem do bloků jedničky (1), vzniká zápisem disjuktní normální forma (součet součinů). Můžeme rovněž seskupovat nuly (0), pak vzniká konjuktní normální forma (součin součtů).

<img src=Images/Karnaugh_example.png>