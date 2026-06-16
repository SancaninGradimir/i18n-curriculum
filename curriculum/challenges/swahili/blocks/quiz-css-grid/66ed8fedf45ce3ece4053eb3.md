---
id: 66ed8fedf45ce3ece4053eb3
title: CSS Grid Kviz
challengeType: 8
dashedName: quiz-css-grid
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Šta je CSS Grid?
#### --distractors--
Metoda korišćena za prikaz tabela na veb-sajtu.

---

Metoda koja se koristi za mozaično postavljanje slika.

---

Način za prikaz kontura oko HTML elemenata.
#### --answer--
Dvodimenzionalni raspored za HTML dokumente.
### --question--

#### --text--
Koja od sledećih metoda predstavlja ispravan način za kreiranje mrežnog kontejnera (grid container)?
#### --distractors--

`display: grid-area;`

---

`grid: grid-template;`

---

`grid-template: set;`

#### --answer--

`display: grid;`

### --question--

#### --text--
Šta radi svojstvo `grid-template-columns`?
#### --distractors--
Definiše dve kolone i tri reda za kontejner mreže.

---

Postavlja sve kolone za mrežni raspored na fiksnu širinu.

---

Kreira kontejner za dvokolonski grid raspored.
#### --answer--
Definiše broj kolona u mrežnom rasporedu.
### --question--

#### --text--
Šta radi svojstvo `grid-template-rows`?
#### --distractors--
Definiše dimenzije i poziciju elementa u rasporedu mrežnog sistema (grid).

---

Kreira šablon za kreiranje novih redova u mrežici.

---

Definiše podrazumevanu veličinu reda u kontejneru mreže.
#### --answer--
Definiše broj i visinu za svaki red u mrežnom rasporedu.
### --question--

#### --text--
Šta radi funkcija `minmax()`?
#### --distractors--
Prebacuje između prve i druge vrednosti, u zavisnosti od raspoloživog prostora.

---

Vraća prosek dva ulaza.

---

Postavlja minimalnu veličinu elementa za pretraživače koji rade u režimu punog ekrana.
#### --answer--
Postavlja minimalne i maksimalne dimenzije za traku.
### --question--

#### --text--
Koja je skraćenica za svojstva `column-gap` i `row-gap`?
#### --distractors--

`gap-column-row`

---

`gutters`

---

`grid-gap`

#### --answer--

`gap`

### --question--

#### --text--
Koja je razlika između implicitnog i eksplicitnog grida?
#### --distractors--
Implicitne mreže koriste ``grid-template-columns`` svojstvo, dok eksplicitne mreže koriste ``grid-template-rows`` svojstvo.

---

Eksplicitne mreže koriste svojstvo `grid-template-columns` dok implicitne mreže koriste svojstvo `grid-template-rows`.

---

Implicitne mreže koriste svojstva ``grid-template-columns`` ili ``grid-template-rows`` za kreiranje kolona, dok se redovi i kolone automatski kreiraju u eksplicitnim mrežama.
#### --answer--
Eksplicitne mreže koriste svojstva ``grid-template-columns`` ili ``grid-template-rows`` za kreiranje kolona, dok se redovi i kolone u implicitnim mrežama automatski kreiraju.
### --question--

#### --text--
Koja od sledećih jedinica predstavlja frakciju prostora unutar grid kontejnera?
#### --distractors--

`fractional`

---

`frac`

---

`f`

#### --answer--

`fr`

### --question--

#### --text--
Šta su mrežne linije?
#### --distractors--
Skraćeni oblik za redove i kolone.

---

Kontura mrežnog elementa.

---

Linije duž kojih se kreiraju kolone i redovi mreže.
#### --answer--
Linije na kojima počinju i završavaju se svi elementi mrežice.
### --question--

#### --text--
Šta radi svojstvo `grid-column`?
#### --distractors--
Dodaje novi gridi element kao dete elementa na koji je primenjen.

---

