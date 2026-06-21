id: 691f7773cddba1caf1bf5ecb
title: "Vežba 132: Uklonite najčešće ponavljane elemente"
challengeType: 28
dashedName: challenge-132
---

# --description--

Iz niza podataka sa različitim vrednostima, uklonite sve pojavljivanja elementa koji se najčešće ponavljaju i vratite preostali niz podataka.

- Ako više vrednosti izgleda da se ponavljaju najviše puta, uklonite sve njih.
- Ne menjajte druge elemente niti njihov redosled.

# --hints--

`purgeMostFrequent([1, 2, 2, 3])` bi trebalo da vrati `[1, 3]`.

```js
assert.deepEqual(purgeMostFrequent([1, 2, 2, 3]), [1, 3]);
```

`purgeMostFrequent(["a", "b", "d", "b", "c", "d", "c", "d", "c", "d"])` bi trebalo da vrati `["a", "b", "b", "c", "c", "c"]`.

```js
assert.deepEqual(purgeMostFrequent(["a", "b", "d", "b", "c", "d", "c", "d", "c", "d"]), ["a", "b", "b", "c", "c", "c"]);
```

`purgeMostFrequent(["red", "blue", "green", "red", "blue", "green", "blue"])` bi trebalo da vrati `["red", "green", "red", "green"]`.

```js
assert.deepEqual(purgeMostFrequent(["red", "blue", "green", "red", "blue", "green", "blue"]), ["red", "green", "red", "green"]);
```

`purgeMostFrequent([5, 5, 5, 5])` bi trebalo da vrati `[]`.

```js
assert.deepEqual(purgeMostFrequent([5, 5, 5, 5]), []);
```

`purgeMostFrequent([10, 12, 7, 3, 7, 7, 12, 12])` bi trebalo da vrati `[10, 3]`.

```js
assert.deepEqual(purgeMostFrequent([10, 12, 7, 3, 7, 7, 12, 12]), [10, 3]);
```

# --seed--

## --seed-contents--

```js
function purgeMostFrequent(arr) {

  return arr;
}
```

# --solutions--

```js
function purgeMostFrequent(arr) {
  const freq = {};
  for (const val of arr) {
    freq[val] = (freq[val] || 0) + 1;
  }

  const maxFreq = Math.max(...Object.values(freq));

  const toRemove = new Set(
    Object.keys(freq).filter(key => freq[key] === maxFreq)
  );

  return arr.filter(val => !toRemove.has(String(val)));
}
```