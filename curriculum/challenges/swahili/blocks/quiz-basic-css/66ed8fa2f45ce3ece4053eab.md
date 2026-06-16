---
id: 66ed8fa2f45ce3ece4053eab
title: Test iz osnova CSS-a
challengeType: 8
dashedName: quiz-basic-css
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Šta znači CSS?
#### --distractors--
Kaskadna skripta stila

---

Konkatenacija Stilskih Skripti

---

Castor Sage Stil
#### --answer--
Kasadni listovi stilova
### --question--

#### --text--
Koja od sledećih je ispravno CSS pravilo?
#### --distractors--

`p=red`

---

`p (color: red)`

---

`{p color: red;}`

#### --answer--

`p {color: red;}`

### --question--

#### --text--
Šta radi `<meta name="viewport">`?
#### --distractors--
Povezuje eksterne stilove sa web stranicom radi responsivnog dizajna.

---

On određuje metadata koje koriste pretraživači za indeksiranje web stranice.

---

Definiše kodiranje znakova korišćeno na veb stranici.
#### --answer--
Upravlja oblikom i veličinom web stranice na različitim veličinama ekrana.
### --question--

#### --text--
Koja sintaksa je ispravna za korišćenje inline CSS-a?
#### --distractors--

`<p color =  blue></p>`

---

`<p><style = blue></p>`

---

`p {color: blue;}`

#### --answer--

`<p style="color: blue;"></p>`

### --question--

#### --text--
Kada se koristi interni CSS, gde je element ``style`` postavljen unutar HTML-a?
#### --distractors--
U `meta` elementu.

---

U elementu `script`.

---

U elementu `body`.
#### --answer--
U `head` elementu.
### --question--

#### --text--
Koji pravilo je tačno za određivanje širine i visine u CSS-u?
#### --distractors--

`height-width: 50px;`

---

`width-and-height: 50px;`

---

`flex-width: 50px; flex-height: 50px;`

#### --answer--

`width: 50px; height: 50px;`

### --question--

#### --text--
Koji selektor pravilno cilja elemente `h1` samo kada su unutar `div`?
#### --distractors--

`div, h1 {}`

---

`div ~ h1 {}`

---

`div + h1 {}`

#### --answer--

`div h1 {}`

### --question--

#### --text--
Koji selektor je tačan za ciljanje direktnih potomaka elementa `footer`?
#### --distractors--

`footer ~ ul {}`

---

`footer + ul {}`

---

`footer ul {}`

#### --answer--

`footer > ul {}`

### --question--

#### --text--
Koji selektor je tačan za ciljanje sledećeg brata od `img`?
#### --distractors--

`img h1 {}`

---

`img > h1 {}`

---

`img ~ h1 {}`

#### --answer--

`img + h1 {}`

### --question--

#### --text--
Koji selektor je ispravan za ciljanje svih suseda koji nastaju nakon `img` elementa?
#### --distractors--

`img > caption {}`

---

`img caption {}`

---

`img + caption {}`

#### --answer--

`img ~ caption {}`

### --question--

#### --text--
Koja tvrdnja je TAČNA za blok elemente?
#### --distractors--
Elementi na nivou bloka podrazumevano se slažu horizontalno.

---

``width` i `height` svojstva obično ne važe za elemente nivoa bloka, osim ako ne postavite njihovo `display` svojstvo na `inline-block`.`

---

Blok elementi ne smeju sadržati inline elemente unutar sebe.
#### --answer--
Elementi na nivou bloka počinju sa nove linije i zauzimaju punu širinu svog kontejnera.
### --question--

#### --text--
Koja izjava je TAČNA kada se koristi vrednost `inline-block`?
#### --distractors--
Elementi se slažu vertikalno, uvek zauzimajući punu širinu svog kontejnera.

---

Elementi se poravnaju horizontalno, ali ne dozvoljavaju primenu vertikalnog paddinga ili margine.

---

Elementi poštuju podešavanja širine i visine, ali ne mogu da sadrže druge elemente unutar sebe.
#### --answer--
Elementi zadržavaju protok na nivou linije (inline flow), ali omogućavaju postavljanje širine i visine.
### --question--

#### --text--
Iz navedenih selektora, koji ima najveću specifičnost?
#### --distractors--

`div`

---

`h1`

---

`p`

#### --answer--

`#id`

### --question--

#### --text--
Iz navedenih selektora, koji ima najmanju specifičnost?
#### --distractors--

