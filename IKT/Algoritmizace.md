## Definice algoritmu 

Algoritmus je popis kroků, které musíme realizovat, abychom dosáhli výsledku.

Pojem algoritmu se nejčastěji objevuje při programování, kdy se jím myslí teoretický princip řešení problému (oproti přesnému zápisu v konkrétním programovacím jazyce)

## Vlastnosti algoritmu

1. elementárnost
	- postup je složený z tak jednoduchých kroků, ...
2. determinovanost
	- v každém okamžiku musí být jednoznačně jasné, jaký další krok bude následovat, nebo zda již postup skončil
3. konečnost a rezultativnost
	- výpočet vždy skončí po konečném počtu kroků výsledkem
4. hromadnost
	- algoritmus je použitelný pro celou skupinu přípustných vstupních dat
	- "pro stejnou kvadratickou rovnici vyhodí algoritmus vždy stejné kořeny"
5. efektivnost 
	- výpočet se uskuteční v co nejkratším čase a s využitím co nejmenšího počtu prostředků
	- dnes s výkonnými počítači se moc neřeší

## Způsoby zápisu algoritmů 

- graficky orientované algoritmické jazyky
	- vývojové diagramy (Flowgorithm)
	- strukturogramy
	- obrázkové jazyky (Scratch)
- textově orientované alg. jazyky
	- slovní zápis v mateřském jazyce
	- zápis v programovacím jazyce

## Základní algoritmické struktury

- Sekvence = posloupnost příkazů, jeden příkaz následuje druhý
- Větvení programu s podmínkou (if)
- Cyklus = opakování jednoho nebo více příkazů pořád kolem dokola (for, while, do while)

## Vývoj programovacích jazyků

Programovací jazyky se historicky dělí do generací podle úrovně abstrakce a způsobu, jakým komunikují s hardwarem.

1. generace (1GL) - Strojový kód
	- Přímo binární instrukce (např. 10110000 011 00001)
	- Prováděný přímo procesorem
	- Extrémně rychlé, ale velmi obtížné na psaní a údržbu
2. generace (2GL) - Asemblery
	- Symbolické instrukce (např. MOV AL, 61h)
	- Každý příkaz odpovídá jedné instrukci
	- Nutný překladač
3. generace (3GL) - Vysoce úrovňové jazyky
	- Abstrakce od hardware, snadno čitelné pro člověka
	- Příklady: C, C++, Java, Python, Pascal
	- Kompilují nebo interpretují se do strojového kódu
4. generace (4GL) - Jazyky zaměřené na problém
	- Navrženy pro specifické úlohy (např. databáze, reporty)
	- Příklady: SQL, MATLAB, R, SAS, chatGPT
	- Vyšší produktivita, méně kódu
5. generace (5GL) - Logické a deklarativní jazyky
	- Zaměřené na umělou inteligenci a řešení problémů bez algoritmů
	- Prolog, Mercury
	- Používají se v expertních systémech, AI výzkumu

## Rozdělení programovacích jazyků

1. kompilované programovací jazyky (např. Algol, Fortan, Colol, C, Java)
	- před spuštěním jsou nejprve kompletně přeloženy kompilátorem
	- výsledkem je větší rychlost, ale také větší náročnost na správně zapsaný kód
2. interpretované programovací jazyky (např. BASIC, PHP, Python, Shell)
	- program se překládá a provádí řádek po řádku, je proto pomalejší
3. programovací jazyky s virtuálním strojem
	- Java
	- .java = zdrojový program, ten se zkompiluje do souboru .class
	- .class = bytekód neboli mezikód, ten se interpretuje pomocí virtuálního stroje
	- výhody: snadná přenositelnost mezi operačními systémy


