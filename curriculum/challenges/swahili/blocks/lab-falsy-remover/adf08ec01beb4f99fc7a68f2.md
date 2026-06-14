---
id: adf08ec01beb4f99fc7a68f2
title: Implementirajte uklonač lažnih vrednosti
challengeType: 26
dashedName: implement-a-falsy-remover
---

# --description--

U ovom laboratorijumu ćete kreirati funkciju koja uklanja sve lažne vrednosti iz niza.

Lažne vrednosti u JavaScriptu su `false`, `null`, `0`, `""`, `undefined`, i `NaN`.

**Cilj**: Ispunite korisničke priče ispod i prođite sve testove kako biste završili laboratorijum.

**Korisničke priče:**

1. Trebalo bi da imate funkciju `bouncer` koja prima niz kao argument.
1. Funkcija `bouncer` bi trebalo da vrati novi niz koji sadrži iste elemente kao i niz prosleđen kao argument, ali bez lažnih elemenata.
1. Funkcija `bouncer` ne bi trebalo da promeni niz prosleđen kao argument.

Savet: Pokušajte da svaku vrednost konvertujete u Boolean.

# --hints--

You should have a `bouncer` function.

```js
assert.isFunction(bouncer);
```

`bouncer([7, "ate", "", false, 9])` should return `[7, "ate", 9]`.

```js
assert.deepEqual(bouncer([7, 'ate', '', false, 9]), [7, 'ate', 9]);
```

`bouncer(["a", "b", "c"])` should return `["a", "b", "c"]`.

```js
assert.deepEqual(bouncer(['a', 'b', 'c']), ['a', 'b', 'c']);
```

`bouncer([false, null, 0, NaN, undefined, ""])` should return `[]`.

```js
assert.deepEqual(bouncer([false, null, 0, NaN, undefined, '']), []);
```

`bouncer([null, NaN, 1, 2, undefined])` should return `[1, 2]`.

```js
assert.deepEqual(bouncer([null, NaN, 1, 2, undefined]), [1, 2]);
```

The `bouncer` function should not mutate the array passed in as argument.

```js
const arr = ['a', false, 0, 'Naomi'];
bouncer(arr);
assert.deepEqual(arr, ['a', false, 0, 'Naomi']);
```

`bouncer([])` should return `[]`.  

```js  
assert.deepEqual(bouncer([]), []);  
```  

# --seed--

## --seed-contents--

```js

```

# --solutions--

```js
function bouncer(arr) {
  return arr.filter(e => e);
}
```
