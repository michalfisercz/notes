
Analogový signál -> nabývá všech hodnot
Digitální signál -> nabývá pouze 0 a 1

ADC a DAC - Analog to digital converter 

# AD

Idea: Máme spojitý analogový signál, chceme ho diskretizovat do diskrétních hodnot, abychom měli digitálně reprezentované hodnoty (0 a 1)

<img src=Images/multiplexor.jpg> 


V případě jednoho pinu mámu pouze hodnoty 0, 1.

použitím více pinů, např. 3, můžeme získat větší rozpětí hodnot, (0-7 pro 3 piny)

Pro diskretizaci porovnáváme analogový signál s určitými hodnotami napětí

<img src=Images/comparator.jpg> 


##### Signál -> Komparátor -> D flipflop -> multiplexor

Komparátor -> Porovnává zda analogová hodnota dosáhla určité zdiskretizované hodnoty
D flipflop -> Uloží "obrázek" výstupů ze všech komparátorů v jeden konkrétní čas, protože analogový vstup se mění v čase.  Uložený obrázek pak může přečíst počítač. 

Multiplexor -> Jednotlivé výstupy komparátorů jsou použity jako jednotlivé vstupy do multiplexoru, multiplexor vybere pin s nejvyšším číslováním, který má hodnotu 1, a převede číslo tohoto pinu do binární reprezentace (pin č. 3 má hodnotu jedna, výstupem bude 011).
-> Kvantizace napětí

## 1) Komparační převodník
   
   Pro každou diskretizovanou hodnotu používáme jeden komparátor. Každý komparátor porovnává signál pro jinou hodnotu diskretizace (0-7), typově: Je signál větší než 4?

<img src=Images/AD1.jpg>
 Poznámka: Napěťová reference v tomto zapojení je stejná pro všechny komparátory, kvůli stabilitě napětí, ale místo reference se mění (resp. dělí) signál pomocí rezistorů, čímž se efektivně dosahuje stejného výsledku, kdy každý komparátor porovnává zlomek napětí signálu s referencí, což je stejné jako kdyby porovnával signál s násobkem reference.  


## 3) Integrační převodník

 Využíváme jeden komparátor, kterému dynamicky mění porovnávací hodnotu pro signál, tím že do + svorky posíláme pilový signál, generovaný pilovým generátorem. Pilový generátor postupně zvyšuje napětí a porovnává, kdy jeho hodnota překročí hodnotu signálu.
	
<img src=Images/pila.jpg>

	  
V momentě překročení se zastaví čítač, a z poměru času kdy výstup byl 0 a celkového času jednoho úseku pily (závisí na frekvenci pilového signálu), lze dopočítat hodnotu napětí signálu. Čítač uloží hodnotu do registru. Rozlišení závisí na frekvenci pilového signálu a frekvenci čítače (jeho hodinového signálu).

<img src=Images/AD2.jpg>
Poznámka: Pinem START spustíme cyklus, čímž:
1) pilový generátor začne generovat signál (rostoucí napětí)
2) resetuje se flipflop, resp. nastaví se Q na logickou nulu, tedy $Q_{not}$ na logickou 1, čímž AND začne být propustný, a oscilátor (hodiny) umožní čítači počítat
3) čítač začne počítat

Napětí na svorce + komparátoru začne růst, a když dosáhne hodnoty signálu tak se komparátor sepne na logickou 1, čímž se flipflop nastaví na logickou 1 a dá znamení že je hotovo. Zároveň $Q_{not}$ spadne na logickou 0, čímž se zablokuje AND, a čítač přestane počítat. Poslední hodnota čítače se uloží do datové digitální sběrnice, čímž získáme informaci o čase v rámci jednoho pulzu pilového signálu kdy došlo k překročení. Z toho můžeme dopočítat v jaké části pilového úseku k přerušení došlo, a tedy i analogovou hodnotu napětí, kterou lze uložit do digitální podoby.


# DA

Digitální (diskretizované) hodnoty signálu (např. napětí) převádíme na analogový signál (hodnoty neomezené, reálné, nabývající všech hodnot)

##### Dělič napětí:

<img src=Images/separator.jpg>

Zapojení uvedené výše využívá rezistor, na kterém vzniká úbytek napětí, čímž obvod funguje jako dělič napětí.

#### Princip DA převodníku

Když zapojíme více děličů napětí do paralelních větví (více rezistorů), a přidáme do každé větve spínací tlačítko, které buďto větev uzemňuje nebo nechává viset ve vzduchu, můžeme pomocí stavu tlačítek (s1, s2) konfigurovat výstupní napětí. Jelikož stav tlačítek lze reprezentovat binárně (00, 01, 10, 11, celkem $2^n \to 2^2$ kombinací), a výstupní napětí je analogové, pak zařízení funguje jako převodník digitální hodnoty na analogovou. Aby konfigurace tlačítek reprezentovaná binárně správně odpovídala digitální hodnotě napětí, musíme použít speciální používané zapojení (viz dále).


<img src=Images/DAprinciple.jpg>

Poznámka: Když jednu z paralelních větví odpojíme (tj. rozepneme tlačítko), tak větev bude "viset ve vzduchu", nebudu spojená se zemí, a nebude způsobovat úbytek napětí. Když sepneme obě tlačítka, budeme sčítat převrácené hodnoty odporů.

#### Schéma zapojení DA

<img src=Images/DA.jpg>

Při převádění digitálních hodnot napětí na analogové, máme zdroj napětí AVDD (stabilní zdroj). AVDD (např. 5 V) určuje rozsah analogových hodnot napětí, kterých jsme schopni dosáhnout (zpravidla méně než 5 V, např. 4.6). Sepínáním jednotlivých kontaktů A-D si vybíráme, zda každý rezistor zapojíme na zdroj (+), nebo zem (-). Jednotlivé větve jsou zatíženy sériově zapojenými rezistory nahoře, čímž se snižuje "váha" hlubších větví, směrem dále od výstupu (vpravo). Např. když necháme na zdroj připojený pouze kontakt D, a ostatní připojené na zem, výstupní napětí bude zhruba 2,5 V. Sepnutí/rozepnutí jednotlivých kontaktů rozhoduje o tom, zda daná větev zvětší/zmenší výstupní napětí, s tímže vzdálenější větve mají menší vliv. Tato skutečnost je názorně zachycena na bifurkačním diagramu na horní části tabule. Tím že měním spínač D, ovlivňujeme onen první nejvýraznější skok (zda bude nahoru či dolu). Další rozcestí odpovídají sepnutí/rozepnutí dalších kontaktů (A-C).



