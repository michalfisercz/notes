

**Git** = distribuovaný verzovací systém  

## Distribuovaný
Repositář je na více místech najednou (web, počítač).  
- Lze ho **naklonovat** na lokální zařízení – každá kopie má všechny informace (je kompletní).  
- Různé kopie se mohou v čase vyvíjet různě.  

## Verzovací
Ukládá jednotlivé verze souboru.  
- Neukládá celou novou verzi, ale jen změnu → úspornější.  
- Každý checkpoint uložení souboru = **commit**.  
- Commity jsou textové soubory obsahující řádky (+/−, přidán nebo smazán), které byly změněny.  

---

## Vytvoření nového repositáře
- `git init` – nutno inicializovat velké množství parametrů ručně.  
- `git clone` – optimální založit repositář na GitHubu kvůli automatické inicializaci, následně naklonovat na lokální počítač.  

---

## Umístění repositáře v počítači
Repositář obsahuje skrytou složku **`.git`**, která drží všechny informace o projektu (např. jednotlivé změny řádků).  

---

## Základní příkazy Git

### 1. `git clone` / `git init`
- Vytvoření nového nebo zkopírovaného repositáře.  

### 2. `git fetch`
- Git se zeptá serveru, zda je lokální kopie aktuální.  
- Porovná seznam commitů, jejich délku, poslední společný commit.  
- Stahuje aktuální informace o rozdílech mezi lokální a vzdálenou verzí.  

### 3. `git status`
- Vypíše informace o stavu pracovního adresáře.  
- Nutné nejdříve stáhnout aktuální data pomocí `git fetch`.  

### 4. `git pull`
- Nejdříve spustí `git fetch`.  
- Poté stáhne změny z online serveru a aktualizuje lokální repositář.  
- Pokud se lokální a online verze liší:  
  - Git provede **merge** (riziko konfliktů).  
  - Pokud se změny nekříží, spojí je automaticky.  
  - Pokud se změny kříží → nutný manuální zásah.  

### 5. `git add <soubor>`
- Přidává soubor na seznam souborů, které budou zahrnuty do commitu.  
- Poskytuje **dvoufázový systém ukládání** nové verze.  
- Nevyžaduje online server (funguje lokálně).  

### 6. `git commit`
- Aktualizuje lokální repositář (konkrétně soubory přidané pomocí `git add`).  
- Doporučuje se dělat menší commity (snadnější návrat zpět).  

### 7. `git push`
- Nejprve spustí `git fetch`.  
- Pokud nejsou na serveru novější změny → nahraje lokální commity na vzdálený server.  
- Pokud jsou na serveru změny → je nutné nejprve spustit `git pull`.  

## Větvení (branches)

- Git umožňuje pracovat na více **větvích** současně – každá větev je plnohodnotná.  
- Příkazy Gitu se vztahují vždy na **aktuální větev**, ve které pracuješ.  
- Větve umožňují vést paralelní verze projektu (např. `release` branch, `developer` branch).  

### Základní příkazy pro větvení
- `git branch` – zobrazí seznam větví (hvězdička = aktuální větev).  
- `git branch <název>` – vytvoří novou větev.  
- `git checkout <název>` – přepne se do zadané větve.  
- `git checkout -b <název>` – vytvoří **a zároveň přepne** na novou větev.  
- `git merge <název>` – sloučí zadanou větev do aktuální větve.  
- `git branch -d <název>` – smaže větev (pokud už byla sloučena).  

