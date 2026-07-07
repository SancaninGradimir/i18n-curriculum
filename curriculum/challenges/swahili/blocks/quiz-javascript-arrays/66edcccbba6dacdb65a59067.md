---
id: 66edcccbba6dacdb65a59067
title: Pokušao sam da napišem redove podataka za JavaScript
challengeType: 8
dashedName: quiz-javascript-arrays
---

# --description--

Da biste položili kratki test, morate tačno odgovoriti na najmanje 18 od 20 pitanja koja su navedena ispod.

# --quizzes--

## --quiz--

### --question--

#### --text--

Šta će biti rezultat sledećeg koda?

```js
const numbers = [1, 2, 3];
console.log(numbers[10]);
```

#### --distractors--

`[1, 2, 3]`

[No Swahili text provided.]

`null`

[No Swahili text provided.]

`10`

#### --answer--

`undefined`

### --question--

#### --text--

Koji od sljedećih načina je ispravan za dobijanje sekvence slova `"Jessica"` iz niza podataka `developers`?

#### --distractors--

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[1]
```

[No Swahili text provided.]

```js
const developers = ["Jessica", "Naomi", "Tom"];
developers[2]
```

[No Swahili text provided.]

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

Koja vrednost će biti data za parametar `index`?

```js
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(20);
console.log(index);
```

#### --distractors--

2

[No Swahili text provided.]

3

[No Swahili text provided.]

-1

#### --answer--

1

### --question--

#### --text--

Šta radi sintaksa REST?

#### --distractors--

Koristi se za podelu sekvence karaktera u niz manjih segmenata.

[No Swahili text provided.]

Koristi se za dodavanje ili uklanjanje elemenata iz bilo kog dela niza podataka.

[No Swahili text provided.]

Koristi se za dodavanje elemenata na kraj niza podataka i vraća novu dužinu.

#### --answer--

Prikuplja preostale elemente iz reda podataka i postavlja ih u novi red.

### --question--

#### --text--

Šta je rešenje za strukturu podataka?

#### --distractors--

Koristi se za spajanje svih elemenata niza podataka u jedan niz znakova/string.

[No Swahili text provided.]

Koristi se za proveru da li niz podataka ima određenu vrednost.

[No Swahili text provided.]

Koristi se za uklanjanje poslednjeg elementa iz niza podataka i vraćanje tog uklonjenog elementa.

#### --answer--

Koristi se za izvlačenje vrednosti iz kolona podataka i njihovo predstavljanje u skraćenim i lakše čitljivim parametrima.

### --question--

#### --text--

Koja vrednost će biti dodeljena parametru `arr2`?

```js
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2);
```

#### --distractors--

`[4, 5, 1, 2, 3]`

[No Swahili text provided.]

`[1, 2, [3, 4, 5]]`

[No Swahili text provided.]

`[1, 2, 3]`

#### --answer--

`[1, 2, 3, 4, 5]`

### --question--

#### --text--

Šta će ovaj kod napisati na konzolu?

```js
const colors = ["red", "blue", "green", "yellow"];
colors.splice(1, 2, "purple");
console.log(colors);
```

#### --distractors--

`["red", "blue", "green", "yellow"]`

[No Swahili text provided.]

`["red", "blue", "yellow"]`

[No Swahili text provided.]

`["red", "yellow"]`

#### --answer--

`["red", "purple", "yellow"]`

### --question--

#### --text--

Koja vrednost će biti dodeljena parametru `slicedArr`?

```js
const arr = ["apple", "banana", "cherry", "date"];
const slicedArr = arr.slice(1, 3);
console.log(slicedArr);
```

#### --distractors--

`["apple", "banana"]`

[No Swahili text provided.]

`["cherry", "date"]`

[No Swahili text provided.]

`["apple", "cherry"]`

#### --answer--

`["banana", "cherry"]`

### --question--

#### --text--

Koja funkcija vraća prvu instancu određene karakteristike u nizu podataka?

#### --distractors--

`firstIndex()`

[No Swahili text provided.]

`lastIndex()`

[No Swahili text provided.]

`searchIndex()`

#### --answer--

`indexOf()`

### --question--

#### --text--

Koja se metoda koristi za uklanjanje prvog elementa iz niza podataka i vraćanje tog uklonjenog elementa?

#### --distractors--

`pop()`

[No Swahili text provided.]

`slice()`

[No Swahili text provided.]

`splice()`

#### --answer--

`shift()`

### --question--

#### --text--

Šta radi put `concat()`?

#### --distractors--

Spaja elemente niza podataka u niz znakova.

[No Swahili text provided.]

Dodaje element na početak reda podataka.

[No Swahili text provided.]

Uklanja element iz niza podataka.

#### --answer--

Spoji dve kolone podataka u jednu novu kolonu.

### --question--

#### --text--

Šta će biti rezultat ovog koda?

```js
const fruits = ["apple", "banana", "cherry", "apple", "orange"];

