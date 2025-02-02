## Úkol: Sledování užívání léků

### Co máš udělat?

Napiš program v Pythonu, který bude sledovat, jaké léky si člověk vzal, kolik pilulek, a kolik mg má každý lék. Program taky zkontroluje, jestli je všechno v pořádku a neberou se léky příliš často. Hlavní cíl je mít funkční konzolovou aplikaci, ale pro bonusy se můžeš zaměřit na převod do GUI (s použitím PyQt5 – více info [tady](https://cs.wikipedia.org/wiki/PyQt5)) a práci s čísly.

## Co budeš potřebovat?

1. **Uživatelský vstup:**
   - Uživatel zadá název léku, počet pilulek a množství mg na jednu pilulku. Může také zadat další informace, jako je výrobce léku a odkaz na lék (např. Dr.Max).
   - Tato data budou uložena v seznamu, kde každá položka bude obsahovat název léku, počet pilulek, množství mg, výrobce a link.

2. **Výpis informací:**
   - Na konci ti program vypíše seznam všech léků, které byly užity, včetně počtu pilulek, množství mg, výrobce a odkazu na lék.

3. **Kontrola předávkování:**
   - Pokud uživatel zadá, že vzal víc než 10 pilulek najednou, program ho upozorní, že by to mohl být problém.

4. **Maximální denní dávka:**
   - Každý lék bude mít určenou maximální dávku, tedy kolik pilulek je bezpečné vzít za den.

5. **Výstup na konci:**
   - Na závěr program vypíše:
     - Kolik různých léků a pilulek bylo užito.
     - Jestli někdo překročil doporučenou denní dávku.
     - Kolik mg každého léku bylo užito.
     - Doplňující informace jako výrobce a odkaz na lék. např. [tady](https://www.pribalovy-letak.cz/584-rivotril-2-mg-tablety)

## Bonusy

- **Hezký výstup:**
   - Přidej funkci, která všechny léky a pilulky vypíše pěkně naformátované do tabulky nebo s odrážkami.
   - Můžeš použít knihovnu `prettytable` nebo si s tím pohrát a udělat to hezké i bez toho.

- **Průměr pilulek za den:**
   - Vytvoř proměnnou, která bude sledovat celkový počet pilulek, a nakonec spočítej průměr na den.
   - K tomu budeš potřebovat i počet dní, kdy uživatel nějaké léky užil.

- **Převod na camelCase:**
   - Uprav všechny názvy funkcí a proměnných na camelCase. Pokud nevíš co to je, je to styl, kdy každé nové slovo začíná velkým písmenem a není mezi nimi mezera (např. `sledovaniLeku`). (Tohle udělej přes GPT, aspoň uvidíš jak je to OP, nebo můžeš napsat skript co to převede ten soubor na ten způsob zápisu kódu)

- **Převod do GUI:**
   - Pokud máš chuť a čas, můžeš celý program přepsat do grafického rozhraní pomocí PyQt5, takže místo zadávání v konzoli budeš mít okna pro zadávání léků a zobrazení výsledků. (Vlastně to stejný)

## Doporučené Python Extensions

Pokud bys chtěl svůj vývoj ještě zjednodušit nebo obohatit, doporučuji následující Python extensions pro VSCode nebo jiný IDE:

1. **Pylance** - Intellisense a zrychlené lintování pro Python. Skvělý nástroj pro zajištění kvalitního kódu.
2. **Python** (oficiální rozšíření pro VSCode) - Pomáhá s běžnými funkcemi, jako je spouštění skriptů, debugging a zjednodušuje práci s virtuálními prostředími.
3. **Jupyter** - Pokud budeš chtít testovat kód interaktivně, tato extension umožňuje běh Python kódu v Jupyter noteboocích přímo v IDE.
4. **autopep8** nebo **black** - Automatické formátování kódu podle PEP 8.
5. **Python Docstring Generator** - Pomáhá automaticky generovat docstringy pro funkce, což usnadňuje dokumentování kódu.
6. **GitLens** - Pokud budeš používat Git, tato extension poskytuje rozsáhlé možnosti sledování změn v kódu a vylepšení práce s repozitáři.