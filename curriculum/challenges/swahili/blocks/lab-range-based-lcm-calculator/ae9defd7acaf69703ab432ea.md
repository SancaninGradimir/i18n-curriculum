---
id: ae9defd7acaf69703ab432ea
title: Implementirati kalkulator najmanjeg zajedničkog sadržalnika baziran na opsegu
challengeType: 26
dashedName: implement-a-range-based-lcm-calculator
---

# --description--

U ovom laboratorijumu, kreiraćete funkciju koja prima niz od dve brojeve i vraća najmanji zajednički višekratnik (NZV) tih dva broja i svih brojeva između njih.

**Cilj**: Ispunite priče korisnika ispod i učinite da svi testovi prođu kako biste završili laboratorijum.

**Priče korisnika:**

1. Trebalo bi da imate funkciju `smallestCommons` koja prima niz od dve brojeve kao argument.
1. Funkcija `smallestCommons` treba da vrati najmanji zajednički višekratnik koji je ravnomerno deljiv oba broja i svim uzastopnim brojevima u opsegu između njih.
1. Funkcija treba da obrađuje ulaz gde dva broja nisu u numeričkom redosledu.

# --hints--

You should have a `smallestCommons` function.

```js
assert.isFunction(smallestCommons);
```

`smallestCommons([1, 5])` should return a number.

```js
assert.isNumber(smallestCommons([1, 5]));
```

`smallestCommons([1, 5])` should return `60`.

```js
assert.strictEqual(smallestCommons([1, 5]), 60);
```

`smallestCommons([5, 1])` should return `60`.

```js
assert.strictEqual(smallestCommons([5, 1]), 60);
```

`smallestCommons([2, 10])` should return `2520`.

```js
assert.strictEqual(smallestCommons([2, 10]), 2520);
```

`smallestCommons([1, 13])` should return `360360`.

```js
assert.strictEqual(smallestCommons([1, 13]), 360360);
```

`smallestCommons([23, 18])` should return `6056820`.

```js
assert.strictEqual(smallestCommons([23, 18]), 6056820);
```

# --seed--

## --seed-contents--

```js

```

# --solutions--

```js
function smallestCommons(arr) {
  let [min, max] = arr.sort((a, b) => a - b);

  function gcd(a, b) {
    return b === 0 ? a : gcd(b, a % b);
  }

  function lcm(a, b) {
    return (a * b) / gcd(a, b);
  }

  let multiple = min;

  for (let i = min + 1; i <= max; i++) {
    multiple = lcm(multiple, i);
  }

  return multiple;
}
```
