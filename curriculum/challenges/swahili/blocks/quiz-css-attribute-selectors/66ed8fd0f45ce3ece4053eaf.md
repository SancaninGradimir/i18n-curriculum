---
id: 66ed8fd0f45ce3ece4053eaf
title: Kratak test selektora svojstava elemenata CSS
challengeType: 8
dashedName: quiz-css-attribute-selectors
---

# --description--

Da bi prošao kratki test, moraš tačno odgovoriti na najmanje 9 od 10 pitanja koja su navedena ispod.

# --quizzes--

## --quiz--

### --question--

#### --text--

Selektori svojstava elementa za CSS, za šta se koriste?

#### --distractors--

Postavljanje stilova za elemente u zavisnosti od imena njihove etikete.

[No Swahili text provided.]

Postavljanje stilova elemenata na osnovu naziva klase predmeta.

[No Swahili text provided.]

Postavljanje stilova za elemente u odnosu na njihov roditeljski element.

#### --answer--

Postavljanje stilova elemenata na osnovu njihovih svojstava.

### --question--

#### --text--

Koji/Koja je među sljedećim koji nije izabran ovim selektorom CSS?

```css
[title~="flower"] {
  border: 5px solid yellow;
}
```

#### --distractors--

```html
<img src="img1.jpg" title="clematis flower" width="150" height="113">
```

[No Swahili text provided.]

```html
<img src="img2.jpg" title="flower" width="150" height="113">
```

[No Swahili text provided.]

```html
<img src="img2.jpg" title="FLOWERS of flower" width="150" height="113">
```

#### --answer--

```html
<img src="img2.jpg" title="flowers" width="150" height="113">
```

### --question--

#### --text--

Koji je selektor za CSS koji odgovara svim elementima `p` sa atributom `lang` postavljenim na `"fr"`?

#### --distractors--

```css
p[lang-="fr"] { color: blue; }
```

[No Swahili text provided.]

```css
p[lang~="fr"] { color: blue; }
```

[No Swahili text provided.]

```css
p[lang=="fr"] { color: blue; }
```

#### --answer--

```css
p[lang="fr"] { color: blue; }
```

### --question--

#### --text--

Koji selektor za CSS odgovara svim elementima od `a` koji imaju atribut `href`?

#### --distractors--

```css
a(href) { color: green; }
```

[No Swahili text provided.]

```css
a { color: green; }
```

[No Swahili text provided.]

```css
a[href~=""] { color: green; }
```

#### --answer--

```css
a[href] { color: blue; }
```

### --question--

#### --text--

Koji selektor CSS odgovara strukturiranim listama sa velikim rimskim brojevima?

#### --distractors--

```css
ol[type="a"] { border-color: black; }
```

[No Swahili text provided.]

```css
ol[type="A"] { border-color: black; }
```

[No Swahili text provided.]

```css
ol[type="i"] { border-color: black; }
```

#### --answer--

```css
ol[type="I"] { border-color: black; }
```

### --question--

#### --text--

Za šta se svojstvo `data-lang` obično koristi?

#### --distractors--

Identifikujte jezik dokumenta.

[No Swahili text provided.]

Definisanje kodovanja karaktera dokumenta.

[No Swahili text provided.]

Postavljanje jezika elementa u skladu sa njegovim roditeljskim elementom.

#### --answer--

Sačuvajte specifične podatke u komponentu HTML koju mogu koristiti CSS ili JavaScript.

### --question--

#### --text--

Koji selektor za CSS treba da koristiš za postavljanje stila za elemente sa `img`, samo ako je njihov atribut `alt` jednak `"code"`?

#### --distractors--

```css
img[alt~="code"] { border: 1px solid red; }
```

[No Swahili text provided.]

```css
img[alt=="code"] { border: 1px solid red; }
```

[No Swahili text provided.]

```css
img[alt*="code"] { border: 1px solid red; }
```

#### --answer--

```css
img[alt="code"] { border: 1px solid red; }
```

### --question--

#### --text--

Koji je selektor za CSS koji odgovara strukturiranim listama sa tipom digitalnih brojeva?

#### --distractors--

```css
ol[type="i"] { color: purple; }
```

[No Swahili text provided.]

```css
ol[type="I"] { color: purple; }
```

[No Swahili text provided.]

```css
ol[type="a"] { color: purple; }
```

#### --answer--

```css
ol[type="1"] { color: purple; }
```

### --question--

#### --text--

Koji od sledećih selektora za CSS biste koristili da postavite stil za elemente `a` koji imaju oba svojstva `href` i `title`?

#### --distractors--

```css
a[href] a[title] { text-decoration: underline dotted; }
```

[No Swahili text provided.]

```css
a[href]a[title] { text-decoration: underline dotted; }
```

[No Swahili text provided.]

```css
a[href].[title] { text-decoration: underline dotted; }
```

#### --answer--

```css
a[href][title] { text-decoration: underline dotted; }
```

### --question--

#### --text--

Koji selektor za CSS bi koristio ako praviš web-stranicu za restoran i želiš primeniti stil na sve elemente koji imaju klasu stvari `menu-item` a koji imaju atribut `data-special`?

#### --distractors--

```css
menu-item[data-special] { background-color: blue; }
```

[No Swahili text provided.]

```css
#menu-item[data-special] { background-color: blue; }
```

[No Swahili text provided.]

```css
[data-special="menu-item"] { background-color: blue; }
```

#### --answer--

```css
.menu-item[data-special] { background-color: blue; }
```
