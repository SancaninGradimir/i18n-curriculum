id: 691f7773cddba1caf1bf5eca
title: "Vežba 131: Parovi"
challengeType: 28
dashedName: challenge-131
---

# --description--

Ako vam je dat niz celih brojeva i ciljna brojka, pronađite sve parove elemenata u nizu čije vrednosti sabiraju na ciljni broj i vratite zbir njihovih indeksa.

Na primer, ako dobijete `[2, 3, 4, 6, 8]` i `10`, pronaći ćete dva validna para:

- `2` i `8` (2 + 8 = 10), njihovi indeksi su `0` i `4`
- `4` i `6` (4 + 6 = 10), njihovi indeksi su `2` i `3`

Saberi sve indekse da biste dobili povratnu vrednost od `9`.

# --hints--

`pairwise([2, 3, 4, 6, 8], 10)` treba da vrati `9`.

```js
assert.equal(pairwise([2, 3, 4, 6, 8], 10), 9);
```

`pairwise([4, 1, 5, 2, 6, 3], 7)` treba da vrati `15`.

```js
assert.equal(pairwise([4, 1, 5, 2, 6, 3], 7), 15);
```

`pairwise([-30, -15, 5, 10, 15, -5, 20, -40], -20)` treba da vrati `22`.

```js
assert.equal(pairwise([-30, -15, 5, 10, 15, -5, 20, -40], -20), 22);
```

`pairwise([7, 9, 13, 19, 21, 6, 3, 1, 4, 8, 12, 22], 24)` treba da vrati `10`.

```js
assert.equal(pairwise([7, 9, 13, 19, 21, 6, 3, 1, 4, 8, 12, 22], 24), 10);
```

# --seed--

## --seed-contents--

```js
function pairwise(arr, target) {

  return arr;
}
```

# --solutions--

```js
function pairwise(arr, target) {
  let total = 0;

  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] + arr[j] === target) {
        total += i + j;
      }
    }
  }

  return total;
}
```