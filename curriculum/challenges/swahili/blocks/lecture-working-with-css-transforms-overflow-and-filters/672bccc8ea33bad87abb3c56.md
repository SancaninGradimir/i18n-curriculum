---
id: 672bccc8ea33bad87abb3c56
title: Šta je razlika između content-box-a i border-box-a?
challengeType: 19
dashedName: what-is-the-difference-between-content-box-and-border-box
---

# --interactive--

Svojstvo `box-sizing` se može postaviti na `content-box` ili `border-box` kako bi se kontrolisalo kako su širina i visina elemenata izračunate.

Ovo svojstvo može se postaviti na univerzalni selektor (`*`) da bi se primenilo na sve elemente u dokumentu:

```css
* {
  box-sizing: border-box;
}
```

Vrednost svojstva ``box-sizing`` je podrazumevano ``content-box``, ali možete izabrati ``border-box`` ako vam zatreba. Prvo ćemo istražiti ``content-box``, a zatim ćemo ući u ``border-box``.

Da biste razumeli kako modeli funkcionišu, morate da budete upoznati sa četiri osnovna koncepta iz CSS kutnog modela. Hajde da ih brzo pregledamo.

- Oblast sadržaja je prostor zauzet sadržajem elementa.
- Padding je prostor između oblasti sadržaja i ivice/granice.
- Ivica je kontura koja okružuje oblast sadržaja i padding.
- Margin je prostor van ivice koji odvaja element od drugih elemenata.

U `content-box` modelu, širina i visina koje postavite za element određuju dimenzije sadržajnog područja, ali ne uključuju padding, granicu ili marginu. Koristite `content-box` kada vam je potrebna precizna kontrola nad sadržajnim područjem. Kada postavite `width` i `height`, postavljate samo veličinu samog sadržaja.

Da biste pronašli ukupnu širinu elementa, moraćete da dodate levu i desnu unutrašnju razmak (padding), kao i leve i desne ivice (borders). Slično tome, ukupna visina elementa može se pronaći dodavanjem visine sadržaja, gornjeg i donjeg unutrašnjeg razmaka (padding), kao i gornjih i donjih ivica (borders).

Na primer, ovde imamo CSS tip selektor za sve `div` elemente.

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css">
<div></div>
```

```css
div {
  width: 300px;
  height: 200px;
  padding: 20px;
  border: 4px solid black;
}
```

:::

U ovom slučaju, ako se koristi `content-box`, oblast sadržaja će biti 300px x 200px. Ukupna prikazana veličina uključuje padding i ivice — na primer, ukupna širina = 300px (sadržaj) + 40px (padding) + 8px (ivice) = 348px; ukupna visina se računa na isti način.

Odlično! Sada ćemo istražiti `border-box`. Razlikuje se jer širina i visina koje postavite uključuju sadržaj elementa, padding i ivicu (ali ne i margine). Koristite `border-box` kada želite da ukupna veličina elementa ostane fiksirana čak i ako se padding ili ivice promene — to je često korisno u responsivnim rasporedima.

Sa `border-box`, padding i granice su uključeni unutar specifikovane veličine elementa. `width` i `height` koje postavite postaju ukupne dimenzije elementa: sadržaj + padding + granica; margine ostaju isključene.

U sledećem primeru, ima dve `div` elementa sa istim dimenzijama, ali različitim vrednostima `box-sizing`. Primećujte kako ovo rezultira različitim ukupnim veličinama kada se pregleda u pretraživaču:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css">
<div class="box" id="red-div"></div>
<div class="box" id="blue-div"></div>
```


```css
.box {
  width: 300px;
  height: 200px;
  padding: 20px;
  border: 4px solid black;
  margin: 10px;
}

#red-div {
  box-sizing: content-box;
  background-color: red;
}

#blue-div {
  box-sizing: border-box;
  background-color: blue;
}
```

:::

Možete videti da oba imaju iste `width`, `height`, `padding`, `border` i `margin`. Jedine razlike su u bojama i vrednosti svojstva `box-sizing` property. Ova mala razlika ima veoma važan uticaj na konačne dimenzije.

Izbor između `content-box` i `border-box` zaista zavisi od specifičnih potreba vašeg projekta. Iako `border-box` postaje sve popularniji zbog svoje jednostavnosti i fleksibilnosti, razumevanje oba modela važno je za implementaciju efikasnih CSS rasporeda.
# --questions--

## --text--

Koja od sledećih je podrazumevana vrednost za svojstvo `box-sizing` u većini pregledača?
## --answers--

`content-box`

---

`border-box`

### --feedback--

Razmislite o podrazumevanom ponašanju za određivanje veličine elemenata.
---

`padding-box`

### --feedback--

Razmislite o podrazumevanom ponašanju za određivanje veličine elemenata.
---

`margin-box`

### --feedback--

Razmislite o podrazumevanom ponašanju za određivanje veličine elemenata.
## --video-solution--

1

## --text--

Koja je glavna prednost korišćenjem `border-box` za kreiranje responsivnih rasporeda?
## --answers--

To čini proračune komplikovanijim.
### --feedback--

Razmislite o tome kako model `border-box` obrađuje `padding` i `border` unutar navedenih `width` i `height`.
---

It allows for more precise control over element dimensions.

### --feedback--

Razmislite o tome kako model `border-box` obrađuje `padding` i `border` unutar navedenih `width` i `height`.
---

It ensures that elements maintain their specified dimensions regardless of changes in `padding` or `border`.

---

It improves browser compatibility.

### --feedback--

Razmislite o tome kako model `border-box` obrađuje `padding` i `border` unutar navedenih `width` i `height`.
## --video-solution--

3

## --text--

U modelu `content-box`, šta predstavlja navedeno `width` od elementa?
## --answers--

Ukupna `width` vrednost elementa, uključujući `padding`, `border` i `margin`.
### --feedback--

Razmislite o odnosu između područja sadržaja i ukupnih dimenzija elementa u modelu `content-box`.
---

The `width` of the content area only.

---

The `width` of the `border`.

### --feedback--

Razmislite o odnosu između područja sadržaja i ukupnih dimenzija elementa u modelu `content-box`.
---

The `width` of the `padding`.

### --feedback--

Razmislite o odnosu između područja sadržaja i ukupnih dimenzija elementa u modelu `content-box`.
## --video-solution--

2
