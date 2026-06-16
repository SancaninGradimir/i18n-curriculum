---
id: 66edcccbba6dacdb65a59067
title: Kviz o JavaScript nizovima
challengeType: 8
dashedName: quiz-javascript-arrays
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koji će biti izlaz za sledeći kod?

```js
const numbers = [1, 2, 3];
console.log(numbers[10]);
```

#### --distractors--

`[1, 2, 3]`

---

`null`

---

`10`

#### --answer--

`undefined`

### --question--

#### --text--
Koji od sledećih načina je ispravan za pristup stringu `"Jessica"` iz niza `developers`?
#### --distractors--

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[1]
```

---

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[2]
```

---

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[-1]
```

#### --answer--

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[0]
```

### --question--

#### --text--
Koja vrednost će biti dodeljena promenljivoj `index`?

```js
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(20);
console.log(index);
```

#### --distractors--
2

---

3

---

-1
#### --answer--
1
### --question--

#### --text--
Šta radi rest sintaksa?
#### --distractors--
Služi za razdvajanje stringa u niz podnizaka.

---

Koristi se za dodavanje ili uklanjanje elemenata sa bilo koje pozicije u nizu (array).

---

Koristi se za dodavanje elemenata na kraj niza i vraća novu dužinu.
#### --answer--
Uzima preostale elemente iz niza i stavlja ih u novi niz.
### --question--

#### --text--
Šta je dekonstrukcija nizova?
#### --distractors--
Služi za spajanje svih elemenata niza u jedan string.

---

Koristi se za proveru da li niz sadrži određenu vrednost.

---

Služi za uklanjanje poslednjeg elementa iz niza i vraća taj uklonjeni element.
#### --answer--
Koristi se za izvlačenje vrednosti iz nizova i dodeljivanje ih promenljivama na koncizniji i čitljiviji način.
### --question--

#### --text--
Koja vrednost će biti dodeljena promenljivoj `arr2`?

```js
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2);
```

#### --distractors--

`[4, 5, 1, 2, 3]`

---

`[1, 2, [3, 4, 5]]`

---

`[1, 2, 3]`

#### --answer--

`[1, 2, 3, 4, 5]`

### --question--

#### --text--
Šta će ovaj kod da ispisa u konzolu?

```js
const colors = ["red", "blue", "green", "yellow"];
colors.splice(1, 2, "purple");
console.log(colors);
```

#### --distractors--

`["red", "blue", "green", "yellow"]`

---

`["red", "blue", "yellow"]`

---

`["red", "yellow"]`

#### --answer--

`["red", "purple", "yellow"]`

### --question--

#### --text--
Koja vrednost će biti dodeljena promenljivoj `slicedArr`?

```js
const arr = ["apple", "banana", "cherry", "date"];
const slicedArr = arr.slice(1, 3);
console.log(slicedArr);
```

#### --distractors--

`["apple", "banana"]`

---

`["cherry", "date"]`

---

`["apple", "cherry"]`

#### --answer--

`["banana", "cherry"]`

### --question--

#### --text--
Koji metod vraća prvi indeks određenog elementa u nizu?
#### --distractors--

`firstIndex()`

---

`lastIndex()`

---

`searchIndex()`

#### --answer--

`indexOf()`

### --question--

#### --text--
Koji metod se koristi za uklanjanje prvog elementa iz niza i vraćanje tog uklonjenog elementa?
#### --distractors--

`pop()`

---

`slice()`

---

`splice()`

#### --answer--

`shift()`

### --question--

#### --text--
Šta radi metoda `concat()`?
#### --distractors--
Spaja elemente niza u string.

---

Dodaje element na početak niza.

---

Uklanja element iz niza.
#### --answer--
Spaja dva niza u novi niz.
### --question--

#### --text--
Koji će biti rezultat izvršavanja ovog koda?

```js
const fruits = ["apple", "banana", "cherry", "apple", "orange"];

fruits.splice(0, 1);

console.log(fruits);
```

#### --distractors--

`["apple", "banana", "cherry", "apple", "orange"]`

---

`["apple", "banana", "cherry"]`

---

`["cherry", 'apple']`

#### --answer--

`["banana", "cherry", "apple", "orange"]`

### --question--

#### --text--
Šta radi metoda `includes()`?
#### --distractors--
Služi za razdvajanje stringa u niz podnizaka.

---

Koristi se za konkatenisanje svih elemenata niza u jedan string.

---

Koristi se za dodavanje ili uklanjanje elemenata sa bilo koje pozicije u nizu (array).
#### --answer--
Koristi se za proveru da li niz sadrži određenu vrednost.
### --question--

#### --text--
Koji od sledećih metoda se koristi za obrnjavanje niza na mestu?
#### --distractors--

`reversed()`

---

`reverseArr()`

---

`reversing()`

#### --answer--

`reverse()`

### --question--

#### --text--
Šta je dvodimenzionalni niz?
#### --distractors--
Niz koji sadrži samo literalne objekte.

---

Niz fiksne dužine.

---

Niz od brojeva sa fiksnim zarezom (float).
#### --answer--
Niz nizova.
### --question--

#### --text--
Koja od sledećih tvrdnji je tačna o metodi `indexOf()` u nizovima?
#### --distractors--
Uvek vraća poslednju pojavu elementa.

---

Izbacuje grešku ako element nije pronađen.

---

Niz mora biti sortirano.
#### --answer--
Vraća `-1` ako element nije pronađen.
### --question--

#### --text--
Koji od sledećih nije metoda niza (array method)?
#### --distractors--

`includes()`

---

`pop()`

---

`push()`

#### --answer--

`trim()`

### --question--

#### --text--
Koji će biti izlaz za sledeći kod?

```js
const arr = ["o", "l", "l", "e", "h"];
console.log(arr.join(""));
```

#### --distractors--

`["o", "l", "l", "e", "h"]`

---

`"hello"`

---

`undefined`

#### --answer--

`"olleh"`

### --question--

#### --text--
Koji će biti rezultat korišćenja metode `shift()` na praznom nizu?


#### --distractors--

`TypeError`

---

`[]`

---

`null`

#### --answer--

`undefined`

### --question--

#### --text--
Koja metoda će vratiti novi niz bez menjanja originalnog niza?
#### --distractors--

`shift()`

---

`pop()`

---

`push()`

#### --answer--

`slice()`
