---
id: 672bbe9171a5cca90f2edeea
title: Koje su primere veštačke klase akcije korisnika za karakteristiku/funkciju?
challengeType: 19
dashedName: what-are-examples-of-element-user-action-pseudo-classes
---

# --interactive--

Povratne informacije korisnika su važan element u dizajnu veb stranice. Na primer, važno je da korisnici dobiju vizuelne indikacije kada interaguju sa elementima na veb stranici, kao što je naleti na dugme ili klikatanje na link. Ove povratne informacije pomažu korisnicima da razumeju stanje interaktivnih elemenata, kao što je prikazivanje da li je link kliknut ili ne.

Darasa la bandia za radnji korisnika u CSS su specijalne reči koje mu omogućavaju da pruži ove komentare bez potrebe za JavaScript ili drugim programskim jezicima.

Ove pseudo-klase uključuju `:hover`, `:active`, `:focus`, i `:visited`, među ostalnim. One omogućavaju menjanje izgleda elemenata u zavisnosti od interakcije korisnika, poboljšavajući ukupno korisničko iskustvo.

Neka pregledamo neke veštačke klase korisničkog ponašanja koje imamo i da vidimo kako funkcionišu.

Darasa la bandia la `:active` linaweka mitindo wakati kipengele kinapowashwa na mtumizi. Kwa mfano, mtumizi anapobofya kitufe au kiungo, hutoa maoni ya kuona mara moja, kuonyesha watumizi kuwa vitendo vyao vinatambuliwa.

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

Pseudo-klasa za `:hover` se aktivira kada korisnik pređe mišem ili drugim pokazivačem preko elementa. Razvojari ga često koriste za kreiranje vizuelnog povratnog informacija za dugmiće, link ili bilo koji element koji treba da reaguje na pažnju korisnika. Evo dugmeta preko koje će korisnik preći mišem pre klika:

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

Darasa la bandia la `:focus` linaweka mitindo wakati kipengele kinapopata makini, kawaida kupitia urambazaji wa kibodi au mtumizi anapobofya sehemu ya ingizo ya fomu. Hii si kwa ajili ya maoni tu bali pia ni muhimu kwa Ufikikaji. Inahakikisha watumizi wanaotegemea sana kibodi wanaweza kutambua kwa urahisi kipengele wanachoshirikiana nacho.

Hapa kuna mfano wa sehemu ya ingizo inayopata makini inapobofya au kupelekwa kupitia kibodi:

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

Darasa la bandia la `:visited` linawalenga viungo ambavyo mtumizi amevitembelea. Hii inaweza kusaidia watumizi kutofautisha kati ya kurasa walizotembelea na zile ambazo bado hawajatembelea. Hapa kuna mfano wa kubadilisha rangi ya maandishi ya nanga kuwa cyan wakati kiungo kimebofyanwa:

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

Darasa la bandia la `:checked` katika CSS linakuwezesha kuweka mitindo kwa vipengele vya fomu kama kisanduku cha kuchagua na kitufe cha radio wakati vimechaguliwa (vimekaguliwa). Darasa hili la bandia ni muhimu kwa kubinafsisha muonekano wa vipengele hivi ili kuboresha uzoefu wa mtumizi, ingawa vivinjari hutoa mitindo ya msingi kwao.

Ovo je primer čekmarke za saglasnost sa uslovima na veb stranici.

**NAPOMENA**: Neki od CSS u ovom primeru koriste svojstva koja još nisu data za učenje. Ovo je da vam damo ideju kako kreirati prilagođeni padajući meni (ili okvir za izbor). Naučićete kako sve ovo funkcioniše na budućim časovima i radionicama.

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

U ovom primeru, koristimo atribut `appearance` postavljen na `none` da ukloni osnovni stil koji je dostavljen od strane pretraživača za polja unosa u izbirnoj kutiji. Kada korisnik pregleda kutiju, imaće pozadinsku boju `green`.

Ostali primjeri umjetne klase akcije su:

- `:focus-within`: za postavljanje stilova elementu kada je ili bilo koji od njegovih potomaka fokusiran.
- `:enabled`: za ciljanje dugmadi forme ili drugih elemenata koji su trenutno aktivni.
- `:disabled`: za ciljanje dugmadi forme ili drugih deaktiviranih elemenata.
- `:target`: za postavljanje stilova elementu koji je ciljan delom URL (delom URL nakon oznake `#`).

# --questions--

## --text--

Šta vam veštačka klasa korisničkog ponašanja omogućava?

## --answers--

Omogućava crteže i izmene stila.

### --feedback--

Razmislite kako možete sarađivati sa korisnicima koristeći samo CSS.

[No Swahili text provided.]

Omogućava menjanje strukture DOM u realnom vremenu.

### --feedback--

Razmislite kako možete da sarađujete sa korisnicima koristeći CSS samo.

[No Swahili text provided.]

Dostavlja komentare korisniku bez zavisnosti od JavaScript.

[No Swahili text provided.]

Omogućava vam da postavite stil za poslednji element u listi.

### --feedback--

Razmislite kako možete sarađivati sa korisnicima koristeći samo CSS.

## --video-solution--

3

## --text--

Šta je lažna baza podataka ``:checked`` u `CSS` radi?

## --answers--

Izaberite element kada je onemogućen.

### --feedback--

Razmislite kako forme obrađuju izbor korisnika.

[No Swahili text provided.]

Izaberite element dok ga pregledavate.

### --feedback--

Razmislite kako forme obrađuju izbor korisnika.

[No Swahili text provided.]

Postavlja stilove za elemente kao što su polje za označavanje ili radio dugme koja su odabrana.

[No Swahili text provided.]

Primjenjuje stil za element kada primi fokus.

### --feedback--

Fikiria jinsi fomu zinavyoshughulikia uchaguzi wa mtumizi.

## --video-solution--

3

## --text--

Šta radi lažna klasa `:focus`?

## --answers--

Selektuje element kada ga mišem pređete.

### --feedback--

Zamislite kako korisnici navigiraju po obrascima koristeći tastaturu.

[No Swahili text provided.]

Postavlja se stil kada element dobije fokus, obično putem navigacije tastaturom ili klikom.

[No Swahili text provided.]

Izaberite polje nakon slanja forme.

### --feedback--

Razmislite kako korisnici navigiraju po formularima koristeći tastaturu.

[No Swahili text provided.]

Postavlja stil za element kada se isključuje.

### --feedback--

Razmislite kako korisnici navigiraju po formularima koristeći tastaturu.

## --video-solution--

2