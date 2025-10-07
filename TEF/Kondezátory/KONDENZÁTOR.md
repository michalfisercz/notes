![[kondezatory]]
electrolitický

![[KONDENZATOR_SCHEM]]
$$
\begin{align}
Q = \epsilon_{0}\epsilon_{r}\frac{S}{d}
\end{align}
$$

Kondenzátor je součástka jejíž vlastností je kapacita na principu elektrostatického pole

# využití
- fotografický blesk
- defiblilátor
- vyhlazení napěťových špiček
- oscilátor - generátor střídavého průběhu

# DC zapojení
![[Drawing 2024-11-06 11.18.46.excalidraw]]

# AC zapojení
![[Drawing 2024-11-06 11.24.39.excalidraw]]
- probíhá fázový posun 90˚
- kapacitní reaktance = zdánlivý odpor při průchodu AC

# volt-culombová charakteristika
![[Drawing 2024-11-06 11.33.22.excalidraw]]
C2>C1

# REÁLNÝ KONDENZÁTOR
- ideálně
	- kapacita
- reálně pro přesné výpočty
	- náhradní schéma
		![[Drawing 2024-11-07 08.05.35.excalidraw]]$$
		ESR=R_{iz}+R_{d}+R_{p}
		$$
		

# Dělení kondenzátorů
- pevné
	- svitkové![[Drawing 2024-11-07 08.13.43.excalidraw]]
	- keramické
	- elektrolitické
		- má polaritu
- proměnné
	- ladící
		- použití: kapesní rádio
	- dolaďovací (trimry)

# značení kondenzátorů
- základní jednotka 
	- pF
- 4J7 = 4,7 pF
- jiná varianta
	- 121 -> hodnota
	   K1 -> tolerance
- SMD
	- barvičky

### super-kapacitory
- až tisíce F

# výpočet
- sériově
$$
\frac{1}{c} = \sum \frac{1}{c_{i}}
$$
- paralelní
$$
C=\sum C_{i}
$$
