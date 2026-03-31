
### Histogram intenzity

<img src=Images/exposure.jpg>
Díky našim technologiím sledujeme konstantně rozsah 0 - 255. Pokud křivka histogramu leží mimo tuto mez, dochází ke ztrátě informace (podsvícení, přesvícení).

V histogramu intenzit můžeme použít segmentaci prahováním. Např. v intenzitním histogramu zelené barvy, za použití zeleného pozadí na fotce, lze oddělit hlavní peak od zbytkového šumu, a oddělit popředí od pozadí (lze smazat pozadí).

#### Konvoluce

Metoda computer vision pro zpracování obrázku a detekce objektů.
Obrázek je reprezentován maticí (popř. tenzorem) čísel n x n x d, kde d = 3 pro rgb.
Je dáno konvoluční jádro, které má rozměr m x m, kde n bývá mnohem větší než m, neboť dochází ke snižování rozměrů původního obrázku. Konvoluční jádro se posouvá po původním obrázku, po jeho částech, které mají stejný rozměr jako konvoluční jádro. Pro každý takový segment spočítá dot product, a určený (většinou středový) pixel v dané oblasti nahradí hodnotou tohoto sčítání- násobení. Speciální konvoluční jádra slouží např. k detekci hran atd. 
Konvoluční jádro pro detekci vertikálních hran:
[-1, 0, 1
-2, 0, 2
-1, 0, 1]

##### Konvoluční vrstva neuronové sítě 

Máme definovanou velikost jádra (3x3, etc.), a zároveň počet takových jader. - Definice konvoluční vrstvy
Hodnoty jádra se zpravidla inicializují náhodně.
Účelem sítě je najít optimální hodnoty jader tak, aby byla požadovaná data z obrázku správně extrahována.

Vstupem sítě je obrázek, konvoluční vrstva jako výstup vrátí počet obrázků, který odpovídá počtu jader, kde každý výstupní obrázek bude mít trochu menší rozměr m (m<n). Při použití těchto obrázků jako vstupů do další konvoluční vrstvy, se dimenze výstupu násobí, neboť pro každý vstupní obrázek se počet výstupů vynásobí počtem jader.
Př. 
n = 100; n1 = 98; n2 = 96; n3 = 94 (pro velikost jádra 3 x 3)
počet jader = 10 -> počet výstupů z jednoho obrázku po průchodu jednotlivými konvolučními vrstvami: 10, 100, 1000, 10000, ...  $10^n$

###### Pooling

Narozdíl od konvoluce, není závislý na hodnotách jádra, jde o filtr, který snižuje dimenzionalitu obrázku, z určité oblasti obrázku definované velikostí jádra přiřazuje dané oblasti typickou hodnotu danou specifikací filtru. 
Typické hodnoty:
1) Maximální hodnota (max pooling)
2) Střední hodnota (mediánový pooling)
3) Average pooling

Často používaný ve vrstvách neuronových sítí.
Příklad konvoluční sítě:

<img src=Images/convolucni_sit.png>

Na obrázku je vidět, že v konvolučních vrstvách neuronových sítí dochází ke snížení rozměrů obrázku, až na jediný "pixel", který má ale obrovskou "hloubku", nahrazujeme tedy plochu obrázku tloušťkou výsledného políčka, a reprezentujeme obrázek jedním vektorem vlastností.
Konvoluční sítě jsou užitečné, protože dokáží plošnou informaci obrázku přenášet dál efektivně. Kdybychom použili klasické fully-connected sítě, měli bychom extrémně moc parametrů.

