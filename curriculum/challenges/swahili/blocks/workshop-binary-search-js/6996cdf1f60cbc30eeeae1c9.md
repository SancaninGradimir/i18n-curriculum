---
id: 6996cdf1f60cbc30eeeae1c9
title: Korak 12
challengeType: 1
dashedName: step-12
---

# --description--

Ako je uslov u `else if` tačan, ažuriraće se vrednost varijable `low` dodavanjem `1` varijabli `mid`.

Ovo će proširiti pretragu na desnu polovinu trenutnih područja pretrage u listi, jer ako je `value` veće od `valueAtMiddle`, to znači da `value` mora biti u desnoj polovini trenutnog područja pretrage.

# --hints--

You should update the `low` variable to `mid + 1`.

```js
assert.match(__helpers.removeJSComments(String(binarySearch)), /low\s*=\s*mid\s*\+\s*1/);
```

# --seed--

## --seed-contents--

```js
function binarySearch(searchList, value) {
  let pathToTarget = [];
  let low = 0;
  let high = searchList.length - 1;
  
  while (low <= high) {
    let mid = Math.floor((low + high) / 2);
    let valueAtMiddle = searchList[mid];
    pathToTarget.push(valueAtMiddle);
    
    if (value === valueAtMiddle) {
      return pathToTarget;
    } else if (value > valueAtMiddle) {
--fcc-editable-region--
      
--fcc-editable-region--     
    }
    break;
  }
  return [];
}

console.log(binarySearch([1, 2, 3, 4, 5], 3));
console.log(binarySearch([1, 2, 3, 4, 5, 9], 4));
```