Vertikalno poravnava tekst unutar elementa mreže.

---

Postavlja dve kolone za kontejner mreže.
#### --answer--
Definiše elementu u mrežici na kojoj liniji mreže bi trebalo da počne i gde treba da se završi.
### --question--

#### --text--
Kako kreirati četiri kolone jednakih širina?
#### --distractors--

`grid-template-columns: repeat(4);`

---

`grid-template-columns: repeat(1, 4);`

---

`grid-template-columns: repeat(1fr, 4);`

#### --answer--

`grid-template-columns: repeat(4, 1fr);`

### --question--

#### --text--
Šta radi svojstvo `grid-template-areas`?
#### --distractors--
Koristi se za određivanje gde element počinje na liniji unutar mrežnog kontejnera.

---

Služi za kreiranje razmaka između traka unutar kontejnera.

---

Koristi se za ponavljanje sekcija u spisku pesama.
#### --answer--
Koristi se za definisanje imena stavkama koje ćete pozicionirati na mreži.
### --question--

#### --text--
Šta radi svojstvo `grid-auto-flow`?
#### --distractors--
Upravlja redosledom kojim se elementi mreže prikazuju.

---

Podešava razmak između elemenata mrežice.

---

Automatski prilagođava element kako bi odgovarao mreži.
#### --answer--
Kontroliše način na koji se elementi postavljeni automatski ubacuju u mrežu.
### --question--

#### --text--
Koji od sledećih predstavlja ispravan način korišćenja svojstva `grid-template-areas`?
#### --distractors--

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr; 
  grid-template-rows: auto 1fr auto; 
  grid-template-areas: set(
    "header header"
    "sidebar main"
    "footer footer" 
  );
  gap: 20px; 
}
```

---

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr; 
  grid-template-rows: auto 1fr auto; 
  grid-template-areas: apply(
    "header header"
    "sidebar main"
    "footer footer" 
  );
  gap: 20px; 
}
```

---

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr; 
  grid-template-rows: auto 1fr auto; 
  grid-template-areas: set-areas;
  gap: 20px; 
}
```

#### --answer--

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr; 
  grid-template-rows: auto 1fr auto; 
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer"; 
  gap: 20px; 
}
```

### --question--

#### --text--
Koji od sledećih načina je ispravan za rad sa svojstvom `grid-auto-flow`?
#### --distractors--

```css
.social-icons {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: none;
  grid-auto-columns: 1fr;
}
```

---

```css
.social-icons {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: allow;
  grid-auto-columns: 1fr;
}
```

---

```css
.social-icons {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: set;
  grid-auto-columns: 1fr;
}
```

#### --answer--

```css
.social-icons {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-flow: column;
  grid-auto-columns: 1fr;
}
```

### --question--

#### --text--
Koje od sledećih NIJE važeće svojstvo mreže (grid)?
#### --distractors--

`gap`

---

`grid-column`

---

`grid-template-columns`

#### --answer--

`grid-set`

### --question--

#### --text--
Koje od ovih svojstava se mogu koristiti za centriranje elemenata unutar grid elementa?
#### --distractors--

`allow-items`

---

`set-items`

---

`center-items`

#### --answer--

`align-items`

### --question--

#### --text--
Koja od sledećih predstavlja ispravnu vrednost za upotrebu sa svojstvom ``grid-auto-columns``?
#### --distractors--

`grid-auto-columns: unset-grid;`

---

`grid-auto-columns: revert-grid;`

---

`grid-auto-columns: set-content(20%);`

#### --answer--

`grid-auto-columns: 1fr;`

### --question--

#### --text--
Šta su mrežne trake?
#### --distractors--
Skraćena notacija za redove i kolone.

---

Linije po kojima možete animirati kretanje elemenata mreže.

---

Linije na kojima počinje i završava se svaki element mreže.
#### --answer--
Razmaci između dve susedne mrežne linije.
### --question--

#### --text--
Koji je ispravan način korišćenja funkcije `minmax()`?
#### --distractors--

