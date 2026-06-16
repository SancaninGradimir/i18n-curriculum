---
id: 66ed8fc1f45ce3ece4053ead
title: CSS Pristupačnost Test
challengeType: 8
dashedName: quiz-css-accessibility
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 9 od 10 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Zašto je potrebno imati dobar kontrast boja na vašoj veb stranici?
#### --distractors--
Kako bi se stranica učinila življom.

---

Radi ispunjavanja zahteva za optimizaciju pretraživačkih mesinica (SEO).

---

Za isticanje važnih elemenata stranice.
#### --answer--
Da bi sadržaj stranice bio pristupačan i čitljiv.
### --question--

#### --text--
Koji od sledećih alata vam omogućava da unesete pozadinske i prednje boje i proverite njihov odnos kontrasta?
#### --distractors--
TPGi Analizator bojarne kontraste

---

Figma

---

Canva
#### --answer--
WebAIM-ov Prover Kontrasta Boja
### --question--

#### --text--
Koji od sledećih alata vam omogućava da izaberete boje pozadine i prednjeg plana iz sadržaja prikazanog na vašem ekranu i proverite njihov kontrastni odnos?
#### --distractors--
Figma

---

Canva

---

WebAIM-ov Proverivač Kontrasta Boja
#### --answer--
TPGi Analizator bojarne kontraste
### --question--

#### --text--
Zašto ne biste trebali koristiti `display: none` i `visibility: hidden` za vizuelno skrivanje sadržaja?
#### --distractors--
Ovi metodi osiguravaju da samo asistivne tehnologije, poput čitača ekrana, mogu pristupiti skrivenom sadržaju.

---

Ovi metodi omogućavaju da je sadržaj skriven samo sve dok korisnik mišem ne pređe preko njega.

---

Ovi metodi ne funkcionišu u nekim pregledačima.
#### --answer--
Ovi metodi uklanjaju sadržaj iz stabla pristupačnosti, što čini nemogućim da čitači ekrana pristupe skrivenom sadržaju.
### --question--

#### --text--
Šta je stabak pristupačnosti?
#### --distractors--
Vizuelni prikaz rasporeda web stranice.

---

Struktura koju koriste čitači ekrana kako bi pročitali tekstualni sadržaj veb stranice.

---

Kopija stabla DOM-a.
#### --answer--
Struktura koju čitači ekrana koriste da tumače i interaguju sa sadržajem na veb stranici.
### --question--

#### --text--
Koja od sledećih osigurava da slika ima minimalnu širinu od `400px`, ali postaje šira kada je širina vidokruga veća od `1000px`?
#### --distractors--

```css
img {
  width: max(400px, 10vw);
}
```

---

```css
img {
  width: max(400px, 30vw);
}
```

---

```css
img {
  width: max(400px, 20vw);
}
```

#### --answer--

```css
img {
  width: max(400px, 40vw);
}
```

### --question--

#### --text--
Koju od sledećih `scroll-behavior` vrednosti omogućava glatko skrolovanje?
#### --distractors--

`auto`

---

`inherit`

---

`revert`

#### --answer--

`smooth`

### --question--

#### --text--
Koja od sledećih karakteristika se koristi za detekciju preferencija animacija korisnika?
#### --distractors--

`prefers-contrast`

---

`display-mode`

---

`animation`

#### --answer--

`prefers-reduced-motion`

### --question--

#### --text--
Koji od sledećih predstavlja problem pristupačnosti atributa `placeholder` u elementu `input`?
#### --distractors--
Placeholder tekst sprečava čitače ekrana da pročitaju tekst oznake polja za unos.

---

Placeholder tekst sprečava čitače ekrana da čitaju vrednost unosa.

---

Tekst za zamenu je premali/premalen da bi bio čitljiv.
#### --answer--
Placeholder tekst se može pomešati sa stvarnom vrednošću unosa.
### --question--

#### --text--
Šta atribut `hidden` radi?
#### --distractors--
Skriva sadržaj i otkriva ga pri prelizanju mišem.

---

Skriva sadržaj samo od stabla pristupačnosti.

---

Skriva sadržaj vizuelno, ali je sadržaj dostupan u drvetu pristupačnosti.
#### --answer--
Skriva sadržaj kako vizuelno, tako i iz stabla pristupačnosti.