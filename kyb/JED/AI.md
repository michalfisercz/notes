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

### 1. Učení s učitelem *(Supervised Learning)*  
- Systém se učí z **dat označených štítky (labely)**.  
- Trénovací sada obsahuje dvojice **[datový vektor, label]**.  
- Label udává správné řešení, které systém napodobuje.  
- Po natrénování systém dostává pouze **data** a na jejich základě **predikuje výsledek**.  
- **Přesnost modelu** se vyhodnocuje takto:
  1. Data se **promíchají** (aby se odstranila systematická chyba).  
  2. Rozdělí se na **trénovací** a **testovací** sadu (např. 9:1 nebo 8:2).  
  3. Model se natrénuje na trénovací sadě a **ověří** na testovací.  
  4. Porovnání výsledků s testovacími daty určí **přesnost modelu**.  
  5. Porovnání s trénovacími daty je **neobjektivní** – model by je už „znal“.  

---

### 2. Učení bez učitele *(Unsupervised Learning)*  
*(poznámka: zatím bez rozpracování – zde lze doplnit např. klastry, PCA, apod.)*

---

### 3. Učení posilováním *(Reinforcement Learning)*  
*(poznámka: zatím bez rozpracování – zde lze doplnit princip odměny a trestu, např. Q-learning.)*
