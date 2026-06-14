---
id: 66cc1ccfefdd727e18c2ab20
title: Korak 14
challengeType: 1
dashedName: step-14
---

# --description--

Vaš `calculateQuotient` izgleda da radi ispravno, ali postoji jedan slučaj koji niste još testirali.

Dodajte `console.log` koji poziva funkciju `calculateQuotient` sa argumentima `3` i `0`.

Obavezno pogledajte izlaz ovog poziva.

# --hints--

You should have a `console.log` that calls the `calculateQuotient` function with the arguments `3` and `0`.

```js
assert.match(code, /console\.log\s*\(\s*calculateQuotient\s*\(\s*3\s*,\s*0\s*\)\s*\)\s*;?/);
```

# --seed--

## --seed-contents--

```js
function calculateSum(num1, num2) {
  return num1 + num2;
}

console.log(calculateSum(2, 5));
console.log(calculateSum(10, 10));
console.log(calculateSum(5, 5));

function calculateDifference(num1, num2) {
  return num1 - num2;
}

console.log(calculateDifference(22, 5));
console.log(calculateDifference(12, 1));
console.log(calculateDifference(17, 9));

function calculateProduct(num1, num2) {
  return num1 * num2;
}

console.log(calculateProduct(13, 5));

function calculateQuotient(num1, num2) {
  return num1 / num2;
}

console.log(calculateQuotient(7, 11));
--fcc-editable-region--

--fcc-editable-region--
```
