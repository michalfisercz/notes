## 🧠 Definice Umělé Inteligence

> **AI = Studium toho, jak umožnit strojům jednat tak, aby jejich chování mohlo být považováno za inteligentní (1995).**

---

### 💡 Ale co je to inteligence?
- **1950 – Alan Turing** navrhl **Turingův test**, který zkoumá, zda lze rozpoznat, zda odpovědi pochází od člověka nebo stroje.

---

## 🤖 Umělá inteligence

Rozlišujeme dva základní typy AI:  
- **Narrow (slabá, úzká) AI**  
- **General (silná, obecná) AI**

---

### 1️⃣ Narrow AI  
*(úzce zaměřená umělá inteligence)*  

1. Zaměřena na konkrétní úkoly nebo oblasti.  
2. Základním principem je **strojové učení** – učení se na základě dat.  
3. Nemá schopnost **generalizace** mimo definovaný rámec.  
4. **Příklady:** computer vision, LLMs, machine learning algoritmy, hlasoví asistenti.  
5. **Výhody:**
   - Vysoce efektivní při řešení specifických problémů.  
   - Bezpečnější než obecná AI – nemůže překročit dané hranice.  
6. **Nevýhody:**
   - Neschopnost učit se mimo úzce definovanou oblast.  
   - Závislost na velkém množství dat.  
   - Omezená flexibilita a nepochopení širších souvislostí.  

---

### 2️⃣ General AI  
*(obecná umělá inteligence)*  

1. Cíl: vytvořit systémy schopné **obecné inteligence** – učit se, myslet, uvažovat, rozhodovat se.  
2. Umí vykonávat širokou škálu úkolů, řešit neznámé problémy a **generalizovat** znalosti.  
3. Dokáže napodobit, nebo dokonce **překonat člověka**.  
4. **Výhody:**
   - Přizpůsobivost novým úkolům bez nutnosti přeprogramování.  
5. **Nevýhody:**
   - Extrémní technická náročnost.  
   - Současná (slabá) AI je zatím velmi vzdálená teoretickému cíli GAI.  
   - Závažné **etické otázky**.  

---

## 🔁 Strojové učení vs. Umělá inteligence

- Veškerá AI využívá **proces učení na datech**.  
- **Strojové učení (Machine Learning)** je **podmnožinou AI**.  

---

## 📘 Typy učení

## 1. Učení s učitelem *(Supervised Learning)*  
- Systém se učí z **dat označených štítky (labely)**.  
- Trénovací sada obsahuje dvojice **[datový vektor, label]**.  
- Label udává správné řešení, které systém napodobuje.  
- Po natrénování systém dostává pouze **data** a na jejich základě **predikuje výsledek**. 
- lineární regrese
- **Přesnost modelu** se vyhodnocuje takto:
  1. Data se **promíchají** (aby se odstranila systematická chyba).  
  2. Rozdělí se na **trénovací** a **testovací** sadu (např. 9:1 nebo 8:2).  
  3. Model se natrénuje na trénovací sadě a **ověří** na testovací.  
  4. Porovnání výsledků s testovacími daty určí **přesnost modelu**.  
  5. Porovnání s trénovacími daty je **neobjektivní** – model by je už „znal“.  
- regrese, klasifikace
- Regrese = lineární fit
- Klasifikace:
### Klasifikace: k-NN (k-Nearest Neighbors)

**k-nejbližších sousedů** je jeden z nejjednodušších, ale velmi účinných algoritmů strojového učení.

#### Princip fungování

- **Učení s učitelem (Supervised Learning):** Algoritmus pracuje s daty, která již mají přiřazené správné labely (třídy).
    
- **Líný algoritmus (Lazy Learning):** Na rozdíl od jiných modelů netvoří během trénování žádnou matematickou funkci. Pouze si „zapamatuje“ všechna tréninková data a veškeré výpočty provádí až ve chvíli, kdy dostane nový bod ke klasifikaci.
    
- **Logika rozhodování:** Nový datový bod je vložen do prostoru a algoritmus vyhledá $k$ nejbližších sousedů. Bod je pak přiřazen do té třídy, která má mezi těmito sousedy většinu.
    

---

#### Klíčové parametry

##### 1. Parametr $k$

Určuje, kolik sousedů ovlivňuje výsledek. Výběr správného $k$ je kritický pro přesnost modelu:

- **Malé $k$ (např. 1):** Model je velmi citlivý na šum v datech. Hrozí **overfitting** (přeučení).
    
- **Velké $k$:** Model se stává příliš robustním a ignoruje lokální vzorce. Hrozí **underfitting** (nedostatečné naučení).
    
- **Tip:** Obvykle se volí **liché číslo**, aby se předešlo remíze při hlasování o třídě.
    

##### 2. Metrika vzdálenosti

Určuje, jakým způsobem měříme „blízkost“ bodů v prostoru.

- **Eukleidovská vzdálenost:** Nejpoužívanější (přímá čára mezi body).
    
- **Manhattanská vzdálenost:** Součet absolutních rozdílů souřadnic.

---

## 2. Učení bez učitele (Unsupervised Learning)

V tomto režimu algoritmus pracuje s daty, která **neobsahují žádné štítky** (labely) ani „správná řešení“. Model se snaží sám najít skryté struktury, vzorce nebo podobnosti.

