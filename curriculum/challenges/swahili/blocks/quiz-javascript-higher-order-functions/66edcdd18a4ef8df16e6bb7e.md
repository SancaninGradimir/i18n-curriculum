---
id: 66edcdd18a4ef8df16e6bb7e
title: Kviz o funkcijama višeg reda u JavaScriptu
challengeType: 8
dashedName: quiz-javascript-higher-order-functions
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koja od sledećih tvrdnji o funkcijama višeg reda u JavaScriptu nije tačna?
#### --distractors--
Funkcije višeg reda mogu značajno poboljšati čitljivost i održivost koda omogućavanjem tehnika funkcionalnog programiranja.

---

Funkcije višeg reda, kao što su `map`, `filter` i `reduce`, su moćni alati za manipulaciju nizovima, ali nisu jedinstveni samo za funkcionalno programiranje.

---

Funkcije višeg reda mogu uvesti složenost u razumevanje koda, ali takođe mogu dovesti do ekspresivnijih i konciznijih rešenja.
#### --answer--
Sve funkcije u JavaScriptu, uključujući one koje ne uzimaju niti vraćaju druge funkcije, mogu se klasifikovati kao funkcije višeg reda.
### --question--

#### --text--
Šta je factory funkcija u kontekstu funkcija višeg reda?
#### --distractors--
Funkcija koja stvara nove varijable.

---

Funkcija koja radi isključivo sa stringovima.

---

Funkcija koja automatski generiše komentare koda.
#### --answer--
Funkcija koja vraća novu funkciju na osnovu specifičnih parametara
### --question--

#### --text--
Nakon izvršavanja koda, koja će biti vrednost za `forEachRes` i `mapRes`?

```js
const numbers = [1, 1, 1, 1, 1];
let sum = 0;
const forEachRes = numbers.forEach(num => {
  return (sum += num);
});
const mapRes = numbers.map(num => {
  return (sum += num);
});
```

#### --distractors--
`forEachRes` je `undefined` i `mapRes` je `[1,2,3,4,5]`

---

`forEachRes` je `0` i `mapRes` je `[1,2,3,4,5]`

---

`forEachRes` je `5` i `mapRes` je `[1,2,3,4,5]`
#### --answer--
`forEachRes` je `undefined` i `mapRes` je `[6,7,8,9,10]`
### --question--

#### --text--
Koji je rezultat ovog koda?

```js
[, undefined, 'a', 'b', { 20: 5 }].sort();
```

#### --distractors--
Nisu podržani elementi za sortiranje niza, zbog čega je nastala greška.

---

Callback not supplied, hence error.

---

```js
[empty, 'a', 'b', undefined, { '20': 5 }]
```

#### --answer--

```js
[{ '20': 5 }, 'a', 'b', undefined, empty]
```

### --question--

#### --text--
Koja od sledećih opisa callback funkciju u JavaScript-u?
#### --distractors--
Funkcija koja se poziva odmah nakon deklaracije.

---

Funkcija koja se poziva sa specifičnim kontekstom.

---

Funkcija koja vraća drugu funkciju.
#### --answer--
Funkcija koja se prosleđuje kao argument drugoj funkciji i koja će biti izvršena logikom te funkcije.
### --question--

#### --text--
Koji je rezultat korišćenjem `reduce()` na nizu?
#### --distractors--
Booleanski tip podataka koji ukazuje da li bilo koji element zadovoljava određeni uslov.

---

Niz sa svim elementima redukovanim pomoću zadane funkcije povratne pozive.

---

Niz boolean vrednosti.
#### --answer--
To zavisi od početne vrednosti akumulatora i funkcije povratnog poziva.
### --question--

#### --text--
Kako se metoda `sort()` ponaša ako nije dostavljena funkcija za poređenje pri numeričkom sortiranju?
#### --distractors--
Popunjava prazne utičnice sa `null`.

---

Vraća niz specijalnih znakova.

---

Sortira niz u opadajućem redosledu.
#### --answer--
Sortira niz kao stringove na osnovu UTF-16 kodnih jedinica.
### --question--

#### --text--
Koja je svrha metode `some()` u JavaScript-u?
#### --distractors--
Kreiranje novog niza sa rezultatima funkcije primenjene na svaki element.

---

Iterirati kroz niz bez proizvodnje rezultata.

---

Redukuje niz na jednu vrednost zasnovano na funkciji povratne pozive.
#### --answer--
Za određivanje da li bilo koji elementi u nizu zadovoljavaju određeni uslov/test.
### --question--

#### --text--
Koji od sledećih predstavlja validan primer metodskog lančevanja?
#### --distractors--

```js
Math.random();
```

---

```js
array.push(1).pop();
```

