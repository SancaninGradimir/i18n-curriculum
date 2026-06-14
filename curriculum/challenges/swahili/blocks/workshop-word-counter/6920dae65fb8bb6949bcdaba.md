---
id: 6920dae65fb8bb6949bcdaba
title: Korak 4
challengeType: 1
dashedName: step-4
---

# --description--

Da biste videli kako petlja unutar `printCharacters` radi, pozovite je sa argumentom `"hello"`.

# --hints--

You should call the function `printCharacters` with `"hello"` as its argument.

```js
const codeWithoutJSComments = __helpers.removeJSComments(code);
const normalizedCode = __helpers.removeWhiteSpace(codeWithoutJSComments);
assert.match(normalizedCode, /printCharacters\(('|"|`)hello\1\)/);
```

# --seed--

## --seed-contents--

```js
function printCharacters(str) {
  for (const char of str) {
    console.log(char);
  }
}
--fcc-editable-region--

--fcc-editable-region--
```
