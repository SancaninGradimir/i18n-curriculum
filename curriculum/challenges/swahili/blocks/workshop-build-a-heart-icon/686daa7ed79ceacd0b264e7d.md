---
id: 686daa7ed79ceacd0b264e7d
title: Korak 2
challengeType: 0
dashedName: step-2
---

# --description--

Trebalo bi da ugnježđite jedan `path` element unutar vašeg `svg` elementa kako biste dali slici oblik.

Kreirajte `path` element.

# --hints--

You should have a `path` element nested inside of your `svg` element.

```js
const path = document.querySelector('svg path');
assert.exists(path);
```

# --seed--

## --seed-contents--

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Heart Icon</title>
  </head>
  <body>
    <svg>
    --fcc-editable-region--
      
    --fcc-editable-region--
    </svg>
  </body>
</html>
```
