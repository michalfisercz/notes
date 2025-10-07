1) Pravdivostní tabulka
	 v levé části tabulky jsou v jednotlivých řádcích postupně všechny možné stavy na vstupu a v pravé části na příslušných řádcích na výstupu
	C : nejméně významná vstupní proměnná

| číslo řádku |   A   |  B   |  C   |  \|  |  Y   |
| :---------: | :---: | :--: | :--: | :--: | :--: |
|    <hr>     | <hr>  | <hr> | <hr> | <hr> | <hr> |
|      0      |   0   |  0   |  0   |  \|  |  0   |
|      1      |   0   |  0   |  1   |  \|  |  0   |
|      2      |   0   |  1   |  0   |  \|  |  0   |
|    3<br>    |   0   |  1   |  1   |  \|  |  1   |
|      4      |   1   |  0   |  0   |  \|  |  1   |
|      5      | 1<br> |  0   |  1   |  \|  |  0   |
|      6      |   1   |  1   |  0   |  \|  |  0   |
|      7      |   1   |  1   |  1   |  \|  |  1   |

| číslo řádku |   A   |  B  |  C  | \|  |  Y  |
| :---------: | :---: | :-: | :-: | :-: | :-: |
|      0      |   0   |  0  |  0  | \|  |  0  |
|      1      |   0   |  0  |  1  | \|  |  1  |
|      2      |   0   |  1  |  0  | \|  |  1  |
|    3<br>    |   0   |  1  |  1  | \|  |  0  |
|      4      |   1   |  0  |  0  | \|  |  1  |
|      5      | 1<br> |  0  |  1  | \|  |  0  |
|      6      |   1   |  1  |  0  | \|  |  0  |
|      7      |   1   |  1  |  1  | \|  |  1  |
2) úplný disjunktní tvar
	Funkce je zapsána ve formě **součtu součinů (minternů)**
	Jen řádky kde Y = 1 a negujeme 1 na 0
	
| číslo řádku |   A   |   B   |   C   |   \|   | Y$_{1}$ | Y$_2$ | Y$_3$ |
| :---------: | :---: | :---: | :---: | :----: | :-----: | :---: | :---: |
|      0      |   0   |   0   |   0   |   \|   |    0    |   1   |   1   |
|      1      |   0   |   0   |   1   |   \|   |    0    |   1   |   1   |
|      2      |   0   |   1   |   0   |   \|   |    0    |   0   |   0   |
|  **3<br>**  | **0** | **1** | **1** | **\|** |  **1**  |   0   |   1   |
|    **4**    | **1** | **0** | **0** | **\|** |  **1**  |   0   |   0   |
|      5      | 1<br> |   0   |   1   |   \|   |    0    |   0   |   0   |
|      6      |   1   |   1   |   0   |   \|   |    0    |   1   |   0   |
|    **7**    | **1** | **1** | **1** | **\|** |  **1**  |   0   |   1   |
 $$
 \begin{align}
Y_{1}=& \overline{A} \cdot B \cdot C + A \cdot \overline{B} \cdot \overline{C} + A \cdot B \cdot C \\
Y_{2}=&\overline{A}\cdot\overline{B}\cdot\overline{C}+\overline{A}\cdot\overline{B}\cdot C+A\cdot B\cdot\overline{C}\\
Y_{3}=&\overline{A}\cdot\overline{B}\cdot\overline{C}+\overline{A}\cdot\overline{B}\cdot C+ \overline{A}\cdot B\cdot C+A\cdot B\cdot C
\end{align}
 $$

3) úplný konjuktní tvar
	Zápis ve formě: **součin součtů** (maxtermů)
	řádky kde Y = 0

| číslo řádku |   A   |  B  |  C  | \|  | Y$_{1}$ | Y$_2$ | Y$_3$ |
| :---------: | :---: | :-: | :-: | :-: | :-----: | :---: | :---: |
|      0      |   0   |  0  |  0  | \|  |    0    |   1   |   1   |
|      1      |   0   |  0  |  1  | \|  |    0    |   1   |   1   |
|      2      |   0   |  1  |  0  | \|  |    0    |   0   |   0   |
|    3<br>    |   0   |  1  |  1  | \|  |    1    |   0   |   1   |
|      4      |   1   |  0  |  0  | \|  |    1    |   0   |   0   |
|      5      | 1<br> |  0  |  1  | \|  |    0    |   0   |   0   |
|      6      |   1   |  1  |  0  | \|  |    0    |   1   |   0   |
|      7      |   1   |  1  |  1  | \|  |    1    |   0   |   1   |
$$
 \begin{align}
Y_{1}=& (A+B+C)\cdot(A+B+\overline{C})\cdot(A+\overline{B}+C)\cdot(\overline{A}+B+\overline{C})\cdot(\overline{A}+\overline{B}+C)\\
Y_{2}=& (A+\overline{B}+C)\cdot(A+\overline{B}+\overline{C})\cdot(\overline{A}+B+C)\cdot(\overline{A}+B+\overline{C})\cdot(\overline{A}+\overline{B}+\overline{C})\\
Y_{3}=& (A+\overline{B}+C)\cdot(\overline{A}+B+C)\cdot(\overline{A}+B+\overline{C})\cdot(\overline{A}+\overline{B}+C)
\end{align}
 $$
4) Grayův kód (zajímavost)
	kód, v němž se sousední datová slova liší jen v 1 bitu
	**konstrukce**
	- 1 bit
		- 0, 1
	- 2 bit
		- 00, 01, 11, 10
	- 3 bit 
		- 000, 001, 011, 010, 110, 111, 101, 100 

