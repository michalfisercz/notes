
# 1) Čítač

## 🔢 Čítače: Teorie a principy

Čítač (anglicky *counter*) je základní stavební prvek digitální techniky a informatiky, určený k zaznamenávání počtu výskytů určitého jevu nebo impulzu, tj. počítá od n do m. V praxi se s ním setkáváme ve třech hlavních podobách:

### 1. Hardwarový (Digitální obvody)

Sekvenční logický obvod složený převážně z J-K klopných obvodů. Každý vstupní impulz změní vnitřní stav obvodu, což navenek odpovídá binárnímu nárůstu hodnoty.

**Využití:** Digitální hodiny, děličky kmitočtu, čítače adres v procesoru.

### 2. Softwarový (Programování)

Proměnná (často označená jako `i` nebo `counter`), která se inkrementuje (zvyšuje o 1) uvnitř cyklů nebo při zachycení specifické události v kódu.

**Příklad:**
```python
count = count + 1
```

### 3. Průmyslový (Automatizace)

Funkční bloky v rámci PLC systémů, které zpracovávají signály ze senzorů (např. průchod výrobku na pásu).


#### Zapojením více J-K klopných obvodů lze získat více výstupů s polovičními frekvencemi.

<img src=Images/citac1.jpg>


#### Sledováním všech výstupů v každém tiku hodinu (v okamžiku 0 ->1 přechod) zjišťujeme, že série výstupních hodnot tvoří binární číslo, které v každém tiku hodin narůstá/klesá. 

<img src=Images/citac2.jpg>


###### Toto zapojení může tvořit čítač, který počítá např. od 1 do 10. 

# 2) Časovač

Čítač se strukturovaným vstupem (odpovídá reálnému času, např. f = 1 Hz), a s omezením (tj. hodnota při které se čítač ukončí.)
Kritická hodnota pro ukončení je uložená v registru pomocí více vstupů, tedy jako binární hodnota. 

<img src=Images/casovac.jpg>

# 3) Přerušení 

<img src=Images/preruseni.jpg>

Přerušení je obecně funkce, která se zavolá za určitých podmínek (např. vypršení časovače). 
Při zavolání funkce procesor přeruší veškeré vyhodnocování kódu, a soustředí se na Interrupt.



"Příští týden chceme navázet na interupty přes PWM" '!!!!'




