---
id: af2170cad53daa0770fabdea
title: Implementirati Mutacije Algoritam
challengeType: 26
dashedName: implement-the-mutations-algorithm
---

# --description--

**Cilj:** Ispunite korisničke priče ispod i osigurajte da svi testovi prođu kako biste završili laboratoriju.

**Korisničke priče:**

1. Kreirajte funkciju pod nazivom `mutation` koja prima niz kao argument.
1. `mutation` bi trebalo da vrati `true` ako string u prvom elementu niza sadrži sva slova stringa iz drugog elementa niza, i `false` inače. Primer:
    - `mutation(["hello", "Hello"])`, bi trebalo da vrati `true` jer su sva slova u drugom stringu prisutna u prvom, bez obzira na veličinu (case).
    - `mutation(["hello", "hey"])` bi trebalo da vrati `false` jer string `hello` ne sadrži `y`.
    - `mutation(["Alien", "line"])`, bi trebalo da vrati `true` jer su sva slova u `line` prisutna u `Alien`.

# --hints--

`mutation(["hello", "hey"])` should return `false`.

```js
assert.isFalse(mutation(['hello', 'hey']));
```

`mutation(["hello", "Hello"])` should return `true`.

```js
assert.isTrue(mutation(['hello', 'Hello']));
```

`mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"])` should return `true`.

```js
assert.isTrue(mutation(['zyxwvutsrqponmlkjihgfedcba', 'qrstu']));
```

`mutation(["Mary", "Army"])` should return `true`.

```js
assert.isTrue(mutation(['Mary', 'Army']));
```

`mutation(["Mary", "Aarmy"])` should return `true`.

```js
assert.isTrue(mutation(['Mary', 'Aarmy']));
```

`mutation(["Alien", "line"])` should return `true`.

```js
assert.isTrue(mutation(['Alien', 'line']));
```

`mutation(["floor", "for"])` should return `true`.

```js
assert.isTrue(mutation(['floor', 'for']));
```

`mutation(["hello", "neo"])` should return `false`.

```js
assert.isFalse(mutation(['hello', 'neo']));
```

`mutation(["voodoo", "no"])` should return `false`.

```js
assert.isFalse(mutation(['voodoo', 'no']));
```

`mutation(["ate", "date"])` should return `false`.

```js
assert.isFalse(mutation(['ate', 'date']));
```

`mutation(["Tiger", "Zebra"])` should return `false`.

```js
assert.isFalse(mutation(['Tiger', 'Zebra']));
```

`mutation(["Noel", "Ole"])` should return `true`.

```js
assert.isTrue(mutation(['Noel', 'Ole']));
```

# --seed--

## --seed-contents--

```js
```

# --solutions--

```js
function mutation(arr) {
  let hash = Object.create(null);

  arr[0]
    .toLowerCase()
    .split('')
    .forEach(c => (hash[c] = true));

  return !arr[1]
    .toLowerCase()
    .split('')
    .filter(c => !hash[c]).length;
}

mutation(['hello', 'hey']);
```
