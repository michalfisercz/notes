PID = Proporcionální, Integrační, Derivační
PID regulace je spojitá regulace.
# Regulátor s konstantním zesílením (P-regulátor)

![Regulátor s konstantním zesílením](RegulatorP.png)

## Popis
- Na vstupu regulátoru je **regulační odchylka** (chyba = rozdíl mezi požadovanou a aktuální hodnotou).  
- Výstup regulátoru je přímo úměrný odchylce:  
  
  $$u(t) = K_{p}  \cdot e(t)$$
  
  kde:
  - $u(t)$ = výstup regulátoru  
  - $e(t)$ = regulační odchylka  
  - $K_{p}$ = konstantní zesílení regulátoru  

## Vlastnosti
- Jedná se o **nejjednodušší typ regulátoru**.  
- Regulátor **zesiluje chybu**, ale nijak neakumuluje ani nepamatuje minulost.  
- Při **konstantním rušivém působení** (např. odporová síla, tření) se výsledná hodnota **ustálí s trvalou regulační odchylkou** (chyba ≠ 0).  
- Regulátor pouze **zamezuje dalšímu poklesu** a udržuje systém poblíž požadované hodnoty, ale ne na ní přesně.  

![image](regulator_1_odezva.png)

## Výhody
- Jednoduchost, snadná realizace.  
- Rychlá reakce na změny.  

## Nevýhody
- **Statická chyba** – systém nikdy přesně nedosáhne požadované hodnoty, pokud působí trvalá porucha.  
- Není vhodný pro přesné ustálení.  

## Klasifikace
- Řadí se mezi **statické regulátory**.  
- Samotný regulátor s konstantním zesílením nemění řád soustavy – výsledný řád systému závisí na řízené soustavě (může být 1. nebo 2. řádu podle modelu řízené části).  

## Použití
- Vhodný tam, kde **nevadí malá trvalá chyba** (např. jednoduché zesílení signálu, základní stabilizace).  
- Často se používá jako **součást složitějších regulátorů** (např. P-regulátor v PID regulaci).  


---


# Integrační regulátor (I-Regulátor)

1. Diferenciální rovnice
	- Integrační regulátor vytváří výstup, který závisí na integrálu chyby. Výstup se neustále zvyšuje nebo snižuje v závislosti na tom, zda je chyba kladná nebo záporná. 
	- Integrační složka pomáhá eliminovat zbytkovou chybu v ustáleném stavu.
	$$ u(t) = K_{1} \int_{0}^{t} e(\tau) \, \mathrm{d}\tau $$
	- $K_1$ = integrační zisk (zesílení)
	- $\int_{0}^{t} e(\tau) \, \mathrm{d}\tau$ = integrál chyby v čase
2. Přenosová funkce Integračního regulátoru
	- Přenosová funkce = poměr výstupu systému ke vstupu systému (obojí v Laplacově transformaci)
	$$G(s) = \frac{K_{1}}{s}$$

	- $s$ = komplexní frekvence (proměnná přenosové funkce)