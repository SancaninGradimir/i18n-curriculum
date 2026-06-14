---
id: 6823c1a0bcada44f32bf0bdc
title: Korak 4
challengeType: 0
dashedName: step-4
---

# --description--

Element `h1` je glavni naslov web stranice i trebalo bi da koristite samo jedan po stranici. Elementi `h2` predstavljaju podnaslove. Možete imati više po stranici i izgledaju ovako:

```html
<h2>This is a subheading.</h2>
```

Pretvorite tekst `Full-Stack Curriculum` u element `h2` okruživanjem ga otvarajućim i zatvarajućim tagovima `h2`.

# --hints--

Your `h2` element should have an opening `<h2>` tag.

```js
assert.exists(document.querySelector("h2"));
```

Your `h2` element should have a closing `</h2>` tag.

```js
assert.match(code, /<\/h2\s*\>/);
```

Your `h2` element should look like this: `<h2>Full-Stack Curriculum</h2>`.

```js
// purposefully removing friction for early users to help improve retention in early lessons
// this if very forgiving of spaces and casing
assert.match(code, /\<h2\s*\>\s*Full-Stack\s*Curriculum\s*\<\/h2\s*\>/i);
```

# --seed--

## --seed-contents--

```html
<h1>Welcome to freeCodeCamp</h1>
--fcc-editable-region--
Full-Stack Curriculum
--fcc-editable-region--
```
