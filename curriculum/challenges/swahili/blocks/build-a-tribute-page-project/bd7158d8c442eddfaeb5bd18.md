---
id: bd7158d8c442eddfaeb5bd18
title: Napravi stranicu posvete
challengeType: 14
saveSubmissionToDB: true
forumTopicId: 301147
dashedName: build-a-tribute-page
---

# --description--

**Cilj:** Napravi aplikaciju koja je funkcionalno slična <a href="https://tribute-page.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://tribute-page.freecodecamp.rocks</a>. **Ne kopiraj ovaj demonstracioni projekat**.

**Korisničke priče:**

1. Tvoja stranica posvete treba da ima element `main` sa odgovarajućim `id`-jem `main`, koji sadrži sve ostale elemente
1. Treba da vidiš element sa `id`-jem `title`, koji sadrži niz karaktera (odnosno tekst) koji opisuje temu stranice posvete (na primer "Dr. Norman Borlaug")
1. Treba da vidiš element `figure` ili `div` sa `id`-jem `img-div`
1. Unutar elementa `#img-div`, treba da vidiš element `img` sa odgovarajućim `id="image"`
1. Unutar elementa `#img-div`, treba da vidiš element sa odgovarajućim `id="img-caption"` koji sadrži tekstualni opis slike prikazane u `#img-div`
1. Treba da vidiš element sa odgovarajućim `id="tribute-info"`, koji sadrži tekstualni opis teme stranice posvete
1. Treba da vidiš element `a` sa odgovarajućim `id="tribute-link"`, koji vodi ka spoljašnjem sajtu sa dodatnim informacijama o temi stranice posvete. NAPOMENA: Moraš da dodeliš svom elementu atribut `target` i postaviš ga na `_blank` kako bi se tvoj link otvarao u novom tabu
1. Tvoj `#image` treba da koristi svojstva `max-width` i `height` tako da menja veličinu prema širini roditeljskog elementa, ali bez prekoračenja svoje originalne veličine
1. Tvoj element `img` treba da bude centriran unutar roditeljskog elementa

Ispuni korisničke priče i prođi sve testove ispod da bi završio ovaj projekat. Dodaj svoj lični stil. Uživaj u kodiranju!

**Napomena:** Obavezno dodaj `<link rel="stylesheet" href="styles.css">` u svoj HTML kako bi povezao svoju datoteku stilova i primenio svoj CSS

# --hints--

Treba da imaš element `main` sa `id`-jem `main`.

```js
const el = document.getElementById('main');
assert.isNotNull(el);
assert.strictEqual(el.tagName, 'MAIN');
```

Tvoji `#img-div`, `#image`, `#img-caption`, `#tribute-info` i `#tribute-link` svi treba da budu potomci elementa `#main`.

```js
const el1 = document.querySelector('#main #img-div');
const el2 = document.querySelector('#main #image');
const el3 = document.querySelector('#main #img-caption');
const el4 = document.querySelector('#main #tribute-info');
const el5 = document.querySelector('#main #tribute-link');
assert.isNotNull(el1);
assert.isNotNull(el2);
assert.isNotNull(el3);
assert.isNotNull(el4);
assert.isNotNull(el5);
```

Treba da imaš element sa `id`-jem `title`.

```js
const el = document.getElementById('title');
assert.isNotNull(el);
```

Tvoj `#title` ne sme biti prazan.

```js
const el = document.getElementById('title');
assert.isNotNull(el);
assert.isNotEmpty(el.innerText.trim());
```

Treba da imaš element `figure` ili `div` sa `id`-jem `img-div`.

```js
const el = document.getElementById('img-div');
assert.isNotNull(el);
assert.isTrue(el.tagName === 'DIV' || el.tagName === 'FIGURE');
```

Treba da imaš element `img` sa `id`-jem `image`.

```js
const el = document.getElementById('image');
assert.isNotNull(el);
assert.strictEqual(el.tagName, 'IMG');
```

Tvoj `#image` treba da bude potomak elementa `#img-div`.

```js
const el = document.querySelector('#img-div #image');
assert.isNotNull(el);
```

Treba da imaš element `figcaption` ili `div` sa `id`-jem `img-caption`.

```js
const el = document.getElementById('img-caption');
assert.isNotNull(el);
assert.isTrue(el.tagName === 'DIV' || el.tagName === 'FIGCAPTION');
```

Tvoj `#img-caption` treba da bude potomak elementa `#img-div`.

```js
const el = document.querySelector('#img-div #img-caption');
assert.isNotNull(el);
```

Tvoj `#img-caption` ne sme biti prazan.

```js
const el = document.getElementById('img-caption');
assert.isNotNull(el);
assert.isNotEmpty(el.innerText);
```

Treba da imaš element sa `id`-jem `tribute-info`.

```js
const el = document.getElementById('tribute-info');
assert.isNotNull(el);
```

Tvoj `#tribute-info` ne sme biti prazan.

```js
const el = document.getElementById('tribute-info');
assert.isNotNull(el);
assert.isNotEmpty(el.innerText);
```

Treba da imaš element `a` sa `id`-jem `tribute-link`.

```js
const el = document.getElementById('tribute-link');
assert.isNotNull(el);
assert.strictEqual(el.tagName, 'A');
```

Tvoj `#tribute-link` treba da ima atribut `href` i njegovu vrednost.

