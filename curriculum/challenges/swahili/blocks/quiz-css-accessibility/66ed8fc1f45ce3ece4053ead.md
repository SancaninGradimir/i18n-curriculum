---
id: 66ed8fc1f45ce3ece4053ead
title: Pokušaj dobijanja pristupa CSS-a
challengeType: 8
dashedName: quiz-css-accessibility
---

# --description--

Da bi prošao kratki test, moraš tačno odgovoriti na najmanje 9 od 10 pitanja koja su navedena ispod.

# --quizzes--

## --quiz--

### --question--

#### --text--

Zašto je važno imati dobar balans nijansi boja na vašoj veb stranici?

#### --distractors--

Da bi se stranica učinila svetlijim bojama.

[No Swahili text provided.]

Da bi se zadovoljili zahtevi optimizacije pretraživačkih motora (SEO).

[No Swahili text provided.]

Da bi se ključni elementi stranice bolje istakli/videli.

#### --answer--

Da bi sadržaj stranice bio dostupan i čitljiv.

### --question--

#### --text--

Koji alat iz sledećih vam omogućava da unesete boje pozadine i prednjeg plana te proverite njihov odnos kontrasta boja?

#### --distractors--

TPGi Analizator kontrasta boje

[No Swahili text provided.]

Figma

[No Swahili text provided.]

Canva

#### --answer--

WebAIM-ov prover kontrasta boja

### --question--

#### --text--

Koji od sledećih alata vam omogućava da izaberete boje pozadine i prednjeg plana iz sadržaja prikazanog na vašem ekranu i proverite njihov odnos kontrasta boja?

#### --distractors--

Figma

[No Swahili text provided.]

Canva

[No Swahili text provided.]

WebAIM-ov prover kontrasta boja

#### --answer--

TPGi Analizator kontrasta boje

### --question--

#### --text--

Zašto nije moguće koristiti `display: none` i `visibility: hidden` da sakrije sadržaj na vidljiv način?

#### --distractors--

Ove metode čine skriveni sadržaj dostupan samo asistivnim tehnologijama, kao što je čitač ekrana.

[No Swahili text provided.]

Ovi načini skrivaju sadržaj samo dok korisnik ne prevede mišem preko tog sadržaja.

[No Swahili text provided.]

Ove metode ne rade sa nekim pregledačima.

#### --answer--

Ove metode uklanjaju sadržaj iz stabla pristupačnosti i onemogućavaju čitačima ekrana pristup skrivenom sadržaju.

### --question--

#### --text--

Šta je stablo pristupačnosti?

#### --distractors--

Vizuelni odnos/proporcije rasporeda web stranice.

[No Swahili text provided.]

Struktura koja se koristi od strane čitača ekrana za čitanje tekstualnog sadržaja veb stranice.

[No Swahili text provided.]

Kopija drva od DOM.

#### --answer--

Struktura koja je korišćena od strane čitača ekrana za interpretaciju i interakciju sa sadržajem na web stranici.

### --question--

#### --text--

Koji od sljedećih osigurava da slika ima minimalnu širinu od `400px`, ali se više proširi kada je širina vidljivog područja veća od `1000px`?

#### --distractors--

```css
img {
  width: max(400px, 10vw);
}
```

[No Swahili text provided.]

```css
img {
  width: max(400px, 30vw);
}
```

[No Swahili text provided.]

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

Koji od vrednosti `scroll-behavior` ukazuje ponašanje pregledača za stabilnost?

#### --distractors--

`auto`

[No Swahili text provided.]

`inherit`

[No Swahili text provided.]

`revert`

#### --answer--

`smooth`

### --question--

#### --text--

Koja je karakteristika među sledećim koja se koristi za otkrivanje preferencija korisnika u vezi sa pokretnim grafikama?

#### --distractors--

`prefers-contrast`

[No Swahili text provided.]

`display-mode`

[No Swahili text provided.]

`animation`

#### --answer--

`prefers-reduced-motion`

### --question--

#### --text--

Koji od sledećih je problem pristupa/dostupnosti za svojstvo `placeholder` u elementu `input`?

#### --distractors--

Tekst naslovnika sprečava čitače ekrana da pročitaju tekst etikete polja za unos.

[No Swahili text provided.]

Tekst zamenača sprečava čitače ekrana da pročitaju vrednost unosa.

[No Swahili text provided.]

Napisi skraćenica su previše mali za čitanje.

#### --answer--

Predstavljajući tekst može se kombinovati sa stvarnom vrednošću unosa.

### --question--

#### --text--

Svojstvo `hidden`, šta radi?

#### --distractors--

Skriv sadržaj i prikazuj kada se miša pređe preko njega.

[No Swahili text provided.]

Skriva sadržaj samo sa stabla pristupa.

[No Swahili text provided.]

Sakrij sadržaj za pregled, ali se sadržaj nalazi na grani pristupačnosti.

#### --answer--

Sakrij sadržaj takođe vidljivo i sa grane navigacije.