5) Karnaghova mapa
	- pro 2 vstupní proměnou

| ř.  | $x_{1}$ | $x_{0}$ | Y   |
| --- | ------- | ------- | --- |
| 0   | 0       | 0       | 0   |
| 1   | 0       | 1       | 1   |
| 2   | 1       | 0       | 1   |
| 3   | 1       | 1       | 0   |

| 00  | 01  |
| --- | --- |
| 10  | 11  |

| 0   | 1   |
| --- | --- |
| 1   | 0   |

---

|  ř.   | $x_2$ | $x_1$ | $x_0$ |  \|  |  Y   |
| :---: | :---: | :---: | :---: | :--: | :--: |
| <hr>  | <hr>  | <hr>  | <hr>  | <hr> | <hr> |
|   0   |   0   |   0   |   0   |  \|  |  0   |
|   1   |   0   |   0   |   1   |  \|  |  1   |
|   2   |   0   |   1   |   0   |  \|  |  1   |
| 3<br> |   0   |   1   |   1   |  \|  |  0   |
|   4   |   1   |   0   |   0   |  \|  |  1   |
|   5   |   1   |   0   |   1   |  \|  |  0   |
|   6   |   1   |   1   |   0   |  \|  |  0   |
|   7   |   1   |   1   |   1   |  \|  |  1   |

| 0   | 1   | 5   | 4   |
| --- | --- | --- | --- |
| 2   | 3   | 7   | 6   |

|       |     |     |       | $x_2$ | $x_2$ |
| ----- | --- | --- | ----- | ----- | ----- |
|       |     |     | $x_0$ | $x_0$ |       |
|       |     |     |       |       |       |
|       |     | 000 | 001   | 101   | 100   |
| $x_1$ |     | 010 | 011   | 111   | 110   |

| 0   | 1   | 0   | 1   |
| --- | --- | --- | --- |
| 1   | 0   | 1   | 0   |

---

|  ř.   | $x_2$ | $x_1$ | $x_0$ |  \|  |  Y   |
| :---: | :---: | :---: | :---: | :--: | :--: |
| <hr>  | <hr>  | <hr>  | <hr>  | <hr> | <hr> |
|   0   |   0   |   0   |   0   |  \|  |  1   |
|   1   |   0   |   0   |   1   |  \|  |  0   |
|   2   |   0   |   1   |   0   |  \|  |  1   |
| 3<br> |   0   |   1   |   1   |  \|  |  0   |
|   4   |   1   |   0   |   0   |  \|  |  1   |
|   5   |   1   |   0   |   1   |  \|  |  0   |
|   6   |   1   |   1   |   0   |  \|  |  1   |
|   7   |   1   |   1   |   1   |  \|  |  0   |

| 1   | 0   | 0   | 1   |
| --- | --- | --- | --- |
| 1   | 0   | 0   | 1   |

---

| 0   | 1   | 5   | 4   |
| --- | --- | --- | --- |
| 2   | 3   | 7   | 6   |
| 10  | 11  | 15  | 14  |
| 8   | 9   | 13  | 12  |

|     |     |     |      |      | x2   | x2   |
| --- | --- | --- | ---- | ---- | ---- | ---- |
|     |     |     |      | x0   | x0   |      |
|     |     |     |      |      |      |      |
|     |     |     | 0000 | 0001 | 0101 | 0100 |
|     | x1  |     | 0010 | 0011 | 0111 | 0110 |
| x3  | x1  |     | 1010 | 1011 | 1111 | 1110 |
| x3  |     |     | 1000 | 1001 | 1101 | 1100 |

---
**MINIMALIZACE POMOCÍ KARNAUGHOVY MAPY- PRAVIDLA**
1) Sousední políčka se stejnými hodnotami zahrnujeme do SMYČEK.
2) Smyčky mohou mít velikost mocnin čísla 2 tj. 2$^n$ (počet jedniček ve smyčce může být: 1, 2, 4, 8 atd., NE LICHÝ počet 3, 5 atd.).
3) Smyčky se snažíme dělat co největší a mohou se překrývat.
4) Sousední políčka jsou políčka, která se liší v jediné proměnné. Krajní políčka mapy považujeme za sousední.
5) Disjunktní tvar: píšeme pro logické jedničky jako součet součinů. Pod čarou jsou hodnoty např. A, B, x1, x2 apod., mimo čáru jsou proměnné $\overline A$, $\overline B$, $\overline x_{1}$, $\overline x_{2}$ atd.
6) Konjunktní tvar: píšeme pro logické nuly jako součin součtů. Pod čarou jsou proměnné např. $\overline A$, $\overline B$, $\overline x_{1}$, $\overline x_{2}$ apod., mimo čáru jsou proměnné A, B, x1, x2 atd.
![[Pasted image 20250604112012.png]]
$$
\begin{gathered}
f(A,B,C,D) &&=&& B\cdot\overline{C} \cdot \overline{D}  && + && A\cdot \overline{B} && + && C \cdot A  \\
&&&& \mathrm{žlutá} &&&& \mathrm{fialová} &&&& \mathrm{modrá}
\end{gathered}
$$

---

1110
0111
0111
1110

$$
\begin{align}
Y_{D}&=A\cdot\overline{C}\cdot \overline{B} + C\cdot B \\
Y_{D}&=\overline{C}
\end{align}
$$
