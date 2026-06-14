---
id: 66cc1deb1f04647f2aabee2b
title: Korak 15
challengeType: 1
dashedName: step-15
---

# --description--

Ako pogledate u konzolu, videćete vrednost `Infinity`. `Infinity` je posebna vrednost u JavaScriptu koja predstavlja broj veći od bilo kog drugog broja.

Deljenje sa nulom nije validna operacija u matematici.

Da biste uzeli u obzir ovaj rubni slučaj, trebalo bi da ažurirate svoju funkciju `calculateQuotient` kako biste umesto toga proverili da li je `num2` nula. 

Ako jeste, funkcija bi trebalo da vrati string `"Error: Division by zero"`. U suprotnom, treba da vrati rezultat deljenja `num1` sa `num2`.

# --hints--

Your `calculateQuotient` function should return the string `"Error: Division by zero"` if `num2` is zero. 

```js
assert.strictEqual(calculateQuotient(10, 0), 'Error: Division by zero');
assert.strictEqual(calculateQuotient(3, 0), 'Error: Division by zero');
```

Your `calculateQuotient` function should return the result of dividing `num1` by `num2` if `num2` is not zero.

```js
assert.strictEqual(calculateQuotient(10, 2), 5);
assert.strictEqual(calculateQuotient(3, 3), 1);
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
--fcc-editable-region--
  return num1 / num2;
--fcc-editable-region--
}

console.log(calculateQuotient(7, 11));
console.log(calculateQuotient(3, 0));
```
