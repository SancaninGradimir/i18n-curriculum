---
id: afd15382cdfb22c9efe8b7de
title: Implementiraj generator parova DNK
challengeType: 26
dashedName: implement-a-dna-pair-generator
---

# --description--

U dvokraičnoj spirali DNK, baze su uvek uparene: ako na jednoj niti postoji baza <em>A</em>, na drugoj niti direktno napred postoji baza <em>T</em>, druga para je <em>C</em> i <em>G</em>.

U ovom laboratorijskom zadatku, napisaćete funkciju koja će upariti nedostajuće parove baza za dati DNK niz. Za svaki karakter u dato nizu, pronađite karakter para bazi.

Na primer, za ulaz `ATCG`, vratiti `[["A", "T"], ["T", "A"], ["C", "G"], ["G", "C"]]`

Baza <em>A</em> uparena je sa bazom <em>T</em>, baza <em>T</em> uparena je sa bazom <em>A</em>, <em>C</em> je uparen sa bazom <em>G</em>, a na kraju baza <em>G</em> je uparena sa bazom <em>C</em>.

**Cilj**: Ispunite korisničke priče ispod i prođite sve testove kako biste završili laboratorijski zadatak.

**Korisničke priče:**

1. Trebalo bi da imate funkciju `pairElement` koja prima niz bilo koje dužine kao argument.
1. Funkcija `pairElement` bi trebalo da vrati 2D niz (array), gde svaki unutrašnji niz ima dva niza, prvi niz je jedna baza iz ulaza, a drugi niz uparena baza.
1. Kada primi `A`, funkcija bi trebalo da ga upari sa `T`.
1. Kada primi `T`, funkcija bi trebalo da ga upari sa `A`.
1. Kada primi `C`, funkcija bi trebalo da ga upari sa `G`.
1. Kada primi `G`, funkcija bi trebalo da ga upari sa `C`.

# --hints--

You should create a function named `pairElement`.

```js
assert.isFunction(pairElement);
```

`pairElement` should take a single argument.

```js
assert.lengthOf(pairElement, 1);
```

`pairElement("ATCGA")` should return `[["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]]`.

```js
assert.deepEqual(pairElement('ATCGA'), [
  ['A', 'T'],
  ['T', 'A'],
  ['C', 'G'],
  ['G', 'C'],
  ['A', 'T']
]);
```

`pairElement("TTGAG")` should return `[["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]]`.

```js
assert.deepEqual(pairElement('TTGAG'), [
  ['T', 'A'],
  ['T', 'A'],
  ['G', 'C'],
  ['A', 'T'],
  ['G', 'C']
]);
```

`pairElement("CTCTA")` should return `[["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]]`.

```js
assert.deepEqual(pairElement('CTCTA'), [
  ['C', 'G'],
  ['T', 'A'],
  ['C', 'G'],
  ['T', 'A'],
  ['A', 'T']
]);
```

# --seed--

## --seed-contents--

```js

```

# --solutions--

```js
var lookup = Object.create(null);
lookup.A = 'T';
lookup.T = 'A';
lookup.C = 'G';
lookup.G = 'C';

function pairElement(str) {
 return str.split('').map(function(p) {return [p, lookup[p]];});
}
```