```js
const el = document.getElementById('tribute-link');
assert.isNotNull(el);
assert.isNotNull(el.href);
assert.isNotEmpty(el.href);
```

Tvoj `#tribute-link` treba da ima atribut `target` postavljen na `_blank`.

```js
const el = document.getElementById('tribute-link');
assert.isNotNull(el);
assert.strictEqual(el.target, '_blank');
```

Tvoj element `img` treba da ima `display` vrednost `block`.

```js
const img = document.getElementById('image');
const imgStyle = window.getComputedStyle(img);
const style = imgStyle?.getPropertyValue('display');
assert.strictEqual(style, 'block');
```

Tvoj `#image` treba da ima `max-width` od `100%`.

```js
const img = document.getElementById('image');
const imgStyle = window.getComputedStyle(img);
const style = imgStyle?.getPropertyValue('max-width');
assert.strictEqual(style, '100%');
```

Tvoj `#image` treba da ima `height` vrednost `auto`.

```js
// taken from the testable-projects repo
const img = document.getElementById('image');
const imgStyle = window.getComputedStyle(img);
const oldDisplayValue = imgStyle.getPropertyValue('display');
const oldDisplayPriority = imgStyle.getPropertyPriority('display');
img?.style.setProperty('display', 'none', 'important');
const heightValue = imgStyle?.getPropertyValue('height');
img?.style.setProperty('display', oldDisplayValue, oldDisplayPriority);
assert.strictEqual(heightValue, 'auto');
```

Tvoj `#image` treba da bude centriran unutar svog roditelja.

```js
// taken from the testable-projects repo
const img = document.getElementById('image'),
  imgParent = img?.parentElement,
  imgLeft = img?.getBoundingClientRect().left,
  imgRight = img?.getBoundingClientRect().right,
  parentLeft = imgParent?.getBoundingClientRect().left,
  parentRight = imgParent?.getBoundingClientRect().right,
  leftMargin = imgLeft - parentLeft,
  rightMargin = parentRight - imgRight;
assert.isBelow(leftMargin - rightMargin, 6);
assert.isBelow(rightMargin - leftMargin, 6);
```

# --seed--

## --seed-contents--

```html

```

```css

```

# --solutions--

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link
      href="https://fonts.googleapis.com/css?family=Pacifico"
      rel="stylesheet"
    />
    <link
      href="https://fonts.googleapis.com/css?family=Lobster"
      rel="stylesheet"
    />
    <link href="styles.css" rel="stylesheet" />
    <title>Tribute Page</title>
  </head>
  <body>
    <h1>Tribute Page</h1>
    <p>The below card was designed as a tribute page for freeCodeCamp.</p>
    <main id="main">
      <div id="img-div">
        <img
          id="image"
          class="border"
          src="https://upload.wikimedia.org/wikipedia/en/5/53/Pok%C3%A9mon_Togepi_art.png"
          alt="An image of Togepi"
        />
        <figcaption id="img-caption">Togepi, happy as always.</figcaption>
      </div>
      <h2 id="title">Togepi</h2>
      <hr />
      <div id="tribute-info">
        <p>
          Togepi was first discovered in the Johto region, when Ash Ketchum
          discovered a mysterious egg. However, when the egg hatched, Togepi saw
          Ash's friend Misty first and imprinted on her. Like many other
          creatures, this imprinting process created a bond and Togepi views
          Misty as his mother.
        </p>
        <p>
          Togepi is a very childlike Pokemon, and is very emotionally
          expressive. He demonstrates extreme levels of joy and sadness.
        </p>
        <hr />
        <p><u>Battle Information</u></p>
        <ul style="list-style-type: none">
          <li>Type: Fairy</li>
          <li>Evolutions: Togepi -> Togetic -> Togekiss</li>
          <li>Moves: Growl, Pound, Sweet Kiss, Charm</li>
          <li>Weaknesses: Poison, Steel</li>
          <li>Resistances: Dragon</li>
        </ul>
        <p>
          Check out this
          <a
            id="tribute-link"
            href="https://bulbapedia.bulbagarden.net/wiki/Togepi_(Pok%C3%A9mon)"
            target="_blank"
            rel="noopener noreferrer"
            >Bulbapedia article on Togepi</a
          >
          for more information on this great Pokemon.
        </p>
      </div>
    </main>
  </body>
  <footer>
    <a href="../">Return to Project List</a> |
    <a href="https://www.nhcarrigan.com">Return to HomePage</a>
  </footer>
</html>
```

```css
body {
  background-color: #3a3240;
  color: white;
}
main {
  background-color: #92869c;
  font-family: Lobster;
  max-width: 500px;
  margin: 20px auto;
  color: black;
  border-radius: 50px;
  box-shadow: 10px 10px rgba(0, 0, 0, 0.5);
}
h2 {
  text-align: center;
  font-size: 20pt;
  font-family: Pacifico;
}
body {
  text-align: center;
  font-size: 12pt;
}
footer {
  text-align: center;
  font-size: 10pt;
}
.border {
  border-color: black;
  border-width: 5px;
  border-style: solid;
}
#image {
  height: auto;
  display: block;
  margin: auto;
  max-width: 100%;
  border-radius: 50%;
}
#img-caption {
  font-size: 10pt;
}
a:not(#tribute-link) {
  color: white;
}
hr {
  border-color: black;
}
```
