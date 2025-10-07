- Cévka je součástka schopná udržet v sobě v určitém okamžiku nahromaděnou elektrickou energii a v jiném okamžiku ji do elektrického obvodu vydat. Na principu magnetického pole.
![[Images/cívky]]

# využitý
- zvonek
- reproduktor
- elektromagnetické relé
- CRT
- tlumivka v zářivkách
- [[Transformátor]]
- oscilační obvod
- motor

# Vlastnosti
- indukčnost - L \[ 1 Henry ]
	- je závislá
		- rozměrech cívky
		- počtu závitů
		- vlastnosti jádra

# Ampér-Webrová charakteristika
normální
![[civka_char]]

s jádrem (hysterezní smyčka)
![[sivka_char_jadro]]

# zapojení
- DC
	- odpor$$
		R= \rho \frac{l}{s}
		
		$$
	$$
	R= \frac{T}{56} \cos{56}
 $$
	- projevu se jen svým odporem
	- kolem cívky se vytvoří stále magnetické pole
	- magnetický indukční tok závisí přímo úměrně na indukčnosti cívky (L) a velikosti proudu
	- magnetický lze zesílit vložením jádra
	- vlastní indukčnost
		- vyvolá v cívce proud v opačném směru
		![[civka_graf]]
- AC![[civka_graf_AC]]
	- proud je o 90° za napětím

# přesné výpočty
![[Drawing 2024-11-20 11.08.44.excalidraw]]
$$
Z=\frac{R+j\omega(L(1-\omega^2LC)-CR^2)}{(1-\omega ^2LC)^2+(\omega CR)^2}
$$
# reálná cívka
- indukčnost
- počet závitů
- max. proud
- max. napětí
- max. výkon
- činitel jakosti $Q_{L}$ 
- ztrátový činitel $tg(\delta_{L} )$
