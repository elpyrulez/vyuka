Jasně, tady je kompletní kód přepsaný do Markdown formátu včetně podrobného vysvětlení:

## Ukázkový kód pro sledování užívání léků

```python
# Sledování užívání léků v Pythonu

# Funkce pro zobrazení všech užitých léků
def zobrazLeky(lekData):
    print("\nSeznam všech užitých léků:")
    for lek in lekData:
        nazev, pocet_pilulek, mg, vyrobce, link = lek
        print(f"{nazev} - Počet pilulek: {pocet_pilulek}, Množství na pilulku: {mg} mg, "
              f"Výrobce: {vyrobce}, Odkaz: {link}")

# Funkce pro kontrolu předávkování
def kontrolujPredavkovani(pocet_pilulek):
    if pocet_pilulek > 10:
        print("Upozornění: Možné předávkování! Vzali jste více než 10 pilulek najednou.")

# Funkce pro výpočet průměrného množství pilulek za den
def prumerPilulek(celkovyPocetPilulek, dny):
    return celkovyPocetPilulek / dny if dny > 0 else 0

# Hlavní funkce aplikace
def hlavniProgram():
    lekData = []  # Seznam pro uchovávání dat o lécích
    celkovyPocetPilulek = 0
    dny = 0
    
    while True:
        # Uživatelský vstup pro zadání léku
        nazev = input("\nZadejte název léku (nebo 'konec' pro ukončení): ")
        if nazev.lower() == 'konec':
            break
        
        try:
            pocet_pilulek = int(input("Zadejte počet pilulek: "))
            mg = float(input("Zadejte množství mg na jednu pilulku: "))
            vyrobce = input("Zadejte výrobce léku: ")
            link = input("Zadejte odkaz na lék (např. Dr.Max): ")
        except ValueError:
            print("Chyba: Zadejte správné hodnoty pro počet pilulek a množství mg.")
            continue

        # Uložení zadaných údajů do seznamu
        lekData.append((nazev, pocet_pilulek, mg, vyrobce, link))
        
        # Kontrola předávkování
        kontrolujPredavkovani(pocet_pilulek)

        # Sčítání celkového počtu pilulek
        celkovyPocetPilulek += pocet_pilulek

        # Předpokládáme, že každý záznam je pro nový den užívání
        dny += 1

    # Zobrazení všech léků
    zobrazLeky(lekData)

    # Výstup celkového počtu pilulek a průměru na den
    print(f"\nCelkový počet užitých pilulek: {celkovyPocetPilulek}")
    print(f"Průměrný počet pilulek za den: {prumerPilulek(celkovyPocetPilulek, dny):.2f}")

# Spuštění hlavního programu
if __name__ == "__main__":
    hlavniProgram()
```

## Vysvětlení:

1. **Funkce `zobrazLeky(lekData)`**:
   - Tato funkce vypisuje seznam všech léků, které uživatel zadal. Pro každý lék v seznamu `lekData`, který je uložen jako n-tice obsahující název léku, počet pilulek, množství mg na pilulku, výrobce a odkaz, se vypíše příslušná informace o každém léku.

2. **Funkce `kontrolujPredavkovani(pocet_pilulek)`**:
   - Kontroluje, zda počet pilulek, který uživatel zadal, je větší než 10. Pokud ano, funkce vypíše upozornění, že by mohlo jít o předávkování.

3. **Funkce `prumerPilulek(celkovyPocetPilulek, dny)`**:
   - Tato funkce spočítá průměrný počet pilulek, které uživatel užil za den. Pokud je zadáno alespoň jedno užívání (tedy `dny > 0`), funkce vrátí průměrný počet pilulek. Pokud jsou dny 0 (což by znamenalo, že žádné léky nebyly zadány), funkce vrátí 0.

4. **Hlavní funkce `hlavniProgram()`**:
   - Uživatel je opakovaně vyzýván k zadání informací o lécích. Tyto informace (název léku, počet pilulek, mg, výrobce a odkaz na lék) jsou uloženy do seznamu `lekData`.
   - Funkce také provádí kontrolu na předávkování a sčítá celkový počet užitých pilulek.
   - Na konci se vypíše seznam všech léků a průměrný počet pilulek za den.

5. **Podmínka `if __name__ == "__main__"`**:
   - Tento blok kódu se zajistí, že hlavní funkce `hlavniProgram()` bude spuštěna pouze tehdy, když je tento skript spuštěn přímo, nikoli když je importován jako modul v jiném programu.

---

Tento kód umožňuje sledování užívání léků, kontrolu předávkování, výpočet průměru užívaných pilulek a zobrazení výsledků v přehledném formátu.