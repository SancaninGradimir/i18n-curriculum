---
id: 67f39babe1e2ec1fb6eea32a
title: Rečnici i Skupovi: Pregled
challengeType: 31
dashedName: review-dictionaries-and-sets
---

# --description--
## Rečnici

- **Diktionari**: Diktionari su ugrađene strukture podataka koje skladište kolekcije parova ključ-vrednost. Ključevi moraju biti nemenjivi tipovi podataka. Ovo je opšta sintaksa Python diktionara:

```python
dictionary = {
    key1: value1,
    key2: value2
}
```

- **`dict()` Konstruktor**: Konstruktor ``dict()`` je alternativan način za izgradnju rečnika. Prosleđujete listu tupola kao argument konstruktoru ``dict()``. Ovi tupoli sadrže ključ kao prvi element, a vrednost kao drugi.

```python
pizza = dict([('name', 'Margherita Pizza'), ('price', 8.9), ('calories_per_slice', 250), ('toppings', ['mozzarella', 'basil'])])
```

- **Notacija sa uglastim zagradama**: Da biste pristupili vrednosti para ključ-vrednost, možete koristiti sintaksu poznatu kao notacija sa uglastim zagradama.

```python
dictionary[key]
```

## Uobičajene metode rečnika

- **`get()` Metoda**: Metoda `get()` dohvaća vrednost povezanu sa ključem. Slična je notaciji u uglastim zagradama, ali vam omogućava da postavite podrazumevanu vrednost, sprečavajući greške ako ključ ne postoji.

```python
dictionary.get(key, default)
```

- **`keys()`<0xC2><0xA0>i<0xC2><0xA0>`values()`<0xC2><0xA0>Metode**: Metode ``keys()`` i ``values()`` vraćaju objekat pogleda (view object) sa svim ključevima i vrednostima iz rečnika, respektivno. Objekat pogleda je način za pregled sadržaja rečnika bez kreiranja zasene kopije podataka.

```python
pizza = {
    'name': 'Margherita Pizza',
    'price': 8.9,
    'calories_per_slice': 250
}

pizza.keys()
# dict_keys(['name', 'price', 'calories_per_slice'])

pizza.values()
# dict_values(['Margherita Pizza', 8.9, 250])
```

- **`items()` Metoda**: Metoda ``items()`` vraća objekat prikaza (view object) sa svim parovima ključ-vrednost u rečniku (dictionary), uključujući i ključeve i vrednosti.

```python
pizza.items()
# dict_items([('name', 'Margherita Pizza'), ('price', 8.9), ('calories_per_slice', 250)])
```

- **`clear()` Method**: Metoda ``clear()`` uklanja sve parove ključ-vrednost iz rečnika.

```python
pizza.clear()
```

**Method**: Metoda ``pop()`` uklanja par ključ-vrednost sa ključem navedenim kao prvi argument i vraća njegovu vrednost. Ako ne postoji taj ključ, vraća podrazumevanu vrednost navedenu kao drugi argument. Ako ne postoji ključ i nije navedena podrazumevana vrednost, izbacuje se ``KeyError``.

```python
pizza.pop('price', 10)
pizza.pop('total_price') # KeyError
```

- **`popitem()` Metoda**: U Pythonu verzije 3.7 i novijim, metoda `popitem()` uklanja poslednji uneti element.

```python
pizza.popitem()
```

- **`update()` Метод**: Метод `update()` ažurira parove кључ-значење са паровима кључ-значење из drugog речника. Ако имају заједничке кључеве, њихове вредности се препишу. Нови кључеви ће бити додани у речник као нови парови кључ-значење.

```python
pizza.update({ 'price': 15, 'total_time': 25 })
```

## Petljanje kroz rečnik

- **Iteriranje kroz vrednosti**: Ako treba da iterirate kroz vrednosti u rečniku (dictionary), možete napisati petlju `for` sa `values()` da biste dobili sve vrednosti rečnika.

```python
products = {
    'Laptop': 990,
    'Smartphone': 600,
    'Tablet': 250,
    'Headphones': 70,
}

for price in products.values():
    print(price)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
990
600
250
70
```

- **Iteriranje po ključevima**: Ako je potrebno iterirati po ključevima u gore navedenom rečniku ``products``, možete direktno napisati ``products.keys()`` ili ``products``.

```python
for product in products.keys():
    print(product)

# Or

for product in products:
    print(product)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
Laptop
Smartphone
Tablet
Headphones
```

- **Iteriranje preko parova ključ-vrednost**: Ako trebate iterirati preko ključa i njihovih odgovarajućih vrednosti istovremeno, možete iterirati preko ``products.items()``. Dobijate pojedinačne tuple sa ključima i njihovim odgovarajućim vrednostima.

```python
for product in products.items():
    print(product)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
('Laptop', 990)
('Smartphone', 600)
('Tablet', 250)
('Headphones', 70)
```

Da biste skladištili ključ i vrednost u zasebnim varijablama petlje, morate ih razdvojiti zarezom. Prva varijabla skladišti ključ, a druga skladišti vrednost.

