# Python - Základy programování

---

## 1. Proměnné a vstupy

Proměnné jsou místa, kam si Python ukládá hodnoty. Několik základních typů:

```python
x = 10  # Celé číslo (int)
y = 3.14  # Desetinné číslo (float)
text = "Ahoj"  # Řetězec (str)
pravda = True  # Boolean (bool)
```

Pro přečtení vstupu od uživatele použijeme funkci `input()`:

```python
jmeno = input("Jak se jmenujes? ")
print("Ahoj, " + jmeno + "!")
```

---

## 2. Datové typy v Pythonu

Python podporuje různé typy dat. Základní jsou:

### Celá čísla (int)

Celá čísla mohou být kladná i záporná.

```python
x = 10
print(type(x))  # <class 'int'>
```

### Desetinná čísla (float)

Čísla s desetinnou tečkou se zapisují s tečkou.

```python
y = 3.14
print(type(y))  # <class 'float'>
```

### Řetězce (str)

Řetězce se zapisují do uvozovek. Preferuj dvojité uvozovky `""`.

```python
text = "Ahoj"
print(type(text))  # <class 'str'>
```

### Boolean (bool)

Reprezentuje pravdivostní hodnoty `True` nebo `False`.

```python
pravda = True
print(type(pravda))  # <class 'bool'>
```

### Seznamy (list)

Seznamy mohou obsahovat více hodnot různých typů.

```python
ovoce = ["🍎", "🍌", "🍉"]
print(type(ovoce))  # <class 'list'>
```

### Slovníky (dict)

Klíč-hodnota páry pro strukturovaná data.

```python
osoba = {"jmeno": "Standa", "vek": 21}
print(type(osoba))  # <class 'dict'>
```

### Množiny (set)

Neumožňují duplikáty.

```python
cisla = {1, 2, 3, 3, 4}
print(cisla)  # {1, 2, 3, 4}
```

### N-tice (tuple)

Neměnné pole hodnot.

```python
barvy = ("červená", "zelená", "modrá")
print(type(barvy))  # <class 'tuple'>
```

---

## 3. Podmínky a cykly

**Podmínky:**

```python
age = 18
if age >= 18:
    print("Můžeš si dát pivo 🍺")
else:
    print("Sorry, ještě nejsi plnoletý 😢")
```

**Cykly:**

```python
for i in range(5):  # Projede čísla 0-4
    print("Číslo:", i)

while age < 21:  # Dokud je věk menší než 21
    print("Je ti jen", age, "let")
    age += 1
```

---

## 4. Třídy (OOP v Pythonu)

Třídy jsou základní stavební blok objektově orientovaného programování (OOP). Umožňují vytvářet objekty s vlastnostmi (atributy) a funkcemi (metodami).

```python
class Auto:
    def __init__(self, znacka, rychlost):
        """
        Konstruktor třídy, inicializuje objekt.
        Parametry:
        - znacka (str): Značka auta (např. "BMW").
        - rychlost (int): Maximální rychlost auta v km/h.
        """
        self.znacka = znacka
        self.rychlost = rychlost
    
    def info(self):
        """Vrátí informace o autě jako řetězec."""
        return f"{self.znacka} jede {self.rychlost} km/h."

# Vytvoření objektu třídy Auto
auto1 = Auto("BMW", 200)
print(auto1.info())  # BMW jede 200 km/h.
```

Tahle třída se dá pak importovat do jiných souborů a můžeš používat její objekt Auto a třeba to propojit s funkcí v jiném souboru (modulu/knihovně) co ovládá pomocí náhodného generátoru čícsel randomizer rychlosti auta, nebo cokoliv, fantazii se meze nekladou

třeba otevřu **main.py** a zadám tenhle příkaz na začátku scriptu, tím naimportuji třídu **Auto**, a můžu na ní aplikovat i funkce definované v jiném souboru

``` python
from cesta_k_souboru import Auto # Z souboru importujem třídu auto a můžem jí používat

def coJeToZaAuto(auto: Auto): # Tady je dobry mu rict ze ocekava argument typu Auto, coz je ta nase trida, a jen vrati zpatky pres metodu ve tride info o aute
	return auto.info()

# Vytvoření objektu třídy Auto s parametry "BMW" a 200 km/h
auto1 = Auto("Mercedes", 400)
coJeToZaAuto(auto1)
```
