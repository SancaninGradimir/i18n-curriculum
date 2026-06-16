---
id: 66f1aeb60b11aec5abe83c2e
title: CSS Biblioteke i Frameworkovi Kviz
challengeType: 8
dashedName: quiz-css-libraries-and-frameworks
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 9 od 10 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Šta je CSS framework?
#### --distractors--
Alat za popravljanje CSS grešaka.

---

Alat za lintovanje CSS fajlova.

---

Formatator za CSS fajlove.
#### --answer--
Biblioteka za CSS stilove.
### --question--

#### --text--
Koji od sledećih predstavlja popularan utility-first CSS framework?
#### --distractors--
CSS Šablon

---

Učitavanje CSS-a

---

Minimalni CSS
#### --answer--
Tailwind CSS
### --question--

#### --text--
Koji je nedostatak CSS framework-ova?
#### --distractors--
Previše je komponenti.

---

Nema opcija za prilagođavanje.

---

Poboljšana podrška u pregledačima.
#### --answer--
Može povećati veličinu CSS fajlova.
### --question--

#### --text--
Šta znači SCSS?
#### --distractors--
Super Cascading Style Sheets.

---

Strukturirani CSS.

---

Jednostavan CSS.
#### --answer--
Seksi CSS.
### --question--

#### --text--
Koja od sledećih je karakteristika Sass-a?
#### --distractors--
Komentari

---

CSS linovanje.

---

Inline CSS.
#### --answer--
Miksinovi
### --question--

#### --text--
Koji je ispravan način korišćenja utiliti klasa u Tailwind CSS-u?
#### --distractors--

```html
<button class="color-blue text-color font-size allow-hover round-btn">
  Button
</button>
```

---

```html
<button class="blue text font-size hover round-btn margin-full">
  Button
</button>
```

---


```html
<button class="set-blue set-text set-font set-hover round-btn padding-full">
  Button
</button>
```

#### --answer--


```html
<button class="bg-blue-500 text-white font-bold py-2 px-4 rounded-full hover:bg-blue-700">
  Button
</button>
```

### --question--

#### --text--
Koje su dve vrste CSS framework-a?
#### --distractors--
CSS frameworkovi sa pristupom 'tablet-first' i komponentno bazirani CSS frameworkovi.

---

Utility-first CSS okviri i okviri za CSS sa opterećenjem po potrebi (Lazy loading)

---

Minimalni CSS okvirci i Utility-first CSS okvirci.
#### --answer--
Utility-first CSS frameworkovi i Component-based CSS frameworkovi.
### --question--

#### --text--
Koja je ekstenzija fajla za SCSS?
#### --distractors--

`.sass`

---

`.scsss`

---

`.css`

#### --answer--

`.scss`

### --question--

#### --text--
Koji od sledećih načina je ispravan način za definisanje varijable u SCSS?
#### --distractors--

```css
#primary-color: #3498eb;

header {
  background-color: #primary-color;
}
```

---

```css
>primary-color: #3498eb;

header {
  background-color: >primary-color;
}
```

---

```css
?primary-color: #3498eb;

header {
  background-color: ?primary-color;
}
```

#### --answer--

```css
$primary-color: #3498eb;

header {
  background-color: $primary-color;
}
```

### --question--

#### --text--
Koja od sledećih je ispravna metoda za definisanje miksina?
#### --distractors--

```css
--mixin center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

```css
>mixin center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

```css
mixin center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

#### --answer--

```css
@mixin center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