```python
for product, price in products.items():
    print(product, price)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
Laptop 990
Smartphone 600
Tablet 250
Headphones 70
```

- **Funkcija**: Ako vam je potrebno iterirati kroz rečnik (dictionary) i istovremeno pratiti brojač (counter), možete pozvati funkciju ``enumerate()``. Funkcija vraća objekat ``enumerate``, koji dodeljuje ceo broj svakom elementu, kao što je brojač. Možete početi brojač od bilo kog broja, ali podrazumevano počinje od 0.

Dodeljivanje indeksa i elementa u zasebne varijable za petlju je uobičajen način korišćenja `enumerate()`. Na primer, sa `products.items()`, možete dobiti ceo par ključ-vrednost pored indeksa:

```python
for index, product in enumerate(products.items()):
    print(index, product)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
0 ('Laptop', 990)
1 ('Smartphone', 600)
2 ('Tablet', 250)
3 ('Headphones', 70)
```

Da biste prilagodili početnu vrednost brojača, možete proslediti drugi argument u ``enumerate()``. Na primer, ovde započinjemo brojanje od 1.

```python
for index, product in enumerate(products.items(), 1):
    print(index, product)
```

Molim Vas da mi dostavite tekst koji treba prevesti.

Kada mi date sadržaj, obradiću ga po sledećim pravilima:
1.  **Prevešću sav korisnički interfejs (user-facing) tekst** na srpski jezik (sr-RS).
2.  **Neću prevoditi:** kod blokove (` ```...``` `), inline kod, URL adrese, programski termini ili tehničke pojmove (kao što su JavaScript, HTML, CSS, API, itd.).
3.  Popraviću gramatičke i pravopisne greške u prevođenom tekstu.
4.  Koristiću prirodnu srpsku tehničku terminologiju.
5.  Sačuvati ću strukturu Markdown-a.

**Čekam vaš tekst.**

```md
1 ('Laptop', 990)
2 ('Smartphone', 600)
3 ('Tablet', 250)
4 ('Headphones', 70)
```

## Skupovi

- **Setovi**: Setovi su ugrađene strukture podataka u Pythonu koje ne dozvoljavaju duplikate vrednosti. Setovi su mutabilni i nepoređani, što znači da njihovi elementi nisu skladišteni u bilo kom specifičnom redosledu, pa ne možete koristiti indekse ili ključeve za pristup njima. Takođe, setovi mogu sadržati samo vrednosti nemutabilnih tipova podataka, kao što su brojevi (numbers), stringovi i tuple-i.

- **Definisanje Skupa**: Da biste definisali skup, morate napisati njegove elemente unutar vitičastih zagrada i razdvojiti ih zarezima.

```python
my_set = {1, 2, 3, 4, 5}
```

- **Definisanje Praznog Skupa**: Ako treba da definišete prazan skup, morate koristiti funkciju ``set()``. Samo pisanje praznih vitičastih zagrada će automatski kreirati rječnik.

```python
set() # Set
{}    # Dictionary
```

## Uobičajene metode Set-a

- **`add()` Metoda**: Možete dodati element u skup pomoću metode ``add()``, prosleđujući novi element kao argument.

```python
my_set.add(6)
```

**Metode**: Da biste uklonili element iz skupa (set), možete koristiti metodu ``remove()`` ili metodu ``discard()``, prosleđujući element koji želite da uklonite kao argument. Metoda ``remove()`` će baciti ``KeyError`` ako se element ne pronađe, dok metoda ``discard()`` to neće raditi.

```python
my_set.remove(4)
my_set.discard(4)
```

- **`clear()` metoda**: Metoda `clear()` uklanja sve elemente iz skupa.

```python
my_set.clear()
```

## Matematičke Operacije Skupova

- **`issubset()`<0xC2><0xA0>i `issuperset()` Metode**: Metode `issubset()` i `issuperset()` proveravaju da li je skup podskup ili nadskup drugog skupa, respektivno.

```python
my_set = {1, 2, 3, 4, 5}
your_set = {2, 3, 4, 5}

print(your_set.issubset(my_set)) # True
print(my_set.issuperset(your_set)) # True
```

- **`isdisjoint()` Metoda**: Metoda ``isdisjoint()`` proverava da li su dva skupa disjunktna, odnosno da li nemaju zajedničkih elemenata.

```python
my_set = {1, 2, 3}
your_set = {4, 5, 6}

print(my_set.isdisjoint(your_set)) # True
```

- **Operater unije (`|`)**: Operater unije ``|`` vraća novi skup sa svim elementima iz oba skupa.

```python
my_set = {1, 2, 3}
your_set = {4, 5, 6}

my_set | your_set # {1, 2, 3, 4, 5, 6}
```

- **Operater preseka (`&`)**: Operater preseka `&` vraća novi skup sa samo elementima koje je zajedničko za sklopove.

```python
my_set = {1, 2, 3, 4, 5}
your_set = {2, 3, 4, 6}

my_set & your_set # {2, 3, 4}
```

- **Operater razlike (`-`)**: Operater razlike `-` vraća novi skup sa elementima prvog skupa koji nisu u drugim skupovima.

