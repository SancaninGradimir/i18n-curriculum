---
id: 672bbec3b86dbdaa07a5a5be
title: Ni mifano gani ya darasa la bandia la kitendakazi?
challengeType: 19
dashedName: what-are-examples-of-functional-pseudo-classes
---

# --interactive--

Darasa la bandia la kitendakazi linakuwezesha kuchagua vipengele kulingana na masharti au uhusiano tata zaidi. Tofauti na darasa la bandia la kawaida ambalo hulenga vipengele kulingana na hali, kwa mfano, `:hover`, `:focus`, darasa la bandia la kitendakazi linakubali hoja ndani ya mabano ya kawaida, ndio maana linaitwa "darasa la bandia la kitendakazi".

Mifano ya darasa la bandia la kitendakazi ni:

- `:is()`
- `:where()`
- `:has()`
- `:not()`

Tuchunguze kwa undani kila moja ya darasa la bandia la kitendakazi kwa mifano.

Darasa la bandia la `:is()` ni muhimu unapotaka kupamba kundi la vipengele vinavyoshiriki baadhi, lakini siyo sifa zote. Kwa mfano, unaweza kutaka kupamba aina tofauti za vitufe kwenye tovuti yako, ikiwa ni pamoja na vipengele vya `button`, viungo vilivyopambwa kama vitufe, na vipengele vya `input` vyenye aina `submit` na `reset`. Hapa kuna mfano unaowakilisha hilo. Bila kitendakazi cha `:is()`, ungehitaji kuandika kichaguzi tata kama hiki:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<button>Example Button</button>
<a href="#" class="button">Link styled like a button</a>
<input type="submit" value="Submit" />
<input type="reset" value="Reset" />
```

```css
button,
a.button,
input[type='submit'],
input[type='reset'] {
  background-color: darkblue;
  color: white;
  border: 1px solid darkblue;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  cursor: pointer;
  display: inline-block;
  margin: 5px;
  font-size: 16px;
  text-align: center;
}

button:hover,
a.button:hover,
input[type='submit']:hover,
input[type='reset']:hover {
  background-color: blue;
  border-color: blue;
}
```

:::

Kwa kutumia kitendakazi cha `:is()`, unaweza kuandika kichaguzi kifupi na kinachoweza kueleweka kama hiki:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<button>Example Button</button>
<a href="#" class="button">Link styled like a button</a>
<input type="submit" value="Submit" />
<input type="reset" value="Reset" />
```

```css
:is(button, a.button, input[type='submit'], input[type='reset']) {
  background-color: darkblue;
  color: white;
  border: 1px solid darkblue;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  cursor: pointer;
  display: inline-block;
  margin: 5px;
  font-size: 16px;
  text-align: center;
}

:is(button, a.button, input[type='submit'], input[type='reset']):hover {
  background-color: blue;
  border-color: blue;
}
```

:::

Darasa la bandia la `:where()` hufanya kazi kama `:is()`, lakini haliongezi umahiri wa kichaguzi chako. Hii inafanya iwe bora kwa kutumia mitindo bila kuathiri umahiri wa sheria nyingine.

Na primer, možete koristiti funkciju `:where()` da ponovo postavite `margin` i `padding` za elemente zaglavlja sekcije. Ovo osigurava da resetovanje ne utiče na specifične stilove koje možete koristiti kasnije. Evo primera toga:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<h1>Page Title</h1>
<h2>Subtitle</h2>
<h3>A point</h3>

<p>Example paragraph.</p>
<p>Example paragraph.</p>
<p>Example paragraph.</p>
```

```css
:where(h1, h2, h3) {
  margin: 0;
  padding: 0;
}
```

:::

Kupamba kipengele cha mzazi kulingana na hali za watoto wake ilikuwa changamoto hapo awali hadi darasa la bandia la `:has()` lilipotambulishwa. Linakuwezesha kutumia mitindo kwa kipengele cha mzazi kulingana na uwepo au hali ya vipengele vya watoto wake.

Kwa mfano, CSS ifuatayo itatumika tu kwa kipengele chochote cha `article` ambacho kina `h2` ndani yake:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<article>
  <h2>Subheading</h2>
  <p>Lorem ipsum dolor sit amet.</p>
</article>

<article>
  <h3>A point</h3>
  <p>Lorem ipsum dolor sit amet.</p>
  <p>Lorem ipsum dolor sit amet.</p>
</article>
```

```css
article:has(h2) {
  border: 2px solid hotpink;
}
```

:::

Darasa la bandia la `:not()` ni bora kwa hali ambapo unataka kutumia mitindo kwa kundi la vipengele, ukiondoa moja au zaidi ya vipengele maalum. Katika CSS ifuatayo, kitufe chochote ambacho si kitufe cha msingi kitakuwa na rangi ya kijivu ya nyuma:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<button class="primary">Primary Button</button>
<button class="secondary">Secondary Button</button>
<button class="danger">Another Secondary Button</button>
```

```css
button {
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
  border: none;
  color: white;
}

button.primary {
  background-color: deepskyblue;
}

button:not(.primary) {
  background-color: grey;
}
```

:::

# --questions--

## --text--

Koji je to lažni kurs koji radi kao `:is()`, ali ne povećava nikakve veštine vaših birača?

## --answers--

`:not()`

### --feedback--

Ovaj veštački stil je dobar za korišćenje širokih, neupadljivih uzoraka.

[No Swahili text provided.]

`:has()`

### --feedback--

Ova veštačka klasa je dobra za korišćenje širokih, neinvazivnih stilova.

[No Swahili text provided.]

`:where()`

[No Swahili text provided.]

`:empty`

### --feedback--

Ova fiktivna klasa je dobra za korišćenje širokih, neinvazivnih stilova.

## --video-solution--

3

## --text--

Zar nijedan od ovih nije lažni profesionalni kurs?

## --answers--

`:is()`

### --feedback--

Pseudo-funkcionalna klasa koristi standardne zagrade i prima argumente unutar nje.

[No Swahili text provided.]

`:first-child`

[No Swahili text provided.]

`:has()`

### --feedback--

Funkcionalna klasa koristi standardne zagrade i prihvata deklaracije unutar sebe.

[No Swahili text provided.]

`:where()`

### --feedback--

Darasa la bandia la kitendakazi hutumia mabano ya kawaida na hukubali hoja ndani yake.

## --video-solution--

2

## --text--

Ni darasa gani la bandia linalofaa kwa hali ambapo unataka kutumia mitindo kwa kundi la vipengele bila moja au mbili kuingizwa?

## --answers--

`:has()`

### --feedback--

Fikiria jinsi unavyoweza kuondoa vipengele maalum kutoka kupambwa.

[No Swahili text provided.]

`:is()`

### --feedback--

Fikiria jinsi unavyoweza kuondoa vipengele maalum kutoka kupambwa.

[No Swahili text provided.]

`:not()`

[No Swahili text provided.]

`:where()`

### --feedback--

Fikiria jinsi unavyoweza kuondoa vipengele maalum kutoka kupambwa.

## --video-solution--

3