```css
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(apply);
}
```

---

```css
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax();
}
```

---

```css
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(set);
}
```

#### --answer--

```css
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(150px, auto);
}
```

## --quiz--

### --question--

#### --text--
Kako pozicionirati element mreže unutar rasporeda definisanog sa `grid-template-areas`?
#### --distractors--
Direktnim definisanjem veličine i lokacije elementa unutar mreže korišćenjem `grid-template-rows` i `grid-template-columns`.

---

Korišćenjem svojstva ``grid-area`` i navođenjem početnih i krajnjih pozicija za red i kolonu.

---

Postavljanjem kako `grid-area` tako i eksplicitnih koordinata piksela.
#### --answer--
Dodeljivanjem imenovanog područja na svojstvo stavke `grid-area`.
### --question--

#### --text--
Šta svojstvo ``grid-auto-rows`` kontroliše?
#### --distractors--
Visina eksplicitno definisanih redova.

---

Maksimalna širina kolona mreže.

---

Razmak između redova.
#### --answer--
Veličina redova koji su implicitno kreirani.
### --question--

#### --text--
Koje svojstvo biste koristili da biste učinili da element mrežice pokriva više redova?
#### --distractors--

`grid-row-span`

---

`row-span`

---

`span-rows`

#### --answer--

`grid-row`

### --question--

#### --text--
Šta definiše eksplicitnu mrežu?
#### --distractors--
Automatski kreirane trake za prilagođavanje sadržaju.

---

Trase definisane od jedinice `fr`.

---

Staze dodate sa `grid-auto-flow`.
#### --answer--
Trase koje su eksplicitno definisane putem `grid-template-columns` ili `grid-template-rows`.
### --question--

#### --text--
Koja vrednost za `grid-auto-flow` bi omogućila da se novi elementi popune kolona po redosledu?
#### --distractors--

`row`

---

`vertical`

---

`row dense`

#### --answer--

`column`

### --question--

#### --text--
Koja je svrha `grid-template-areas`?
#### --distractors--
Za automatsko generisanje implicitnih traga.

---

Za zamenu jedinice `fr`.

---

Za postavljanje vrednosti `z-index`.
#### --answer--
Za vizuelno mapiranje stavki na nazvane mrežne oblasti.
### --question--

#### --text--
Kako možete nater element da počne na liniji kolone 2 i završi na liniji kolone 4?
#### --distractors--

`grid-column: 2 / span 4;`

---

`grid-column: start 2 / end 4;`

---

`grid-column: from 2 to 4;`

#### --answer--

`grid-column: 2 / 4;`

### --question--

#### --text--
Koji je efekat `grid-template-columns: 1fr 2fr 1fr`?
#### --distractors--
Kreira tri kolone jednakih širina.

---

Čini srednju kolonu tri puta širem nego ostale.

---

Nateruje sve kolone da budu tačno `1fr` širine.
#### --answer--
Kreira tri kolone gde je sredina dvostruko šira od bočnih strana.
### --question--

#### --text--
Kako biste kreirali mrežu sa 3 jednake kolone i razmakom od `20px` između njih?
#### --distractors--

```css
.container {
  display: grid;
  grid-template: repeat(3, 1fr) / 20px;
} 
```

---

```css
.container {
  display: grid;
  grid: 1fr 1fr 1fr / gap 20px;
}
```

---

```css
.container {
  display: grid;
  grid-template-columns: 20px 1fr 1fr 1fr;
}
```