```python
my_set = {1, 2, 3, 4, 5}
your_set = {2, 3, 4, 6}

my_set - your_set # {1, 5}
```

- **Operater simetrične razlike<0xC2><0xA0>(`^`)**: Operater simetrične razlike<0xC2><0xA0>`^`<0xC2><0xA0>vraća novi skup sa elementima koji su ili u prvom ili u drugom skupu, ali ne i u oba.

```python
my_set = {1, 2, 3, 4, 5}
your_set = {2, 3, 4, 6}

my_set ^ your_set # {1, 5, 6}
```

- **`in` Operater**: Možete proveriti da li je element u skupu ili ne pomoću operatera `in`.

```python
print(5 in my_set) # True
```

## Python Standardna biblioteka

- **Python Standard Library**: Biblioteka vam pruža unapred napisani i ponovno upotrebljiv kod, kao što su funkcije, klase i strukture podataka, koje možete koristiti u svojim projektima. Python ima ekstensivnu standardnu biblioteku sa ugrađenim modulima koji implementiraju standardizovana rešenja za mnoge probleme i zadatke. Neki primeri popularnih ugrađenih modula su ``math``, ``random``, ``re`` (skraćeno od "regular expressions"), i ``datetime``.

## Izjava za uvoz

- **Izjava za import**: Da biste pristupili elementima definisanim u ugrađenim modulima, koristite izjavu za import. Izjave za import obično se pišu na samom početku fajla. Izjave za import rade isto i za funkcije, klase, konstante, varijable i sve druge elemente definisane u modulu.

- **Osnovna izjava za uvoz**: Možete koristiti ključnu reč `import` praćenu imenom modula:

```python
import module_name
```

Zatim, ako želite da pozovete funkciju iz tog modula, koristili biste notaciju sa tačkom, uz ime modula praćeno imenom funkcije.

```python
module_name.function_name()
```

Na primer, napisali biste sledeće u vaš kod da importujete modul ``math`` i dobijete kvadratni koren iz 36:

```python
import math

math.sqrt(36)
```

- **Importovanje modula sa drugačijim imenom**: Ako morate da uvezete modul sa drugačijim imenom (poznato i kao "alias"), možete koristiti ``as`` praćenim aliasom na kraju izjave za uvoz. Ovo se često koristi za dugačka imena modula ili kako bi se izbegli sukobi imena.

```python
import module_name as module_alias
```

Na primer, da biste se na modul `math` pozvali kao `m` u vašem kodu, možete dodeliti alias na sledeći način:

```python
import math as m
```

Zatim, možete pristupiti elementima modula koristeći alias:

```python
m.sqrt(36)
```

- **Uvoz specifičnih elemenata**: Ako vam ne trebaju sve stvari iz modula, možete uvesti specifične elemente koristeći ``from``. U tom slučaju, deklaracija za uvoz počinje sa ``from``, praćena imenom modula, zatim ključnom rečju ``import`` i na kraju nazivima elemenata koje želite da uvezete.

```python
from module_name import name1, name2
```

Zatim, možete koristiti ove nazive bez prefiksa modula u vašem Python skriptu. Na primer:

```python
from math import radians, sin, cos

angle_degrees = 40
angle_radians = radians(angle_degrees)

sine_value = sin(angle_radians)
cos_value = cos(angle_radians)

print(sine_value) # 0.6427876096865393
print(cos_value)  # 0.766044443118978
```
 
Ovo je korisno, ali može dovesti do konflikata imenovanja ako već imate funkcije ili varijable istog imena. Imajte to na umu kada birate koji tip `import` naredbe želite da koristite.

Ako je potrebno dodeliti aliasima ovim imenima, možete to učiniti i koristeći ključnu reč `as` praćenu aliasom.

```python
from module_name import name1 as alias1, name2 as alias2
```

- **Izjava za uvoz sa zvezdikom (`*`)**: Zvezdica govori Pythonu da želite da uvezete sve iz tog modula, ali želite da ga uvezete tako da ne morate koristiti ime modula kao prefiks.

```python
from module_name import *
```

Na primer, ako koristite ovo za importovanje modula `math`, moći ćete da pozovete bilo koju funkciju definisanu u tom modulu bez specifikovanja imena modula kao prefiksa.

```python
from math import *
print(sqrt(36))  # 6.0
```

Međutim, ovo se generalno ne preporučuje jer može dovesti do kolizija prostora imena i otežati određivanje porekla imena.

## `if __name__ == '__main__'`

- **`__name__` Varijabla**: ``__name__`` je posebna ugrađena varijabla u Pythonu. Kada se Python fajl izvrši direktno, Python postavlja vrednost ove varijable na string ``"__main__"``. Ali ako se Python fajl uvozi kao modul u drugi Python skript, vrednost varijable ``__name__`` postavljena je na ime tog modula.

Zato ćete često naići na ovu uslovnu izjavu u Python skriptama. Sadrži kod koji želite da pokrenete **samo** ako se Python skript pokreće kao glavni program.

```python
if __name__ == '__main__': 
    # Code
```

# --assignment--
Pregledajte teme i koncepte rečnika i setova.