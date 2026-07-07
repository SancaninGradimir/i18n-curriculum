---
id: 672bbeaa5afdc5a98d5ab8ff
title: Koja su primjeri umjetne/veštačke klase za područje?
challengeType: 19
dashedName: what-are-examples-of-location-pseudo-classes
---

# --interactive--

Darasa la bandia la eneo hutumika kwa ajili ya kupamba viungo na vipengele vinavyolengwa ndani ya hati ya sasa. Hutoa njia ya kutumia mitindo kulingana na kama kiungo kimebofyanwa au kama kipengele kiko makini kwa sasa.

Mifano ya darasa la bandia la eneo ni:

- `:link`
- `:visited`
- `:any-link`
- `:local-link`
- `:target`

Tuchunguze kwa undani kila moja ya darasa la bandia haya.

Darasa la bandia la `:link` linakuwezesha kulenga viungo vyote ambavyo havijabofyanwa kwenye ukurasa wa mtandao. Unaweza kulitumia kupamba viungo tofauti kabla mtumizi hajavibofya. Kwa mfano, unaweza kutaka kufanya viungo vyote visivyobofyanwa kuwa buluu au rangi kuu ya tovuti yako:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<a target="_blank" href="https://www.example.com">Visit Example.com</a>
```

```css
a:link {
  color: magenta;
}
```

:::

U ovom slučaju, bilo koji link koji korisnik još nije kliknuo biće vidljiv u boji magenta. Kada korisnik klikne na link, stil ``:link`` više se neće koristiti, a pseudo-klasa ``:visited`` počinje da deluje. Pseudo-klasa ``:visited`` postaje aktivna nakon što korisnik klikne na link, pa ga možete koristiti za ciljanje linkova koje je korisnik već kliknuo.

Ovo je primer za promenu stanja kliknutog elementa na boju `purple`:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<a target="_blank" href="https://www.example.com">Visit Example.com</a>
```

```css
a:visited {
  color: purple;
}
```

:::

Darasa la bandia la `:visited` husaidia watumizi kutofautisha kati ya viungo ambavyo wamevitembelea na ambavyo hawajavitembelea.

Darasa la bandia la `:any-link` ni mchanganyiko wa madarasa ya bandia ya `:link` na `:visited`. Hivyo linalingana na kipengele chochote cha nanga chenye sifa ya `href`, bila kujali kama kimebofyanwa au la.

Hapa kuna mfano wa kubadilisha rangi ya kiungo kwa darasa la bandia la `:any-link` kuwa `crimson`:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<a target="_blank" href="https://www.example.com">Visit Example.com</a>
```

```css
a:any-link {
  color: crimson;
}
```

:::

Darasa la bandia la `:local-link` linalenga viungo vinavyoelekeza kwenye hati ile ile. Linaweza kuwa na manufaa unapotaka kutofautisha viungo vya ndani na viungo vya nje. Kwa sasa, hakuna kivinjari kinachounga mkono darasa la bandia la `:local-link`.

Sintetička klasa ``:target`` selektuje element koji odgovara ID-u trenutnog elementa `URL`, na primer, ``#section1``. Vrlo je važno za stranice sa internom navigacijom.

Ovde je primer HTML koji predstavlja navigaciju unutar stranice. CSS koristi pseudo-klasu `:target` za stilizovanje sekcije koja odgovara mestu gde je korisnik upućen:

:::interactive_editor

```html
<link rel="stylesheet" href="styles.css" />
<nav id="table-of-contents">
  <ul>
    <li><a href="#section1">Introduction</a></li>
    <li><a href="#section2">Features</a></li>
  </ul>
</nav>

<section id="section1">
  <h2>Introduction</h2>
  <p>This is the introduction section.</p>
</section>

<section id="section2">
  <h2>Features</h2>
  <p>This section describes the features.</p>
</section>
```

```css
section:target {
  background-color: green;
  border: 2px solid green;
  padding: 10px;
}
```

:::

Kada korisnik klikne na jedan od navigacionih linkova, pozadinska boja odgovarajućeg dela će se promeniti u zelenu.

# --questions--

## --text--

Šta je lažna klasa koja omogućava stilizovanje elementa koji odgovara ID-u trenutnog komada, kao što je URL, poput `#section1`?

## --answers--

`:hover`

### --feedback--

Zamislite kako možete istaknuti određeni deo prilikom navigacije kroz interne linkove na stranici.

[No Swahili text provided.]

`:focus`

### --feedback--

Razmislite kako možete istaknuti određeni deo dok pretražujete pomoću internih linkova stranice.

[No Swahili text provided.]

`:target`

[No Swahili text provided.]

`:checked`

### --feedback--

Zamislite kako možete istaknuti određeni deo prilikom navigacije kroz interne linkove na stranici.

## --video-solution--

3

## --text--

Gde se veštačka učionica koristi, posebno?

## --answers--

Kada dekorisać elemente u skladu sa njihovim vezama/povezanjima.

### --feedback--

Razmislite kako možete prilagoditi linkove i ciljane komponente na osnovu interakcije korisnika.

[No Swahili text provided.]

Prilikom primene stilova na osnovu toga da li je link kliknut ili element trenutno fokusiran.

[No Swahili text provided.]

Kada se prilagođavaju elementi u skladu sa svojstvima roditeljskog elementa.

### --feedback--

Razmislite kako možete stilizovati ciljane linkove i elemente na osnovu interakcije korisnika.

[No Swahili text provided.]

Prilikom izmene rasporeda web stranice putem direktnih promena.

### --feedback--

Fikiria jinsi unavyoweza kupamba viungo na vipengele vilivyolengwa kulingana na mwingiliano wa mtumizi.

## --video-solution--

2

## --text--

Ni darasa gani la bandia lililoundwa kulenga viungo vinavyoelekeza kwenye hati ile ile lakini halijaungwa mkono na kivinjari chochote kwa sasa?

## --answers--

`:any-link`

### --feedback--

Zamislite veštačku klasu dizajniranu da razlikuje unutrašnje i spoljašnje organe, iako još uvek nije podržana.

[No Swahili text provided.]

`:local-link`

[No Swahili text provided.]

`:visited`

### --feedback--

Zamislite veštačku strukturu namenjenu za razlikovanje unutrašnjih i spoljašnjih organa, iako još uvek nije potkrepljena.

[No Swahili text provided.]

`:target`

### --feedback--

Zamislite veštačku klasu koja je namenjena da razlikuje unutrašnje i spoljašnje karakteristike, iako još uvek nije podržana.

## --video-solution--

2