- **Cíl:** Nejde o predikci konkrétní hodnoty, ale o **pochopení vnitřní struktury dat**.
    
- **Analogie:** Představte si, že dostanete krabici plnou různých mincí z celého světa, aniž byste věděli, co jsou zač. Vaším úkolem je roztřídit je podle velikosti, barvy nebo materiálu.

### Hlavní úlohy a metody

#### 1. Shlukování (Clustering)

Rozděluje data do skupin (shluků) tak, aby si objekty uvnitř jedné skupiny byly co nejvíce podobné a objekty z různých skupin co nejvíce odlišné.

- **Příklady:** Segmentace zákazníků (marketing), seskupování podobných zpráv v Google News, analýza genů.
    
- **Klíčové algoritmy:** * **K-Means:** Rozděluje data do předem určeného počtu $k$ shluků.
    - **DBSCAN:** Hledá shluky na základě hustoty bodů (skvělé pro nepravidelné tvary).
    - **Hierarchické shlukování:** Vytváří stromovou strukturu (dendrogram) vztahů.
    
```
		### **2Shlukování (K-Means)**

Metoda **K-Means** je nejpoužívanějším algoritmem pro shlukování dat, u kterých předem neznáme správné řešení (nemáme labely).

#### **Základní princip**

- Algoritmus rozděluje data do **$K$ shluků** (skupin).
    
- Cílem je, aby body uvnitř jednoho shluku byly co nejblíže svému středu (**centroidu**) a zároveň co nejdále od bodů v jiných shlucích.
    

#### **Algoritmus v 5 krocích**

1. **Volba $K$:** Určíme počet shluků (např. chci rozdělit zákazníky do 3 skupin).
    
2. **Inicializace:** Algoritmus náhodně umístí $K$ centroidů do prostoru mezi data.
    
3. **Přiřazení:** Každý datový bod se přiřadí k nejbližšímu centroidu.
    
4. **Aktualizace:** Centroidy se přesunou do skutečného geometrického středu svých nových skupin.
    
5. **Opakování:** Kroky 3 a 4 se opakují, dokud se pozice centroidů neustálí.
    

#### **Příklad: Segmentace zákazníků**

- **Vstup:** Data o útratě a věku 1000 lidí (bez informace, kdo je kdo).
    
- **Proces:** K-Means najde shluky (např. "mladí s vysokou útratou", "senioři s nízkou útratou").
    
- **Výstup:** Algoritmus body jen očísloje (Shluk 0, Shluk 1). **Interpretace a pojmenování** skupin je na člověku.
``` 

#### 2. Redukce dimenzionality (Snížení dimenze)

Proces zjednodušení dat s velkým počtem vlastností (sloupců) při zachování co nejvíce důležitých informací.
- **Využití:** Vizualizace složitých (vícerozměrných) dat, odstranění šumu a zrychlení dalších výpočtů.
- **Hlavní metoda:** **PCA (Principal Component Analysis)** – analýza hlavních komponent.
    

#### 3. Asociační pravidla

Hledání zajímavých souvislostí a korelací mezi proměnnými ve velkých databázích.
- **Princip:** „Pokud nastane jev A, s velkou pravděpodobností nastane i jev B.“
- **Využití:** Analýza nákupního košíku (Cross-selling). Klasický (možná i městská legenda) příklad: Pivo a plenky – lidé kupující plenky v pátek večer často přihodí i pivo.

---

## 3. Učení posilováním *(Reinforcement Learning)*  
- zpětnovazebné učení
- Nemáme informaci o jednom datovém bodu zda je správný, ale máme informaci o shluku více datových bodů.
- Nejdříve musíte něco udělat, a pak se dozvíte zda je to dobré. Metoda pokus omyl. Specifické algoritmy se pouze snaží optimalizovat metody odhadu, abychom k výsledku došli nejrychleji, a výpočetně nejlevněji.
- příklad: Piškworky. Nedokážeme vyhodnotit, zda je jednotlivý specifický tah správný (není učitel), ale po určité sekvenci tahů, jsme schopni vyhodnotit, zda tato posloupnost tahů vedla k výhře či ne. Tj. zpětnovazebné učení.
- Učení probíhá pomocí různých algoritmů
	- např. Genetické algoritmy, kdy simulujeme evoluci datových shluků, když je necháme mezi sebou náhodně křížit, každému datovému shluku přiřazujeme skóre, a v dalších generací křížíme pouze shluky s největším skórem, tj. princip evoluce. 
	- Touto metodou slepě hledáme řešení, bez znalosti skryté dynamiky systému.
- Další metody řešení těchto problémů
	- Dijkstrův algoritmus - řeší problém hledání cesty na specifickém grafu, který vypadá jako mapa čtverečků se začátkem a cílem. Každý čtvereček má svou hodnotu = "cenu", která může např. určovat náročnost cesty daným směrem.
	- A* algoritmus - Odhaduje. Využívá heurestiku. Např. chess engine, tj. při hledání v grafu odhaduje hodnotu jednotlivých pozic pomocí vzdušných čar. Podobné jako Dijkstrův algoritmus
- Prohledávání do šířky, do hloubky
- Mnohé další