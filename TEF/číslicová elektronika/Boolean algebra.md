[[číslicová elektronika]]
[[Vyjádření logické funkce]]
Pracuje s logickými hodnotami:  
**0 = nepravda**, **1 = pravda**

---

# 🔁 Komutativnost  
Při sčítání a násobení nezáleží na pořadí:
$$
\begin{gathered}
A \cdot B = B \cdot A\\
A + B = B + A
\end{gathered}
$$

---

# 🧮 Asociativnost  
U tří proměnných je jedno, které se kombinují jako první:
$$
\begin{gathered}
(A \cdot B) \cdot C = A \cdot (B \cdot C)\\
(A + B) + C = A + (B + C)
\end{gathered}
$$

---

# 🧩 Distributivita  
Roznásobení závorky:
$$
\begin{gathered}
A \cdot (B + C) = (A \cdot B) + (A \cdot C)\\
A + (B \cdot C) = (A + B) \cdot (A + C)
\end{gathered}
$$

---

# 🚫 Zákon o vyloučení třetího stavu  
Výrok a jeho negace nemohou být pravdivé zároveň:
$$
\begin{gathered}
A \cdot \overline{A} = 0\\
A + \overline{A} = 1
\end{gathered}
$$

---

# 🔄 Absorpce  
$$
\begin{gathered}
A \cdot A = A\\
A + A = A
\end{gathered}
$$

---

# ⚖️ Zákon o neutrálnosti 0 a 1  
$$
\begin{gathered}
A \cdot 1 = A\\
A + 0 = A
\end{gathered}
$$

---

# 🧨 Zákon o agresivnosti 0 a 1  
$$
\begin{gathered}
A \cdot 0 = 0\\
A + 1 = 1
\end{gathered}
$$

---

# 🔁 Dvojitá negace  
$$
\overline{\overline{A}} = A
$$

---

# 🧼 Absorpce s negací  
$$
\begin{gathered}
A + \overline{A} \cdot B = A + B\\
A \cdot (\overline{A} + B) = A \cdot B
\end{gathered}
$$

---

# 🧱 Absorpce pro složené výroky  
$$
\begin{gathered}
A + A \cdot B = A\\
A \cdot (A + B) = A
\end{gathered}
$$

---

# 📐 De Morganovy zákony  
$$
\begin{gathered}
\overline{A + B} = \overline{A} \cdot \overline{B} \\
\overline{A \cdot B} = \overline{A} + \overline{B} \\
\overline{A \cdot B \cdot C} = \overline{A} + \overline{B} + \overline{C}
\end{gathered}
$$

---

# 🧾 Pravidlo pro negaci logické funkce  
1. Negujeme jednotlivé proměnné  
2. 0 → 1, 1 → 0  
3. Zaměníme operace: ∧ → ∨, ∨ → ∧  
