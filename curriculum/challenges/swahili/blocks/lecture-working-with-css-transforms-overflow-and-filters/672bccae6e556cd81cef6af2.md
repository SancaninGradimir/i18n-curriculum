---
id: 672bccae6e556cd81cef6af2
title: Šta je kolapsiranje margina i kako funkcioniše?
challengeType: 19
dashedName: what-is-margin-collapsing
---

# --interactive--

Kolaps margina je fundamentalni koncept u CSS-u koji često zbunjuje početnike u razvoju veb sadržaja.

Ovo ponašanje nastaje kada se vertikalne margine susednih elemenata preklapaju, što rezultira jednom maržom koja je jednaka većoj od dve.

Razumevanje kolapsiranja margina je važno za preciznu kontrolu nad razmakom i rasporedom u web dizajnu. Stoga, hajde da saznamo kako funkcioniše kolapsiranje margina i istražimo neke uobičajene scenarije gde se to dešava.

U CSS-u kada se dva vertikalna margina dodirnu međusobno, one će kolapsirati, što znači da umesto da se sabere, veća margina pobeđuje i određuje razmak između elemenata. Ovo ponašanje važi samo za vertikalne margine (gore i dole), a ne za horizontalne margine (levo i desno). Dakle, evo primera koji ilustruje ovaj koncept:

:::interactive_editor

```html
<style>
  .box1 {
    margin-bottom: 20px;
    background-color: lightblue;
  }
  .box2 {
    margin-top: 30px;
    background-color: lightgreen;
  }
</style>

<div class="box1">Box 1</div>
<div class="box2">Box 2</div>
```

:::

U ovom primeru, možda očekujete da je ukupni prostor između `.box1` i `.box2` od 50 piksela (20 piksela plus 30 piksela). Međutim, zbog kolapsiranja margina stvarni prostor će biti 30 piksela, što je veći od dve margine.

Kao što smo videli u prethodnom primeru, margine susednih elemenata braće će se kolapsirati. Ovo je najjednostavniji slučaj kolapsiranja margina. Istražićemo više slučajeva gde može doći do kolapsiranja margina.

Margine se mogu kolapsirati i između roditeljskog elementa i njegovog prvog ili poslednjeg deteta. Ako ne postoji ivica, padding, ugrađeni sadržaj ili razmak za razdvajanje margine roditelja od margine deteta, one će se kolapsirati.

:::interactive_editor

```html
<style>
  .parent {
    margin-top: 40px;
    background-color: lightyellow;
  }
  .child {
    margin-top: 30px;
    background-color: lightpink;
  }
</style>

<div class="parent">
  <div class="child">Child element</div>
</div>
```

:::

U ovom slučaju, možda očekujete da je dete na visini od 70 piksela od vrha (40 piksela plus 30 piksela). Međutim, margine se kolabiraju i koristi se veća margina od 40 piksela.

Ako element nema sadržaj, padding ili granicu, njegove gornje i donje margine mogu se srušiti u jednu marginu.

:::interactive_editor

```html
<style>
  .empty-block {
    margin-top: 20px;
    margin-bottom: 10px;
    height: 0;
  }
  .next-block {
    background-color: lightgray;
  }
</style>

<div class="empty-block"></div>
<div class="next-block">Next block</div>
```

:::

U ovom primeru, gornje i donje margine za ``empty-block`` se kolapsiraju u jedan margina od 20 piksela, veći od ta dva.

Evo primera sprečavanja kolapsa korišćenjem padding-a:

:::interactive_editor

```html
<style>
  .parent {
    margin-top: 40px;
    padding-top: 1px;
    background-color: lightyellow;
  }
  .child {
    margin-top: 30px;
    background-color: lightpink;
  }
</style>

<div class="parent">
  <div class="child">Child element</div>
</div>
```

:::

U ovom slučaju, padding od jednog piksela na roditelju sprečava kolaps margine, što rezultira ukupnim prostorom od 71 piksela od vrha roditelja do vrha sadržaja deteta.

Razumevanje kolapsiranja margina važno je za preciznu kontrolu nad rasporedom i razmakom u CSS-u. Iako ponekad može dovesti do neočekivanih rezultata, to je funkcija dizajnirana da stvori estetski prijatniji i konzistentan razmak u dokumentima. Znanjem kada se kolapsiranje margina dešava i kako ga sprečiti kada je potrebno, možete kreirati predvidljivije i održivije rasporede u vašim web dizajnovima.
# --questions--

## --text--

U kom smeru se dešava kolaps margina?
## --answers--

Samo horizontalne margine.
### --feedback--

Razmislite o tome koje margine (gore, dole, levo, desno) su pogođene ovim ponašanjem.
---

Vertical margins only.

---

Both horizontal and vertical margins.

### --feedback--

Razmislite o tome koje margine (gore, dole, levo, desno) su pogođene ovim ponašanjem.
---

Diagonal margins.

### --feedback--

Razmislite o tome koje margine (gore, dole, levo, desno) su pogođene ovim ponašanjem.
## --video-solution--

2

## --text--

Šta se dešava kada dva susedna elementa imaju različite vrednosti margina?
## --answers--

Margine se sabiraju.
### --feedback--

Razmislite koji margina "pobedi" kada dođe do kolapsa.
---

The smaller margin is used.

### --feedback--

Razmislite koji margina "pobedi" kada dođe do kolapsa.
---

The larger margin is used.

---

The average of the two margins is used.

### --feedback--

Razmislite koji margina "pobedi" kada dođe do kolapsa.
## --video-solution--

3

## --text--

Која од следећих НЕЋЕ спречити колапс марине између родитеља и његовог првог детета?
## --answers--

Dodavanje ``border`` roditelju.
### --feedback--

Razmislite o tome koja svojstva stvaraju razmak između margina roditelja i deteta.
---

Setting `padding-top: 1px;` on the parent.

### --feedback--

Razmislite o tome koja svojstva stvaraju razmak između margina roditelja i deteta.
---

Using `display: inline-block;` on the child.

### --feedback--

Razmislite o tome koja svojstva stvaraju razmak između margina roditelja i deteta.
---

Setting `margin-top: 0;` on the child.

## --video-solution--

4