`#id`

---

`.class`

---

`div h1`

#### --answer--

`h1`

### --question--

#### --text--
Šta radi selektor `*`?
#### --distractors--
Cilja na neke elemente na stranici.

---

Cilja elemente koji imaju potomke na stranici.

---

Cilja na sve `p` elemente na stranici.
#### --answer--
Cilja na sve elemente na stranici.
### --question--

#### --text--
Šta radi `!important` u CSS-u?
#### --distractors--
CSS pravilo funkcioniše isključivo za inline stilove i ignoriše stilove definisane u eksternim ili internim listovima stilova.

---

On onemogućava sva druga CSS svojstva primenjena na isti element, efektivno ga čineći jedinim pravilom koje utiče na stilizovanje tog elementa.

---

To se primenjuje samo na određeni selektor ili grupu elemenata.
#### --answer--
Nadjačava bilo koje druge vrednosti primenjene na svojstvo za taj selektor.
### --question--

#### --text--
Kako funkcioniše algoritam CSS kaskade?
#### --distractors--
Određuje stilove elementa na osnovu reda deklaracije, bez obzira na druge faktore.

---

Primjenjuje stilove isključivo na osnovu redosleda u kojem su napisani, ignorisanjem specifičnosti.

---

Primjenjuje stilove prioritetizujući specifičnost, ignorisanjem porekla i relevantnosti.
#### --answer--
Određuje stilove elementa na osnovu specifičnosti i redosleda deklaracije.
### --question--

#### --text--
Koje pravilo se primenjuje za marginu na sve strane?
#### --distractors--

`margin-top: 32px;`

---

`margin: 32px 0;`

---

`margin: 0 32px;`

#### --answer--

`margin: 32px;`

### --question--

#### --text--
Koje pravilo primenjuje `24px` padding za vrh i dno?
#### --distractors--

`padding: 24px;`

---

`padding-top-bottom: 24px;`

---

`padding: 0 24px;`

#### --answer--

`padding: 24px 0;`

### --question--

#### --text--
Za `padding: 10px 20px 30px 40px`, koji je tačan redosled vrednosti?
#### --distractors--
Desno, Gore, Levo, Dole.

---

Gornji, Levi, Donji, Desni.

---

Gornji, Donji, Desni, Levi.
#### --answer--
Gornji, Desni, Donji, Levi.

## --quiz--

### --question--

#### --text--
Koji su glavni delovi CSS pravila?
#### --distractors--
Elementi i atributi

---

Stil i listovi

---

Skripte i vrednosti
#### --answer--
Selectors and declaration blocks
Selektori i blokovi deklaracija
### --question--

#### --text--
Koji od sledećih je ispravna sintaksa za CSS pravilo?
#### --distractors--

```css
body [
  font-family: Arial;
]
```

---

```css
font-family {
  body: Arial;
}
```

---

```css
body {
  font-family; Arial:
}
```

#### --answer--

```css
body {
  font-family: Arial;
}
```

### --question--

#### --text--
Šta su podrazumevani stilovi pregledača?
#### --distractors--
HTML elementi koji poseduju iste stilizacione karakteristike bez obzira na pretraživač.

---

To su obavezni stilovi koje morate koristiti za specifične HTML elemente.

---

To su teme boja za razne pretraživače.
#### --answer--
Pravila CSS-a koja pregledači automatski primenjuju.
### --question--

#### --text--
Koja je podrazumevana vrednost za svojstvo `width`?
#### --distractors--

`none`

---

`0`

---

`100%`

#### --answer--

`auto`

### --question--

#### --text--
Šta svojstvo `min-height` definiše?
#### --distractors--
Početna visina za element.

---

Visina za element.

---

Maksimalna visina za element.
#### --answer--
Minimalna visina za element.
### --question--

#### --text--
Koje od sledećih je TAČNO za univerzalni selektor `*`?
#### --distractors--
Ima najvišu specifičnost jer može stilizovati sve elemente na stranici.

---

Doprinosi 1 svim delovima vrednosti specifičnosti.

---

Ne može da resetuje stilove u različitim pregledačima.
#### --answer--
Ima najnižu vrednost specifičnosti među svim selektorima.
### --question--

#### --text--
Koji selektor pravilno cilja elemente `li` za ukrasnu listu?
#### --distractors--

`li {}`

---

`ul li {}`

---

`ol + li {}`

#### --answer--