#### --answer--

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
```

### --question--

#### --text--
Šta kreira `repeat(3, minmax(100px, 1fr))`?
#### --distractors--
Tri kolone koje ne mogu da se smanje ispod `100px`.

---

Tri fiksne `100px` kolone.

---

Tri reda sa maksimalnom visinom od `1fr`.
#### --answer--
Tri kolone koje rastu proporcionalno, ali neće se smanjiti ispod `100px`.
### --question--

#### --text--
Koja izjava o implicitnim mrežama je tačna?
#### --distractors--
Implicitne mreže ignoriraju svojstvo `gap`.

---

Implicitne traske moraju biti definisane sa `grid-template-areas`.

---

Implicitni traci se mogu kreirati samo korišćenjem ``grid-auto-flow`` property-ja.
#### --answer--
Implicitni kanali se kreiraju kada sadržaj ne odgovara eksplicitnim kanalima.
### --question--

#### --text--
Šta svojstvo `place-items` radi u CSS Gridu?
#### --distractors--
Automatski određuje veličinu elemenata mreže na osnovu dostupnog prostora.

---

Kontroliše definicije kolona i redova šablonu mreže (grid template).

---

Prilagođava redosled elemenata mrežne strukture unutar kontejnera.
#### --answer--
To je skraćeni način za poravnavanje elemenata mreže u obe ose: blok i inline osa.
### --question--

#### --text--
Šta radi ovaj CSS?

```css
.container {
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
}
```

#### --distractors--
Kreira fiksne `150px` kolone koje prelivaju kontejner.

---

Kreira kolone koje su tačno `1fr` široke, bez obzira na sadržaj.

---

Kreira maksimalno jednu kolonu za svaku `150px` raspoložive širine.
#### --answer--
Kreira fleksibilne kolone koje su najmanje `150px` i koje se skupljaju kada je prostor ograničen.
### --question--

#### --text--
Kako možete kreirati asimetrične rasporede mreže?
#### --distractors--
Korišćenjem samo `fr` jedinica.

---

Mešanjem različitih jedinica dužine u `grid-template-columns`.

---

Postavljanjem `grid-asymmetric: true`.
#### --answer--
Definisanjem različitih veličina za svaku traku.
### --question--

#### --text--
Šta `grid-column-start: 2` radi sa elementom mrežice?
#### --distractors--
Razvlači ga tako da pokrije 2 kolone.

---

Pomereno je za 2 piksela.

---

Postavlja ga počevši od druge vertikalne linije mreže.
#### --answer--
Natera ga da počne na drugoj liniji kolone.
### --question--

#### --text--
Koji svojstvo biste koristili za kontrolu ponašanja prelivanja u mrežnim trakama?
#### --distractors--

`grid-overflow`

---

`track-sizing`

---

`fit-content`

#### --answer--

`minmax()`

### --question--

#### --text--
Šta će biti rezultat za sledeći kod?

```css
.container {
  display: grid;
  grid-template-columns: 100px 1fr 2fr;
  grid-template-rows: auto 150px;
  gap: 10px;
}
```

#### --distractors--
Kontejner će imati tri kolone jednakih širina i dva reda, pri čemu svaki red ima visinu od `150px`.

---

Kontejner će imati tri kolone, sve sa širinom `100px`, i dve redove visine `150px`.

---

Kontejner će imati dva reda, svaki sa visinom od `1fr`.
#### --answer--
Kontejner će imati tri kolone: 100px, `1fr` i `2fr` široke i dva reda: jedan sa `auto` visinom i jedan sa visinom od `150px`.
### --question--

#### --text--
Kako biste učinili da stavka u mrežici pokrije sve dostupne redove?
#### --distractors--

`grid-row: full;`

---

`grid-row: auto / -1;`

---

`grid-row: 1 / span infinite;`

#### --answer--

`grid-row: 1 / -1;`

### --question--

#### --text--
Koje svojstvo kontroliše poravnanje elemenata mreže duž blok osi?
#### --distractors--

`justify-items`

---

`place-items`

---

`align-content`

#### --answer--

`align-items`

### --question--

#### --text--
Kako možete osigurati da element u mrežici ostane u prvoj koloni bez obzira na promene mreže?
#### --distractors--

`grid-column: fixed;`

---

`grid-column: first;`

---

`grid-lock: column;`

#### --answer--

`grid-column: 1;`
