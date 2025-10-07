# Java – základní poznámky

## Hlavní principy vývoje Javy
1. Jednoduchý, objektově orientovaný  
2. Robustní, bezpečný  
3. Nezávislý na architektuře – přenosný  
4. Výkonný  
5. Interpretovaný, vícevláknový  

---

## Zpracování programu v Javě
- **Editování**  
  - libovolný textový editor  
  - vývojová prostředí, soubor `.java`  

- **Kompilace**  
  - překlad do pseudojazyka *byte-code*  
  - vznikne soubor `.class`  
  - pro překlad lze použít překladač `javac`  

- **Zavedení do paměti (load)**  

- **Ověřování (verifikace)**  
  - zajišťuje bezpečnost spuštěného programu  

- **Provádění (interpretace)**  
  - pomocí virtuálního stroje (JVM)  

---

## Rozdělení programů v Javě
1. **Aplikace**  
2. **Aplety**  
   - liší se ve fázi zavedení (jsou zaváděny pomocí webových prohlížečů)  
   - platí pro ně přísnější pravidla bezpečnosti  
   - dnes nahrazeny JavaScriptem  

---

## Základní pojmy
- **JDK (Java Development Kit)**  
  - soubor základních nástrojů pro vývoj aplikací pro platformu Java  

- **Součásti JDK**  
  - debugger pro ladění programů  
  - překladač do bajtkódu  
  - virtuální stroj (**JRE = Java Runtime Environment**)  
    - zajišťuje vazby na hardware  
    - interpretuje bajtkód = čte instrukce a hned je provádí  

- **Java Core API**  
  - aplikační programové rozhraní  
  - soubor knihovních tříd, které se musí vyskytovat v každém prostředí, kde se Java používá  
  - pokud Java používá kód z API, ten není součástí programu – knihovní třídy se pouze načítají  

---

## Vývojová prostředí Javy
- **NetBeans**  
  - český open-source program  
  - primárně určený pro vývoj aplikací v Javě  
  - podporuje i další programovací jazyky  

- **Eclipse**  
  - určený pro jazyk Java  
  - pomocí pluginů lze rozšířit i na další programovací jazyky  

- **BlueJ**  
  - vývojové prostředí vyvinuté speciálně pro výuku OOP  
  - umožňuje vytvářet UML diagramy tříd  
  - interaktivní
