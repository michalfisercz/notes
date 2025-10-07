# Frekvenční charakteristika

Popisuje, jak prvek (např. filtr, zesilovač, obvod) reaguje na vstupní signál různých **frekvencí**.  
Zajímá nás:

- **Zesílení / útlum** (velikost výstupu vůči vstupu v závislosti na frekvenci)
- **Fázový posun** (o kolik se signál zpozdí nebo předběhne)

Typické zobrazení je **Bodeho diagram** ( **zisk $\pu{ [dB]}$ vs. frekvence**):
![[Pasted image 20250930100848.png]] 

---

# Low Pass Filter (Dolní propust)

Propouští **nízké frekvence**, vysoké **tlumí**.

Typický příklad: **RC člen (rezistor + [[KONDENZÁTOR]])**.
![[Pasted image 20250930100901.png]]


Nízké frekvence → kondenzátor se chová jako **otevřený obvod** → signál projde.  
Vysoké frekvence → kondenzátor se chová jako **zkrat** → signál je odveden do země.

---

# Časová konstanta

$$  
\begin{align}  
\tau_{RC}&=R\cdot C \quad \pu{ [s] } \\  
\tau_{RL}&=\frac{L}{R} \quad \pu{ [s] }  
\end{align}  
$$

Vyjadřuje, **jak rychle systém reaguje**. Po čase **τ** dosáhne výstup cca **63 %** své konečné hodnoty (při skokovém vstupu).

Velká τ → **pomalý** systém  
Malá τ → **rychlá** odezva

---

# Integrační článek

RC low pass může fungovat jako **integrátor**, pokud je **vstupní frekvence dostatečně vysoká** (nad mezní frekvencí filtru).
![[Pasted image 20250930104627.png]]
Výstupní napětí je **úměrné [[integrálu]] vstupního napětí**:

$$
u_out \approx \frac{1}{RC} \int u_in dt
$$

Použití např. v **měřicí technice, [[PWM]] filtraci nebo analogových regulátorech**.
