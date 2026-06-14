---
id: 6732b28eeadda1158cdbff7b
title: Kako možete proveriti da li niz sadrži određenu vrednost?
challengeType: 19
dashedName: how-can-you-check-if-an-array-contains-a-certain-value
---

# --interactive--

U JavaScriptu, metoda `includes()` je jednostavan i efikasan način za proveru da li niz sadrži određenu vrednost. Ova metoda vraća booleanski vrednost: `true` ako niz sadrži navedeni element, i `false` u suprotnom.

Metoda `includes()` je posebno korisna kada trebate brzo proveriti prisustvo elementa u nizu bez potrebe da znate njegovu tačnu poziciju. Počnimo sa primerom kako koristiti metodu `includes()`:

:::interactive_editor

```js
let fruits = ["apple", "banana", "orange", "mango"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("grape"));  // false
```

:::

U ovom primeru, imamo niz voća. Koristimo metod `includes()` da proverimo da li je `banana` u nizu. Vraća `true` jer je `banana` zaista prisutan. Zatim proveravamo za `grape`, što vraća `false` jer nije u nizu.

Metoda ``includes()`` je osetljiva na veličinu slova kada radi sa nizovima karaktera. To znači da su ``Banana`` sa velikim slovom B i ``banana`` sa svim malim slovima smatrani različitim vrednostima. Evo primera koji to ilustruje:

:::interactive_editor

```js
let fruits = ["apple", "banana", "orange"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("Banana")); // false
```

:::

U ovom slučaju, `banana` (sve u malim slovima) se nalazi u nizu, ali `Banana` (sa prvim slovom velikim) nije, pa drugi `includes()` poziv vraća `false`.

Metoda ``includes()`` takođe može prihvatiti opcionalni drugi parametar koji određuje poziciju u nizu od kojeg početi pretragu. Ovo je korisno ako želite da proverite prisustvo elementa u određenom delu niza. Evo kako možete koristiti ovu funkciju:

:::interactive_editor

```js
let numbers = [10, 20, 30, 40, 50, 30, 60];
console.log(numbers.includes(30, 3)); // true
console.log(numbers.includes(30, 4)); // true
```

:::

Za prvi `console.log`, tražimo broj `30` počevši od indeksa `3`. U ovom slučaju, postoji broj `30` koji se pojavljuje nakon indeksa `3`, pa metoda `includes()` vraća `true`.

Isto važi i za drugi `console.log`. Tražimo broj `30` počevši od indeksa `4`. Pošto se broj `30` pojavljuje nakon tog indeksa, onda će vratiti `true`.

Vredi napomenuti da `includes()` koristi strogo poređenje jednakosti (`===`), što znači da može razlikovati različite tipove. Na primer:

:::interactive_editor

```js
let mixedArray = [1, "2", 3, "4", 5];
console.log(mixedArray.includes(2));  // false
console.log(mixedArray.includes("2")); // true
```

:::

U ovom slučaju, broj `2` i string `"2"` se smatraju različitim tipovima podataka. Dakle, prvi `console.log` će vratiti `false`, dok drugi `console.log` će vratiti `true`.

Metoda `includes()` je moćan alat za proveru prisustva elemenata u nizovima. Lako je za upotrebu, efikasan je i može vas spasiti od pisanja složenijih petlji ili uslova za pretraživanje nizova. Bez obzira da li radite sa stringovima, brojevima ili mešovitim tipovima podataka, `includes()` pruža jednostavan način za proveru da li vrednost postoji u vašem nizu.
# --questions--

## --text--

Koji će biti izlaz sledećeg koda?

```js
let arr = [1, 2, 3, 4, 5];
console.log(arr.includes(3, 3));
```

## --answers--

`true`

### --feedback--

Drugi parametar od `includes()` određuje početnu poziciju za pretragu.
---

`false`

---

`undefined`

### --feedback--

Drugi parametar od `includes()` određuje početnu poziciju za pretragu.
---

This will throw an error.

### --feedback--

Drugi parametar od `includes()` određuje početnu poziciju za pretragu.
## --video-solution--

2

## --text--

Koji će biti izlaz sledećeg koda?

```js
let arr = ["a", "b", "c", "d", "e"];
console.log(arr.includes("C"));
```

## --answers--

`true`

### --feedback--

Zapamtite da je ``includes()`` osetljiv na veličinu slova kada radite sa nizovima (stringovima).
---

`false`

---

`undefined`

### --feedback--

Zapamtite da je ``includes()`` osetljiv na veličinu slova kada radite sa nizovima (stringovima).
---

This will throw an error.

### --feedback--

Zapamtite da je ``includes()`` osetljiv na veličinu slova kada radite sa nizovima (stringovima).
## --video-solution--

2

## --text--

Koji će biti izlaz sledećeg koda?

```js
let arr = [1, "2", 3, "4", 5];
console.log(arr.includes("3"));
```

## --answers--

`true`

### --feedback--

Metoda `includes()` koristi strogo jednakost (`===`) za poređenje.
---

`false`

---

`undefined`

### --feedback--

Metoda `includes()` koristi strogo jednakost (`===`) za poređenje.
---

This will throw an error.

### --feedback--

Metoda `includes()` koristi strogo jednakost (`===`) za poređenje.
## --video-solution--

2
