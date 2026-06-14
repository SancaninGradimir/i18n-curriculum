---
id: 672bbe9171a5cca90f2edeea
title: Šta su primeri pseudo-klasa za akciju korisnika elementa?
challengeType: 19
dashedName: what-are-examples-of-element-user-action-pseudo-classes
---

# --interactive--

Povratne informacije korisnika su ključni element web dizajna. Na primer, važno je da korisnici primete vizuelne signale kada interaguju sa elementima na veb stranici, kao što je prelazak miša preko dugmeta ili klikatanje na link. Ove povratne informacije pomažu korisnicima da razumeju stanje interaktivnih elemenata, kao što je ukazivanje na to da li je link poseta ili ne.

Pseudo-klase za akciju korisnika u CSS-u su specijalni ključni reči koje vam omogućavaju da pružite ovakvu povratnu informaciju bez potrebe za JavaScript-om ili drugim programskim jezicima.

Ovi pseudo-klase uključuju `:hover`, `:active`, `:focus` i `:visited`, između ostalih. Omogućavaju vam da promenite izgled elemenata na osnovu interakcija korisnika, poboljšavajući ukupno korisničko iskustvo.

Hajde da zaronimo u neke od pseudo-klasa akcije korisnika koje imamo i vidimo kako funkcionišu.

Pseudo-klasa `:active` primjenjuje stilove kada je element aktiviran od strane korisnika. Na primjer, kada korisnik klikne na dugme ili link, pruža trenutnu vizuelnu povratnu informaciju, pokazujući korisnicima da su njihove akcije prepoznate.

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<a href="#">Example link</a>
```

```css
a:active {
  color: crimson;
}
```

:::

Pseudo-klasa ``:hover`` se aktivira kada korisnik pređe mišem ili drugim pokazivačem preko elementa. Razvojari često koriste ovo za kreiranje vizuelne povratne informacije za dugmad, linkove ili bilo koji element koji bi trebalo da reaguje na pažnju korisnika. Evo dugmeta preko koje bi korisnik prešao mišem pre klika:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<button class="btn">Hover Over Me</button>
```

```css
.btn:hover {
  background-color: darkgreen;
  color: white;
  cursor: pointer;
}
```

:::

Pseudo-klasa `:focus` primenjuje stilove kada element dobije fokus, obično putem navigacije tastaturom ili kada korisnik klikne u polje za unos forme. Ovo nije samo za povratne informacije, već je i ključno za pristupačnost. Obezbeđuje da korisnici koji se u velikoj meri oslanjaju na tastature mogu lako identifikovati sa kojim elementom interaguju.

Ovo je primer polja za unos koje dobija fokus kada se klikne ili navigira pomoću tastature:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<form>
  <input type="text" />
</form>
```

```css
input:focus {
  outline: 2px solid darkgreen;
  border-radius: 4px;
}
```

:::

Pseudo-klasa ``:visited`` cilja link koji je korisnik posetio. Ovo može biti korisno za pomoć korisnicima da razlikuju između stranica koje su već posetili i onih koje još uvek nisu posetilke. Evo primera menjanja boje teksta sidra na ciano kada je link posetjen:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<a href="https://www.example.com" target="_blank">Visit Example.com</a>
```

```css
a:visited {
  color: cyan;
}
```

:::

Pseudo-klasa `:checked` u CSS-u omogućava vam da stilizujete elemente forme, kao što su čekboksovi i radijski dugmići, kada su izabrani (čekirani). Ova pseudo-klasa je korisna za prilagođavanje izgleda ovih elemenata kako bi se poboljšalo korisničko iskustvo, iako pretraživači pružaju podrazumevane stilove za njih.

Evo primera sa poljem za čekiranje koje služi za saglasnost s uslovima na veb sajtu.

**NAPOMENA**: Neki od CSS-a u ovom primeru koristi svojstva koja još nisu pokrivena. Ovo je samo da vam dam ideju kako kreirati prilagođeni okvir za čekiranje (checkbox). Naučićete kako sve ovo funkcioniše u budućim časovima i radionicama.

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<form>
  <label>
  Agree <input class="checkbox" type="checkbox" />
  </label>
</form>
```

```css
.checkbox {
  appearance: none;
  width: 18px;
  height: 18px;
  border: 2px solid #ccc;
  border-radius: 4px;
  display: inline-block;
  position: relative;
  cursor: pointer;
  transition: all 0.25s ease;
  vertical-align: middle; 
}

.checkbox:hover {
  border-color: #888;
}

.checkbox:checked {
  background-color: #4caf50;
  border-color: #4caf50;
}

.checkbox:checked::after {
  content: "";
  position: absolute;
  left: 4px;
  top: 0px;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}

.checkbox:focus {
  outline: 2px solid #90caf9;
  outline-offset: 2px;
}

```

:::

U ovom primeru, koristimo `appearance` svojstvo postavljeno na `none` da uklonimo podrazumevano stilizovanje koje pregledač primenjuje na polja za čekiranje. Kada korisnik označi kutijicu, imaće pozadinsku boju od `green`.

Drugi primeri akcionih pseudoklasa su:

- `:focus-within`: za primenu stilova na element kada ima fokus ili bilo koji od njegovih potomaka.
- `:enabled`: za ciljanje dugmadi forme ili drugih elemenata koji su trenutno omogućeni.
- `:disabled`: za ciljanje dugmadi forme ili drugih elemenata koji su onemogućeni.
- `:target`: za primenu stilova na element koji je odredište URL fragmenata (deo URL-a nakon simbola `#`).
# --questions--

## --text--

Šta vam omogućavaju pseudo-klase korisničkih akcija (user action)?
## --answers--

Omogućavaju animacije i tranzicije.
### --feedback--

Razmislite o tome kako možete da interagujete sa korisnicima koristeći isključivo CSS.
---

They allow you to modify the DOM structure dynamically.

### --feedback--

Razmislite o tome kako možete da interagujete sa korisnicima koristeći isključivo CSS.
---

They let you provide feedback to the user without relying on JavaScript.

---

They let you style the last element in a list.

### --feedback--

Razmislite o tome kako možete da interagujete sa korisnicima koristeći isključivo CSS.
## --video-solution--

3

## --text--

Šta radi pseudo-klasa ``:checked`` u CSS-u?
## --answers--

Selektuje element kada je onemogućen.
### --feedback--

Razmislite o tome kako forme obrađuju odabir korisnika.
---

It selects an element when it is being hovered over.

### --feedback--

Razmislite o tome kako forme obrađuju odabir korisnika.
---

It styles elements like checkboxes or radio buttons that are checked.

---

It styles an element when it gains focus.

### --feedback--

Razmislite o tome kako forme obrađuju odabir korisnika.
## --video-solution--

3

## --text--

Šta radi pseudo-klasa ``:focus``?
## --answers--

Selektuje element kada ga miš pređe.
### --feedback--

Razmislite o tome kako korisnici navigiraju po formularima koristeći tastaturu.
---

It applies styles when an element gains focus, usually through keyboard navigation or a click.

---

It selects an element after a form is submitted.

### --feedback--

Razmislite o tome kako korisnici navigiraju po formularima koristeći tastaturu.
---

It applies styles to an element when it is disabled.

### --feedback--

Razmislite o tome kako korisnici navigiraju po formularima koristeći tastaturu.
## --video-solution--

2
