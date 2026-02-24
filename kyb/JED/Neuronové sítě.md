
Motivace (mozek vs. počítač)
- Lidský mozek pracuje jiným způsobem než běžné číslicové počítače
- Počítače přesně a rychle provádějí posloupnosti instrukcí, které pro ně byly formulovány
- člověk dokáže lépe řešit řadu výpočetně náročných úkolů (porozumění řeči, zpracování vizuální informace)

=> snaha napodobit "schopnosti mozku" uměle
<img src=Images/computer_vs_brain.png>

## Lidský mozek
- skládá se ze 100 miliard neuronů
### Neuron
- Biologický neuron je základní buňkou biologických neuronových sítí
- Neuron má více vstupů, a pokud dostatečné množství z nich je aktivních, zapne se výstup
- Výstup = axom; Je pouze jeden, může mít délku až 60 cm
- Synapse = jednosměrná brána, která zaručuje jednosměrný provoz neuronu (vstup -> výstup)
- Přenášené signály jsou elektrické impulsy, jejich přenos je ovlivněn uvolňováním budících a tlumících látek v synapsích (excitátory, inhibitory)
- Po vygenerování impulsu nastává období pauzy, kdy neuron nemůže reagovat na podněty. (tzn. že neuron se chová diskrétně, a jeho funkce NENÍ spojitá)
- Období pauzy jednotlivých neuronů se liší, práce neuronů v mozku je asynchronní

## Vytvoření modelu neuronu
<img src=Images/neuron_model.jpg>

1) McCullochův - Pittsův model (nejjednodušší binární model)
	- vstupy $x_i$ nabývají hodnot pouze 0 a 1
	- váhy $w_i$ nabývají +1 nebo -1 = budící nebo tlumící signály
	-  vstupy a váhy určují práh 
2) Perceptron
	- Vstupy a váhy nabývají hodnot reálných čísel
	- excitace - inhibice neporovnáváme s práhem, ale práh odečteme a hodnotu porovnáváme s nulou
	- Nezkoumáme pouze zaplý/vyplý, ale na hodnotě počítáme obecnou aktivační funkci f(x)
	- nejčastěji sigmoida $\frac{2}{(1 + e^{-\lambda x})} - 1$  
	- Bipolární model rozděluje vstupní prostor $\vec{x}$ na dvě části (možnost lineárního rozdělení)


### Typy umělých neuronových sítí

- Neuronová síť vzniká spojením jednotlivých neuronů
- Způsob zapojení neuronové sítě = topologie sítě

<img src=Images/kyb2001.png>
- Každá vrstva neuronů má svůj vektor vah, tedy pro $k$ vrstev synchronních neuronů se stejnou aktivační funkcí se zavádí matice vah (více sloupců, více vektorů vah)
- Každá vrstva neuronů má svou aktivační funkci
- Počet parametrů razantně roste (důsledkem jsou sítě s miliardami a biliony parametrů)
- Síť lze matematicky zapsat maticovým násobením (matice vah, vektor vstupů, jednotlivé vrstvy neuronů)

 - Rekurentní neuronové sítě (výstupy se používají jako vstupy, existují rovnovážné ustálené polohy)

# Fáze činnosti neuronových sítí

1) Fáze nastavování
	1) Cílem je nastavit váhy a prahy jednotlivých neuronů sítě s danou topologií, aby síť prováděla požadovanou činnost. (daná topologie = dané: n vstupů/výstupů, zapojení, aktivační funkce)
	2) Pro specifický úkol je nutno navrhnout síť s vhodnou topologií (počet neuronů, vrstev, etc.) (je to alchymie, topologii pro daný úkol nelze spolehlivě navrhnout = pokus/omyl)
	3) Větší síť se nutně nerovná lepší síť
		
2) Fáze pracovní
	1) Ve fázi pracovní síť reaguje na přeložené vstupy podle svého předchozího nastavení
	2) Výpočetně ne moc náročné
	3) Fáze probíhající při zadání prompt LLM (chatGPT, etc.)

### Možnosti nastavování neuronové sítě

1) Výpočtem
	1) Pouze u velmi triviálních sítí, lze provést výpočet vah pro získání požadovaného vstupu
2) Učením 
	1) Supervised learning
		1) Existuje trénovací množina dvojic (vstup, požadovaný výstup)
		2) Zadáme vstup, a hledáme váhy aby výstupem byl požadovaný výstup
		3) Jde o proces podobný fitování sítě na známá data (=učení)
	2) Unsupervised learning
		1) Existují pouze data
		2) Proces shlukování (metoda K-means)
		3) Rozdělení dat na jednotlivé skupiny



# Využití neuronových sítí

- Při řešení problémů, kde není znám jednoznačný algoritmus řešení, ale kde existuje dost velká množina příkladů, jejichž řešení známe.
	- rozpoznávání složitých signálů a obrazců
	- modelování funkčních závislostí
	- optimalizační úlohy
	- rekonstruktory zašuměných dat
- neuronové sítě nejsou vhodné pro přesné výpočty