fruits.splice(0, 1);

console.log(fruits);
```

#### --distractors--

`["apple", "banana", "cherry", "apple", "orange"]`

[No Swahili text provided.]

`["apple", "banana", "cherry"]`

[No Swahili text provided.]

`["cherry", 'apple']`

#### --answer--

`["banana", "cherry", "apple", "orange"]`

### --question--

#### --text--

Šta radi putnica `includes()`?

#### --distractors--

Koristi se za podelu sekvence karaktera u niz manjih segmenata.

[No Swahili text provided.]

Koristi se za spajanje svih elemenata niza podataka u jedan niz znakova/string.

[No Swahili text provided.]

Koristi se za dodavanje ili uklanjanje elemenata iz bilo kog dela niza podataka.

#### --answer--

Koristi se za proveru da li niz podataka ima određenu vrednost.

### --question--

#### --text--

Koji od sledećih načina se koristi za konverziju reda podataka na njegovo mesto?

#### --distractors--

`reversed()`

[No Swahili text provided.]

`reverseArr()`

[No Swahili text provided.]

`reversing()`

#### --answer--

`reverse()`

### --question--

#### --text--

Šta je niz podataka sa dve dimenzije?

#### --distractors--

Niz podataka koji sadrži samo elemente tipa *object literals*.

[No Swahili text provided.]

Niz podataka sa fiksnom dužinom.

[No Swahili text provided.]

Niz podataka decimalnih brojeva.

#### --answer--

Niz redova podataka.

### --question--

#### --text--

Šta je tačno o načinu `indexOf()` u redovima podataka?

#### --distractors--

Uvek osveži poslednji događaj komponente.

[No Swahili text provided.]

Baciće grešku ako element nije pronađen.

[No Swahili text provided.]

Potreban je red podataka koji je organizovan.

#### --answer--

Hurejesha `-1` ako element nije pronađen.

### --question--

#### --text--

Koja od sledećih metoda NIJE metoda za red podataka?

#### --distractors--

`includes()`

[No Swahili text provided.]

`pop()`

[No Swahili text provided.]

`push()`

#### --answer--

`trim()`

### --question--

#### --text--

Šta će biti rezultat sledećeg koda?

```js
const arr = ["o", "l", "l", "e", "h"];
console.log(arr.join(""));
```

#### --distractors--

`["o", "l", "l", "e", "h"]`

[No Swahili text provided.]

`"hello"`

[No Swahili text provided.]

`undefined`

#### --answer--

`"olleh"`

### --question--

#### --text--

Rezultat korišćenja metode `shift()` na praznom redu će biti?

#### --distractors--

`TypeError`

[No Swahili text provided.]

`[]`

[No Swahili text provided.]

`null`

#### --answer--

`undefined`

### --question--

#### --text--

Koja će putanja vratiti novi red bez menjanja prvobitnog reda?

#### --distractors--

`shift()`

[No Swahili text provided.]

`pop()`

[No Swahili text provided.]

`push()`

#### --answer--

`slice()`