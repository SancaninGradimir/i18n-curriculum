---
id: 672bccc8ea33bad87abb3c56
title: Šta je razlika između `content-box` i `border-box`?
challengeType: 19
dashedName: what-is-the-difference-between-content-box-and-border-box
---

# --interactive--

Svojstvo `box-sizing` može se postaviti na `content-box` ili `border-box` za kontrolisanje kako širina i visina merenih elemenata.

Ovo svojstvo se može postaviti na globalni selektor (`*`) da bi važio za sve elemente u dokumentu:

```css
* {
  box-sizing: border-box;
}
```

Vrednost svojstva `box-sizing` je `content-box` podrazumevano, ali možete odabrati `border-box` ako je potrebno. Proverićemo `content-box` prvo, a zatim ćemo ući na/u `border-box`.

Da biste razumeli kako modeli funkcionišu, morate shvatiti četiri glavna koncepta iz primjera kutije CSS. Hajde da brzo pregledamo.

- Eneo la maudhui ni nafasi inayochukuliwa na maudhui ya kipengele.
- Nafasi ya ndani ni nafasi kati ya eneo la maudhui na mpaka.
- Mpaka ni mstari unaozunguka eneo la maudhui na nafasi ya ndani.
- Ukingo ni nafasi nje ya mpaka inayotenganisha kipengele na vipengele vingine.

Katika mfano wa `content-box`, upana na urefu unaoweka kwa kipengele huamua vipimo vya eneo la maudhui, lakini havijumuishi nafasi ya ndani, mpaka, au ukingo. Tumia `content-box` unapohitaji udhibiti sahihi wa eneo la maudhui. Unapoweka `width` na `height`, unakuwa umeweka ukubwa wa maudhui yenyewe tu.

Da biste dobili ukupnu širinu elementa, morate dodati unutrašnji padding sa leve i desne strane, kao i levu i desnu granicu. Slično tome, ukupna visina elementa može se dobiti sabiranjem visine sadržaja, gornjeg i donjeg unutrašnjeg padding-a, i gornje i donje granice.

Kwa mfano, hapa tuna kichaguzi cha aina ya CSS kwa vipengele vyote vya `div`.

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

Katika kesi hii, ikiwa `content-box` itatumika eneo la maudhui litakuwa 300px kwa 200px. Ukubwa wa jumla unaonyeshwa unajumuisha nafasi ya ndani na mipaka — kwa mfano, upana wa jumla = 300px (maudhui) + 40px (nafasi ya ndani) + 8px (mipaka) = 348px; urefu wa jumla unahesabiwa kwa njia ile ile.

Nzuri! Sasa hebu tuchunguze `border-box`. Ni tofauti kwa sababu upana na urefu unaoweka unajumuisha maudhui ya kipengele, nafasi ya ndani, na mpaka (lakini si ukingo wake). Tumia `border-box` unapotaka ukubwa wa jumla wa kipengele ubaki thabiti hata kama nafasi ya ndani au mipaka itabadilika — hii mara nyingi husaidia katika mipangilio inayojibadilisha kulingana na kifaa.

Za `border-box`, unutrašnji razmak i granice uključeni su u definisanu veličinu elementa. `width` i `height` postavljaju se kao ukupne dimenzije elementa: sadržaj + unutrašnji razmak + granica; ivice nisu uključene.

U sledećem primeru, postoje dva elementa sa `div` koji imaju iste dimenzije, ali različite vrednosti za `box-sizing`. Pogledajte kako ovo uzrokuje različitu ukupnu veličinu kada se gleda u pretraživaču:

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

Možete videti da sve imaju `width`, `height`, `padding`, `border` na `margin` jednako. Jedina razlika je u boji i vrednosti svojstva `box-sizing`. Ova mala razlika ima veoma značajan uticaj na konačne mere.

Izaberite između `content-box` i `border-box` u zavisnosti od specifičnih zahteva vašeg projekta. Iako je `border-box` izuzetno popularan zbog svoje jednostavne upotrebe i fleksibilnosti, razumevanje oba primera ključno je za implementaciju robustnih podešavanja CSS.

# --questions--

## --text--

Koja od sledećih je podrazumevana vrednost svojstva `box-sizing` u mnogim pregledačima?

## --answers--

`content-box`

---

`border-box`

### --feedback--

Razmotrite podrazumevano ponašanje za veličinu elemenata.

---

`padding-box`

### --feedback--

Razmislite o podrazumevanom ponašanju za veličinu elemenata.

---

`margin-box`

### --feedback--

Fikiria tabia ya chaguo-msingi kwa ukubwa wa vipengele.

## --video-solution--

1

## --text--

Koja je glavna korist korišćenja `border-box` za kreiranje podešavanja koja se menjaju u zavisnosti od uređaja?

## --answers--

Otežava proračune.

### --feedback--

Razmislite kako model `border-box` obrađuje `padding` i `border` unutar `width` i `height` definisanih.

---

Omogućava precizniju kontrolu parametara elementa.

### --feedback--

Razmislite kako primer `border-box` obrađuje `padding` i `border` unutar `width` i `height`.

---

Osigurava da komponente održavaju navedene specifikacije bez obzira na promene u `padding` ili `border`.

---

Poboljšava sinhronizaciju pretraživača.

### --feedback--

Razmislite kako primer `border-box` obrađuje `padding` i `border` unutar `width` i `height`, definisanih.

## --video-solution--

3

## --text--

U primeru `content-box`, `width`, šta predstavlja definisani element?

## --answers--

Ukupna veličina `width` elementa, uključujući `padding`, `border` i `margin`.

### --feedback--

Razmotrite odnos između područja sadržaja i ukupnih dimenzija elementa u primeru `content-box`.

---

Ukubwa wa `width` wa eneo la maudhui tu.

---

Veličina `width` od `border`.

### --feedback--

Razmislite o odnosu između područja sadržaja i ukupnih dimenzija elementa u primeru `content-box`.

---

Veličina `width` od `padding`.

### --feedback--

Razmotrite odnos između oblasti sadržaja i ukupnih dimenzija elementa u primeru od `content-box`.

## --video-solution--

2