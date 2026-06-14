---
id: 672bc4ff5e7a4bbdee8ba013
title: Šta su nazvani colori u CSS-u i kada ih koristiti?
challengeType: 19
dashedName: what-are-named-colors-in-css
---

# --interactive--

U CSS-u, boje igraju ključnu ulogu u dizajnu veb stranica, poboljšanju čitljivosti, postavljanju raspoloženja i unapređenju korisničkog iskustva. Jedan od najjednostavnijih načina za definisanje boja u CSS-u je korišćenje imenovanih boja. Imenovane boje su unapred definisana imena boja koja prepoznaju pregledači. Evo primera korišćenja imenovane boje za paragraf element:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<p>This is a paragraph.</p>
```

```css
p {
  color: red;
}
```

:::

U ovom primeru, koristimo naznačenu boju `red` za stilizovanje teksta u pasusu.

Imenovane boje u CSS-u su kolekcija od 140 standardnih imena boja kao što su `red`, `blue`, `yellow`, `aqua`, `fuchsia`, `black`, i tako dalje. Ova imena su jednostavna za korišćenje i čine vaš kod čitljivijim, a ona su samoodopisiva.

Ime boje je korisno za brzo prototipiranje, jednostavne dizajne i poboljšanje čitljivosti koda. Evo još jednog primera korišćenja imenovanih boja za selektor `h1`:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<h1>This is a heading</h1>
```

```css
h1 {
  color: navy;
  background-color: lightgray;
}
```

:::

U ovom primeru, tekst naslova će biti stilizovan u tamno plavoj boji (navy), sa svetlo sivim pozadinom. Čitljivost koda se poboljšava jer nazvani oblici boja pružaju trenutno vizuelno razumevanje namerene stilizacije.

Imenovane boje u CSS-u su praktične, ali ograničene, sa samo 140 dostupnih opcija. Možda ne nude preciznu nijansu potrebnu za detaljnije dizajne.

Imeovane boje u CSS-u su odličan način za brzo i opisno primenjivanje boja. Iako su korisne za osnovni dizajn, prototipiranje i poboljšanje čitljivosti koda, njihov ograničen opseg čini ih manje pogodnim za složene dizajne koji zahtevaju preciznu kontrolu boja.

Razumevanjem snaga i ograničenja imenovanih boja, možete utvrditi kada je najbolje da ih koristite umesto detaljnijih modela boja kao što su RGB ili HSL, o kojima ćete naučiti u budućim časovima.
# --questions--

## --text--

Šta je ključna prednost korišćenja imenovanih boja u CSS-u?
## --answers--

Boje po imenu vam omogućavaju kreiranje gradijenata.
### --feedback--

Razmislite o jednostavnosti i aspektu čitljivosti imenovanih boja.
---

Named colors are simpler to write and make code more readable.

---

Named colors provide a wider range of color options than hex codes.

### --feedback--

Razmislite o jednostavnosti i aspektu čitljivosti imenovanih boja.
---

Named colors are the most precise way to define colors in web design.

### --feedback--

Razmislite o jednostavnosti i aspektu čitljivosti imenovanih boja.
## --video-solution--

2

## --text--

U kojoj situaciji boje po imenu možda nisu najbolji izbor?
## --answers--

Kada vam treba da brzo prototipujete dizajn.
### --feedback--

Razmislite o ograničenjima imenovanih boja u složenijim dizajnovima.
---

When your design requires very specific or nuanced shades of color.

---

When your design involves only primary colors.

### --feedback--

Razmislite o ograničenjima imenovanih boja u složenijim dizajnovima.
---

When collaborating with others on a simple project.

### --feedback--

Razmislite o ograničenjima imenovanih boja u složenijim dizajnovima.
## --video-solution--

2

## --text--

Koji od sledećih je primer imenovane boje u CSS-u?
## --answers--

`#ff5733`

### --feedback--

Nazivane boje su deskriptivne reči, a ne numerički kodovi.
---

`rgb(255, 99, 71)`

### --feedback--

Nazivane boje su deskriptivne reči, a ne numerički kodovi.
---

`tomato`

---

`hsl(120, 100%, 50%)`

### --feedback--

Nazivane boje su deskriptivne reči, a ne numerički kodovi.
## --video-solution--

3
