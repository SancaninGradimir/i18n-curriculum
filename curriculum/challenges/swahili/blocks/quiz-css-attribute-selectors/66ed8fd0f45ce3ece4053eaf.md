---
id: 66ed8fd0f45ce3ece4053eaf
title: CSS Attribute Selectors Quiz
challengeType: 8
dashedName: quiz-css-attribute-selectors
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 9 od 10 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Za šta se koriste CSS atributni selektori?
#### --distractors--
Kako primeniti stilove na elemente na osnovu njihovog imena taga.

---

Kako primeniti stilove na elemente na osnovu njihovog imena klase.

---

Za primenu stilova na elemente na osnovu njihovog roditeljskog elementa.
#### --answer--
Kako primeniti stilove na elemente bazirano na njihovim atributima.
### --question--

#### --text--
Koji od sledećih neće biti selektovan ovim CSS selector-om?

```css
[title~="flower"] {
  border: 5px solid yellow;
}
```

#### --distractors--

```html
<img src="img1.jpg" title="clematis flower" width="150" height="113">
```

---

```html
<img src="img2.jpg" title="flower" width="150" height="113">
```

---

```html
<img src="img2.jpg" title="FLOWERS of flower" width="150" height="113">
```

#### --answer--

```html
<img src="img2.jpg" title="flowers" width="150" height="113">
```

### --question--

#### --text--
Koji CSS selektor odgovara svim elementima `p` sa atributom `lang` postavljenim na `"fr"`?
#### --distractors--

```css
p[lang-="fr"] { color: blue; }
```

---

```css
p[lang~="fr"] { color: blue; }
```

---

```css
p[lang=="fr"] { color: blue; }
```

#### --answer--

```css
p[lang="fr"] { color: blue; }
```

### --question--

#### --text--
Koji CSS selektor odgovara svim elementima ``a`` koji imaju atribut ``href``?
#### --distractors--

```css
a(href) { color: green; }
```

---

```css
a { color: green; }
```

---

```css
a[href~=""] { color: green; }
```

#### --answer--

```css
a[href] { color: blue; }
```

### --question--

#### --text--
Koji CSS selektor odgovara svim numerisanim listama sa velikim rimskim brojevima?
#### --distractors--

```css
ol[type="a"] { border-color: black; }
```

---

```css
ol[type="A"] { border-color: black; }
```

---

```css
ol[type="i"] { border-color: black; }
```

#### --answer--

```css
ol[type="I"] { border-color: black; }
```

### --question--

#### --text--
Za šta se atribut `data-lang` obično koristi?
#### --distractors--
Za određivanje jezika dokumenta.

---

Definisanje enkodiranja karaktera dokumenta.

---

Postavljanje jezika elementa na osnovu njegovog roditeljskog elementa.
#### --answer--
Za skladištenje prilagođenih podataka na HTML elementu koje mogu koristiti ni CSS ni JavaScript.
### --question--

#### --text--
Koji CSS selektor bi trebalo da koristite da stilizujete elemente `img` samo ako je njihov atribut `alt` jednak vrednosti `"code"`?
#### --distractors--

```css
img[alt~="code"] { border: 1px solid red; }
```

---

```css
img[alt=="code"] { border: 1px solid red; }
```

---

```css
img[alt*="code"] { border: 1px solid red; }
```

#### --answer--

```css
img[alt="code"] { border: 1px solid red; }
```

### --question--

#### --text--
Koji CSS selektor odgovara numerisanim listama sa tipom brojanja po rednom broju?
#### --distractors--

```css
ol[type="i"] { color: purple; }
```

---

```css
ol[type="I"] { color: purple; }
```

---

```css
ol[type="a"] { color: purple; }
```

#### --answer--

```css
ol[type="1"] { color: purple; }
```

### --question--

#### --text--
Koji od sledećih CSS selektora bi ste koristili za stilizovanje elemenata `a` sa atributima i `href` i `title`?
#### --distractors--

```css
a[href] a[title] { text-decoration: underline dotted; }
```

---

```css
a[href]a[title] { text-decoration: underline dotted; }
```

---

```css
a[href].[title] { text-decoration: underline dotted; }
```

#### --answer--

```css
a[href][title] { text-decoration: underline dotted; }
```

### --question--

#### --text--
Koji CSS selektor biste koristili ako razvijate veb-sajt za restoran i želite stilizovati sve elemente sa klasom `menu-item` koji imaju atribut `data-special`?
#### --distractors--

```css
menu-item[data-special] { background-color: blue; }
```

---

```css
#menu-item[data-special] { background-color: blue; }
```

---

```css
[data-special="menu-item"] { background-color: blue; }
```

#### --answer--

```css
.menu-item[data-special] { background-color: blue; }
```

