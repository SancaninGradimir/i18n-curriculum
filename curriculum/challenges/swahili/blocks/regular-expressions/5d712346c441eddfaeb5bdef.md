---
id: 5d712346c441eddfaeb5bdef
title: Linganisha nambari zote
challengeType: 1
forumTopicId: 18181
dashedName: match-all-numbers
---

# --description--

Umejifunza njia za mkato za mifumo ya kawaida ya mfuatano wa herufi kama herufi na nambari. Mfumo mwingine wa kawaida ni kutafuta tu tarakimu au nambari.

Njia ya mkato ya kutafuta herufi za tarakimu ni `\d`, kwa herufi ndogo `d`. Hii ni sawa na darasa la herufi `[0-9]`, ambalo linatafuta herufi moja ya nambari yoyote kati ya sifuri na tisa.

# --instructions--

Tumia darasa la herufi la njia ya mkato `\d` kuhesabu ni tarakimu ngapi zipo katika vichwa vya filamu. Nambari zilizoandikwa kwa maneno ("sita" badala ya 6) hazihesabiwi.

# --hints--

Standardni način unosa bi trebalo da koristi prečicu karaktera za pronalaženje cifara

```js
assert(/\\d/.test(numRegex.source));
```

Vaša uobičajena izjava treba da koristi globalnu zastavicu.

```js
assert(numRegex.global);
```

Usemi wako wa kawaida unapaswa kupata tarakimu 1 katika mfuatano `9`.

```js
assert('9'.match(numRegex).length == 1);
```

Usemi wako wa kawaida unapaswa kupata tarakimu 2 katika mfuatano `Catch 22`.

```js
assert('Catch 22'.match(numRegex).length == 2);
```

Usemi wako wa kawaida unapaswa kupata tarakimu 3 katika mfuatano `101 Dalmatians`.

```js
assert('101 Dalmatians'.match(numRegex).length == 3);
```

Usemi wako wa kawaida unapaswa kupata tarakimu 0 katika mfuatano `One, Two, Three`.

```js
assert('One, Two, Three'.match(numRegex) == null);
```

Usemi wako wa kawaida unapaswa kupata tarakimu 2 katika mfuatano `21 Jump Street`.

```js
assert('21 Jump Street'.match(numRegex).length == 2);
```

Vaše uobičajeno ime treba da sadrži cifru 4 u sekvenci `2001: A Space Odyssey`.

```js
assert('2001: A Space Odyssey'.match(numRegex).length == 4);
```

# --seed--

## --seed-contents--

```js
let movieName = "2001: A Space Odyssey";
let numRegex = /change/; // Change this line
let result = movieName.match(numRegex).length;
```

# --solutions--

```js
let movieName = "2001: A Space Odyssey";
let numRegex = /\d/g; // Change this line
let result = movieName.match(numRegex).length;
```
