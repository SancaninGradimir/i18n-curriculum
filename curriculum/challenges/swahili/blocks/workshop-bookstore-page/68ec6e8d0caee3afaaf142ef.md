---
id: 68ec6e8d0caee3afaaf142ef
title: Korak 8
challengeType: 0
dashedName: step-8
---

# --description--

Možete dodati više elemenata unutar `div` elementa kako biste grupisali srodan sadržaj. Unutar elementa koji ima `class` sa vrednošću `card-container`, kreirajte još jedan `div` element. Ovaj `div` će predstavljati prvu knjigu karticu.

Dodajte atribut `class` ovom novom `div` elementu i postavite vrednost atributa `class` na `card`.

# --hints--

You should have a `div` element nested inside the element with a class of `card-container`.

```js
assert.exists(document.querySelector('.card-container div'));
```

Your new `div` element should have a `class` attribute.

```js
assert.isTrue(document.querySelector('.card-container div')?.hasAttribute('class'));
```

Your new `div` element should have a `class` having the value of `card`.

```js
assert.exists(document.querySelector('.card-container div.card'));
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>XYZ Bookstore Page</title>
</head>

<body>
  <h1>XYZ Bookstore</h1>
  <p>Browse our collection of amazing books!</p>
  
  <div class="card-container">
--fcc-editable-region--
    
--fcc-editable-region--
  </div>
</body>

</html>
```
