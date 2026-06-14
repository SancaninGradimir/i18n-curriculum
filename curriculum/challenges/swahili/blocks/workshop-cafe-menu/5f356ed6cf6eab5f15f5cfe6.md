---
id: 5f356ed6cf6eab5f15f5cfe6
title: Korak 16
challengeType: 0
dashedName: step-16
---

# --description--

Element `div` se koristi uglavnom za svrhe dizajnerskog rasporeda, za razliku od drugih elemenata sadržaja koje ste do sada koristili. Dodajte element `div` unutar elementa `body`, a zatim premestite sve ostale elemente unutar novog `div`.

Unutar otvarajućeg taga `div`, dodajte atribut `id` sa vrednošću `menu`.

# --hints--

Your opening `<div>` tag should have an `id` attribute set to `menu`.

```js
assert.strictEqual(document.querySelector('div')?.id, 'menu');
```

You should have a closing `</div>` tag.

```js
assert.match(code, /<\/div>/i);
```

You should not change your existing `body` element. Make sure you did not delete the closing tag.

```js
assert.lengthOf(document.querySelectorAll('body'), 1);
```

Your `div` element should be nested in the `body`.

```js
assert.equal(document.querySelector('div')?.parentElement?.tagName, 'BODY');
```

You should move all the other elements inside the new `div`.

```js
assert.lengthOf(document.querySelector('body > div#menu > main')?.children, 3);
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Cafe Menu</title>
    <link href="styles.css" rel="stylesheet"/>
  </head>
  <body>
--fcc-editable-region--
    <main>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
      <section>
        <h2>Coffee</h2>
      </section>
    </main>
--fcc-editable-region--
  </body>
</html>
```

```css
body {
  background-color: burlywood;
}

h1, h2, p {
  text-align: center;
}
```