---

```js
console.log('Hello');
```

#### --answer--

```js
str.toLowerCase().trim().replace(' ', '_');
```

### --question--

#### --text--
Koji je izlaz sledećeg koda?

```js
let numbers = [2, 4, 8, 10];

numbers.forEach(function(number) {
    console.log(number % 2);
});
```

#### --distractors--

`2 4 8 10`

---

`null null null null`

---

`1 2 4 5`

#### --answer--

`0 0 0 0`

### --question--

#### --text--
Koja od sledećih predstavlja prednost metodnog lančanja?
#### --distractors--
Inherentno optimizuje performanse smanjenjem vremena izvršavanja funkcija.

---

Uklanja potrebu za privremenim varijablama, ali može povećati korišćenje memorije u nekim slučajevima.

---

Omogućava da je rukovanje greškama i debagiranje jednostavnije.
#### --answer--
Pomaže u pojednostavljanju sintakse i kreiranju čitljivijeg koda tako što omogućava više operacija unutar jednog izraza.
### --question--

#### --text--
Kako možete sortirati niz objekata po specifičnom svojstvu koristeći metod ``sort``?
#### --distractors--
Metoda ``sort`` ne može da sortira objekte.

---

Koristite metodu `reverse` nakon sortiranja.

---

Konvertujte objekte u stringove i sortirajte ih.
#### --answer--
Koristite funkciju za poređenje koja poredi vrednosti svojstava.
### --question--

#### --text--
Kod lančovanja metoda, koja je uobičajena praksa za poboljšanje jasnoće i debagovanja?
#### --distractors--
Koristite manje metoda u lancu.

---

Izbegavajte lančanje metoda koje vraćaju samo primitivne vrednosti.

---

Koristite samo ugrađene metode.
#### --answer--
Podeliti dugačke lance u više koraka.
### --question--

#### --text--
Koja je potencijalna mana prekomernog korišćenja metodnog lančanja u vašem kodu?
#### --distractors--
To usporava izvršavanje koda.

---

Sprečava korišćenje komentara.

---

Povećava veličinu fajla.
#### --answer--
Ovo može otežati debagovanje koda.
### --question--

#### --text--
Koja metoda biste koristili da utvrdite da li su svi elementi u nizu stringovi?
#### --distractors--

`some()`

---

`everyInstance()`

---

`filter()`

#### --answer--

`every()`

### --question--

#### --text--
Koja će biti vrednost `originalArray` nakon izvršavanja sledećeg koda?

```js
const originalArray = [{ id: 1 }, { id: 2 }, { id: 3 }];
const filteredArray = originalArray.filter(item => item.id > 1);
filteredArray[0].id = 4;
```

#### --distractors--

`[{ id: 1 }, { id: 2 }, { id: 3 }]`

---

`[{ id: 1 }]`

---

`[{ id: 4 }, { id: 2 }, { id: 3 }]`

#### --answer--

`[{ id: 1 }, { id: 4 }, { id: 3 }]`
### --question--

#### --text--
Koja će biti vrednost `shortWords` nakon izvršavanja sledećeg koda?

```js
const words = ['apple', 'banana', 'pear', 'kiwi'];
const shortWords = words.filter(word => word.length <= 5);
```

#### --distractors--

`[]`

---

`['pear', 'kiwi']`

---

`['apple', 'banana']`

#### --answer--

`['apple', 'pear', 'kiwi']`

### --question--

#### --text--
Koja je svrha prosleđivanja inicijalne vrednosti kao argumenta metodi `reduce()`?
#### --distractors--
Za postavljanje dužine niza.

---

Da ograniči broj iteracija.

---

Za određivanje tipa povratne vrednosti funkcije.
#### --answer--
Za definisanje početne vrednosti akumulatora.
### --question--

#### --text--
Da li se metoda `map` može koristiti na objektima koji nisu nizovi?
#### --distractors--
Da, može se koristiti na bilo kom objektu.

---

Da, ali samo na objekatima sa numeričkim svojstvima.

---

To zavisi od verzije JavaScripta.
#### --answer--
Ne, specifično je dizajnirano za nizove (arrays).
### --question--

#### --text--
Koja je primarna svrha metode ``map`` u JavaScript-u?
#### --distractors--
Da se sortira niz i vrati novi niz, pri čemu se očuvava originalni redosled.

---

Za filtriranje elemenata iz niza i uklanjanje ili dodavanje elemenata na osnovu uslova.

---

Pronalaženje specifičnog elementa u nizu i vraćanje njegovog indeksa zajedno sa samim elementom.
#### --answer--
Da kreira novi niz koji sadrži rezultate pozivanja priložene funkcije na svaki element u početnom nizu.