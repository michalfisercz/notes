# Kybernetika

## Definice
Kybernetika je věda zabývající se obecnými principy řízení a přenosem informace ve strojích a živých organismech.

- **Princip zpětné vazby**  
  ![Regulátor s konstantním zesílením](regulator_1.png)

---

## Kybernetika se zabývá například:
- Automatické řízení  
- Přenos informace  
- Konstrukce robotů  
- Živé organismy  
- Komunikace, spolupráce a interakce člověka a stroje  

---

## Základní kybernetické principy a přístupy

### Systémový přístup
- Systématické studium různých systémů → poznatek, že systémy různé fyzikální podstaty mohou mít podobné chování.  
- Lze je popsat stejnými diferenciálními rovnicemi.  
- **Různé fyzikální podstaty → stejný matematický popis → stejné rovnice použitelné na různé systémy.**

### Informační přístup
- Vznik exaktní teorie informace jako odnože teorie pravděpodobnosti.  

### Řídící přístup
- Základ zpětnovazební regulace.  

---

## Klasifikace kybernetiky

- Teoretická kybernetika  
  *teoretický základ oboru*
  
- Experimentální  
  *studium reálných procesů prostřednictvím jejich modelů*
  
- Technická  
  *konstrukce a využití technických kybernetických systémů (systémy pro přenos informace, tvorba manipulátorů a robotů)*
  
- Aplikovaná  
  *aplikace kybernetiky v jiných oblastech (biokybernetika, lékařská kybernetika, sociální sféra, ekonomika*

---

# Systém

### Definice
Jakýkoli proces, objekt nebo uspořádání komponent, který přijímá vstup a přeměňuje jej na výstup prostřednictvím vnitřní dynamiky.

### Teorie řízení
- Soubor komponent nebo prvků, které mezi sebou interagují podle určitých pravidel.  
- Systém přijímá jeden nebo více vstupů a produkuje jeden nebo více výstupů.  
- Vnitřní dynamika zajišťuje, jak je vstup přeměněn na výstup.  

---

## Klasifikace systémů

1. **Orientované vs. Neorientované**
   - **Orientované** – mají jasně definovaný směr interakce (vstupy → výstupy).  
     - Příklad: řídicí systém, jednosměrný proces (výbuch bomby, entropie).  
   - **Neorientované** – postrádají jasný směr interakce.  

2. **Kauzální vs. Nekauzální**
   - **Kauzální** – výstup závisí pouze na minulých a současných vstupech.  
   - **Nekauzální** – výstup závisí i na budoucích vstupech (teoretické, nereálné).  

3. **Deterministické vs. Stochastické**
   - **Deterministické** – chování je plně předvídatelné na základě počátečních podmínek.  
     - Příklad: kyvadlo ve vakuu.  
   - **Stochastické** – obsahují náhodnost, výstup nelze přesně předpovědět.  
     - Příklad: ceny akcií, počasí.  

4. **Dynamické vs. Statické**
   - **Dynamické** – výstup závisí na čase a minulém chování (mají paměť).  
     - Popsány diferenciálními rovnicemi.  
     - Příklad: tlumení kol auta.  
   - **Statické** – výstup závisí pouze na aktuálním vstupu (bez paměti).  
     - Popsány algebraickými rovnicemi.  
     - Příklad: odpor (U = R·I).  

---

## Vnější popis systému
Systém lze popsat:
1. Diferenciálními rovnicemi  
2. Přenosovými funkcemi  

### Charakteristiky systému
- **Skoková změna**  
  - Přechodová funkce (vstup)  
  - Přechodová charakteristika (odpověď)  

- **Impulsní změna**  
  - Diracův puls (nekonečně vysoký, nekonečně úzký v čase 0).  
  - Po pulsu návrat do původního stavu.  
  - $$\int \delta(x)\,dx = 1$$  
  - Impulsní charakteristika.  

---

# Systém 1. řádu
- Plynulá reakce na změnu.  
- Asymptoticky se blíží požadované hodnotě.  
- Parametr: **časová konstanta τ**.  
- **Doba ustálení** – čas, kdy se systém dostane do určité tolerance (např. 2 %).  
- Diferenciální rovnice:  
  $$\tau \frac{dy(t)}{dt} + y(t) = K u(t)$$  
- Odezva:  
  $$y(t) = K(1 - e^{-\frac{t}{\tau}})$$  
- Příklady: RC obvod, tepelný výměník, nádrž s kapalinou.  

![Charakteristika 1. řádu](charakteristika1radu.png)  

---

# Systém 2. řádu
- Složitější než systém 1. řádu, popisuje širší chování.  
- Může kmity kolem nové hodnoty.  
- Parametry:  
  - **Přirozená frekvence**  
  - **Koeficient tlumení**  

![Charakteristika 2. řádu](charakteristika2radu.png)  

### Klíčové metriky
- **Doba dosažení špičky $(t_p)$** – čas k dosažení první maximální hodnoty.  
- **Maximální překmit** – o kolik % výstup překročí ustálenou hodnotu.  
- **Doba ustálení $(t_s)$** – čas potřebný k ustálení v toleranci (2 %–5 %).  
- **Doba nárůstu $(t_r)$** – čas vzestupu z 10 % na 90 % hodnoty.  

### Výskyt ve fyzice
- RLC nebo LC obvod  
- Kyvadlo (pro malé úhly)  
