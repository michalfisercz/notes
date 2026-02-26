
## Pulzně šířková modulace

Principem pulzně šířkové modulace je regulace výkonu, např. intenzity osvětlení, chabým trikem na náš mozek, který vnímá rychlé blikání tak, že ho nevnímá. Tedy když necháme světlo rychle blikat, náš mozek to bude vnímat pouze jako snížení intenzity (nezaregistruje blikání). Zavádíme pojem "Střída", kterou lze definovat jako procento času, po který je osvětlení zapnuto (0 - 100 %).
PS: osvětlení je jen konkrétní příklad, lze aplikovat obecně.

### Fungování

- Mějme čítač, datový registr, a logickou jednotku porovnávající binární výstupy z těchto součástek. Mějme vzestupný čítač (10 bitový), a datový registr. (viz obr. 1)
- 10 bitový čítač znamená, že čítač dělí frekvenci 1024 krát ($2^{10}$), zároveň má omezený rozsah (po 1024 se resetuje)
- V časovém diagramu lze vidět, že po dosažení maximální hodnoty čítače (1024) dojde k jeho resetování
- Nastavením Datového registru na určitou hodnotu (<1024), např. 512, můžeme zapojit pin (A=B) logické jednotky na RST (reset), čímž dojde k resetování čítače, a začne se počítat znovu.
- Hodnota datového registru je volně nastavitelná
- Počítání se periodicky opakuje. 
- Nastavením datového registru na hodnotu menší než 1024 dojde k zvýšení výstupní frekvence.
- Pokud ale nezapojíme A=B na RST, pak na pinu A<\B bude nastavena hodnota 1 v menším procentu celkového času (střída < 100 %), protože A<\B bude 1 dokud A nedosáhne B, pak bude nula, a pak bude nula dokud čítač nenapočítá do maximální hodnoty (1024), pak se puls znovu opakuje. 
- Binární číslo B tedy určuje střídu, a tedy i např. intenzitu osvětlení

<img src=Images/pwm1.jpg>
Obr. 1

Obrázek 2 zobrazuje podobné zapojení s řídícím registrem, děličem frekvence procesoru, pinem který řídí polaritu počítání (vzestupné/sestupné), a EN pin umožňující vypnutí zařízení.

1 milisekundu na výstupu spočítáme tak, že frekvenci procesoru podělíme hodnotou nastavenou na děliči (např. 32), dále n-bitový čítač vydělí frekvenci hodnotou ($2^n$ ), tedy 1000 pro 10-bitový čítač, čímž dostaneme 1 kHz. To znamená, že frekvence pulzu je 1 kHz, a z toho perioda: 1 ms. 
Nastavením hodnoty A na 1024/5, dosáhneme pulzně šířkové modulace 20 %. 
POZOR! v závislosti na polaritě, dosáhneme buď střídy 20 % nebo 80 %, neboť piny A<\B a A>\B jsou inverzní.

<img src=Images/pwm2.jpg>
Obr. 2