`ol li {}`

### --question--

#### --text--
Koji selektor cilja na paragraf elemente elementa `div`?
#### --distractors--

`p div {}`

---

`div, p {}`

---

`p, div {}`

#### --answer--

`div p {}`

### --question--

#### --text--
Gde ``margin`` primenjuje svojstva stila?
#### --distractors--
Prostor unutar elementa.

---

Između sadržaja i granice.

---

Na obodu elementa.
#### --answer--
Prostor izvan elementa.
### --question--

#### --text--
Gde svojstvo ``padding`` primenjuje stilizovanje?
#### --distractors--
Između granice elementa i okolnih elemenata.

---

Prostor izvan elementa.

---

Na obodu elementa.
#### --answer--
Prostor unutar elementa.
### --question--

#### --text--
Koja tvrdnja je NETAČNA o elementima na nivou bloka?
#### --distractors--
Mogu se proširiti da odgovore širini svog kontejnera.

---

Uobičajeni elementi na nivou bloka uključuju `div`, `p`, i `section`.

---

Elementi na nivou bloka počinju sa nove linije i zauzimaju punu širinu svog kontejnera.
#### --answer--
Ne mogu zauzeti punu dostupnu širinu jer im je to onemogućeno/blokirano.
### --question--

#### --text--
Koja izjava je NETAČNA kada se koristi vrednost `inline-block`?
#### --distractors--
`inline-block` elementi se ponašaju kao ulinjani elementi.

---

Mogu imati svojstva `width` i `height`.

---

Elementi zadržavaju inline protok, ali omogućavaju podešavanje `width` i `height`.
#### --answer--
Oni ne dele svojstva sa inline ili blok nivo elementima.
### --question--

#### --text--
Šta je TAČNO o ključnoj reči `!important`?
#### --distractors--
Koriste se za pravljenje komentara za važno CSS svojstvo.

---

Obezbeđuju da CSS svojstvo ima ispravnu sintaksu.

---

Olakšavaju održavanje CSS pravila.
#### --answer--
Nadjačavaju specifičnost drugih selektora.
### --question--

#### --text--
Koji znak prethodi imenu selektora klase?
#### --distractors--

`#`

---

`$`

---

`*`

#### --answer--

`.`

### --question--

#### --text--
Šta je NETAČNO za inline elemente?
#### --distractors--
Zauzimaju samo onoliko prostora koliko je potrebno.

---

Ne počinju na novoj liniji.

---

Uobičajeni inline elementi uključuju `span` i `img`.
#### --answer--
Uvek počinju na novoj liniji.
### --question--

#### --text--
Gde su dostupni interni CSS stilovi?
#### --distractors--
Ovo su stilovi koji su važni za projekat, pa se ne dele spolja.

---

Budući da čine osnovni stil projekta, sačuvani su u fajlu ``styles.css`` kako bi druge veb stranice mogle da im pristupe.

---

Oni su skladišteni unutar elementa `body` kada postoji samo jedna veb stranica za stilizovanje.
#### --answer--
Napisani su unutar sekcije `style` unutar elementa `head`.
### --question--

#### --text--
Koji je redosled za primenu svojstva ``padding`` kada se koristi skraćena sintaksa?
#### --distractors--
`top`, `bottom`, `left`, `right`

---

`left`, `right`, `top`, `bottom`

---

`right`, `top`, `left`, `bottom`
#### --answer--
`top`, `right`, `bottom`, `left`
### --question--

#### --text--
Koji je redosled za primenu svojstva ``margin`` kada se koristi skraćena sintaksa?
#### --distractors--
`left`, `right`, `top`, `bottom`

---

`right`, `top`, `left`, `bottom`

---

`top`, `bottom`, `left`, `right`
#### --answer--
`top`, `right`, `bottom`, `left`
### --question--

#### --text--
Za šta se koriste inline CSS stilovi?
#### --distractors--
Koriste se samo za stilizovanje uline elemenata.

---

Koriste se za stilizovanje elemenata samo kada su svi prikazani na istoj liniji viewporta pregledača.

---

Koriste se za rešavanje problema sa razdvajanjem odgovornosti.
#### --answer--
Koriste se za direktno stilizovanje unutar elementa, umesto korišćenja internog ili eksternog CSS-a.
### --question--

#### --text--
Koji simbol prethodi ID selektoru?
#### --distractors--

`.`

---

`*`

---

`$`

#### --answer--

`#`

