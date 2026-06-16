---
id: 66ed8ffcf45ce3ece4053eb5
title: CSS Positioning Quiz
challengeType: 8
dashedName: quiz-css-positioning
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koji od sledećih nije važeća vrednost za svojstvo `position`?
#### --distractors--

`fixed`

---

`absolute`

---

`relative`

#### --answer--

`above`

### --question--

#### --text--
Koja je glavna svrha svojstva ``float`` u CSS-u?
#### --distractors--
Floatovi se koriste da uklone element iz normalnog protoka na stranici i automatski ga pozicioniraju u gornji desni ugao web stranice.

---

`Floatovi se koriste za uklanjanje elementa iz njegovog normalnog protoka na stranici i pozicioniranje ga na vrh njegovog kontejnera.`

---

`Floats se koriste za uklanjanje elementa iz njegovog normalnog protoka na stranici i automatsko pozicioniranje ga u donji desni deo web stranice.`
#### --answer--
Floatovi se koriste za uklanjanje elementa iz normalnog protoka na stranici i pozicioniranje ga bilo sa leve ili desne strane njegovog kontejnera.
### --question--

#### --text--
Koji od sledećih je primer koji uzrokuje da se kutni element "pliva" (float) ulevo?
#### --distractors--

```css
.box {
  left: float;
  margin-right: 15px;
  width: 50px;
  height: 50px;
  background-color: black;
}
```

---

```css
.box {
  position: float-left;
  margin-right: 15px;
  width: 50px;
  height: 50px;
  background-color: black;
}
```

---

```css
.box {
  float: left-side;
  margin-right: 15px;
  width: 50px;
  height: 50px;
  background-color: black;
}
```

#### --answer--

```css
.box {
  float: left;
  margin-right: 15px;
  width: 50px;
  height: 50px;
  background-color: black;
}
```

### --question--

#### --text--
Koja je uloga svojstva `clear`?
#### --distractors--
Koristi se za određivanje da li je potrebno pomeriti element na dno stranice.

---

Koristi se za određivanje da li je element potrebno potpuno ukloniti sa stranice.

---

Koristi se za određivanje da li je potrebno fiksirati element na vrh stranice.
#### --answer--
Koristi se za određivanje da li je potrebno pomeriti element ispod plutajućeg sadržaja.
### --question--

#### --text--
Koji CSS atribut se koristi za kontrolisanje vertikalnog redosleda složene pozicioniranih elemenata koji se preklapaju na stranici?
#### --distractors--

`position`

---

`bg-green`

---

`float`

#### --answer--

`z-index`

### --question--

#### --text--
Koji od sledećih je tačna sintaksa za relativno pozicioniranje?
#### --distractors--

```css
.relative {
  position: relative-position;
  top: 30px;
  left: 30px;
}
```

---

```css
.relative {
  relative-position: relative;
  top: 30px;
  left: 30px;
}
```

---

```css
.relative {
  relative: position;
  top: 30px;
  left: 30px;
}
```

#### --answer--

```css
.relative {
  position: relative;
  top: 30px;
  left: 30px;
}
```

### --question--

#### --text--
Koje CSS svojstvo biste koristili da element učinite fiksiranim na određenoj poziciji na stranici, tako da se ne pomera prilikom skrolovanja?
#### --distractors--

`position: no-scroll;`

---

`position: relative;`

---

`display: block;`

#### --answer--

`position: fixed;`

### --question--

#### --text--
Šta radi apsolutno pozicioniranje elementu?
#### --distractors--
Apsolutno pozicioniranje se koristi za određivanje da li je element potreban da bude pomeren ispod flotujućeg sadržaja.

---

Apsolutno pozicioniranje se koristi za pozicioniranje elementa unutar normalnog protoka dokumenta.

---

Apsolutno pozicioniranje se koristi za kontrolu vertikalnog redosleda složene pozicioniranih elemenata koji se preklapaju na stranici.
#### --answer--
Apsolutno pozicioniranje vam omogućava da izvučete element iz normalnog protoka dokumenta, čime ga čini nezavisnim u odnosu na druge elemente.
### --question--

#### --text--
Koji od sledećih NIJE validno svojstvo koje možete koristiti za apsolutno pozicioniranje?
#### --distractors--

`right`

---

`bottom`

---

`top`

#### --answer--

`side`

### --question--

#### --text--
Koja je ključna razlika između relativnog i apsolutnog pozicioniranja?
#### --distractors--
Apsolutno pozicioniranje postavlja element u lepljiv položaj, dok relativno pozicioniranje izvlači element iz normalnog protoka dokumenta.

---

Relativno pozicioniranje postavlja element u fiksnu poziciju, dok apsolutno pozicioniranje izvlači element iz normalnog toka dokumenta.

---

Apsolutno pozicioniranje postavlja element unutar normalnog protoka dokumenta, dok relativno pozicioniranje izvlači taj element iz tog normalnog protoka.
#### --answer--
Relativno pozicioniranje postavlja element unutar normalnog protoka dokumenta, dok apsolutno pozicioniranje izvlači element iz tog normalnog protoka.
### --question--

#### --text--
Koji od sledećih primera prikazuje pozicioniranje boksa u gornjem levom uglu stranice?
#### --distractors--

```css
.box {
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: coral;
  width: 50px;
  height: 50px;
}
```

---

```css
.box {
  position: absolute;
  top: 0;
  right: 0;
  background-color: coral;
  width: 50px;
  height: 50px;
}
```

---

```css
.box {
  position: absolute;
  bottom: 0;
  right: 0;
  background-color: coral;
  width: 50px;
  height: 50px;
}
```

#### --answer--

```css
.box {
  position: absolute;
  top: 0;
  left: 0;
  background-color: coral;
  width: 50px;
  height: 50px;
}
```

### --question--

#### --text--
Koja metoda pozicioniranja omogućava elementu da ostane na definisanoj poziciji samo kada se skroluje preko određene tačke?
#### --distractors--
Float pozicioniranje.

---

Fiksno pozicioniranje.

---

Apsolutno pozicioniranje.
#### --answer--
Lepljivo pozicioniranje.
### --question--

#### --text--
Koji od sledećih predstavlja tačan primer korišćenja *sticky positioning*-a?
#### --distractors--

```css
.box {
  sticky: position;
  top: 30px;
  right: 30px;
  width: 50px;
  height: 50px;
  background-color: red;
}
```

---

```css
.box {
  position: sticky-fixed;
  top: 30px;
  right: 30px;
  width: 50px;
  height: 50px;
  background-color: red;
}
```

---

```css
.box {
  position: sticky-top;
  right: 30px;
  width: 50px;
  height: 50px;
  background-color: red;
}
```

#### --answer--

```css
.box {
  position: sticky;
  top: 30px;
  right: 30px;
  width: 50px;
  height: 50px;
  background-color: red;
}
```

### --question--

#### --text--
Koja je razlika između `sticky` i `fixed` pozicioniranja?
#### --distractors--
Elementi koji se lepe mogu se koristiti samo u tabelarnim rasporedima, dok fiksni elementi mogu se koristiti u bilo kom tipu CSS rasporeda.

---

Elementi tipa "sticky" uvek će ostati na istoj poziciji, dok fiksirani elementi privremeno pričvršćuju za određenu tačku, nakon čega se ponašaju kao relativni elementi.

---

Elementi fiksne pozicije biće pozicionirani u odnosu na svoju normalnu poziciju, dok će elementi lepljive pozicije ostati samo na određenoj tački, a zatim se ponašati kao elementi relativne pozicije.
#### --answer--
Fiksirani elementi će ostati na istoj poziciji na ekranu, dok se *sticky* elementi vezuju samo za određenu tačku, a zatim se ponašaju kao relativni elementi.
### --question--

#### --text--
Koji problem je `clearfix` rešio prilikom rada sa plutajućim tačkama?
#### --distractors--
Trikovi ``clearfix`` pomogao su da se reši problem elemenata sa plutanjem koji se uklanjaju iz normalnog protoka dokumenta i postavljaju na fiksnu poziciju na stranici.

---

The `clearfix` hack je pomogao da se razreši problem plutajućih elemenata koji nisu responsivni u mobilnim i tablet rasporedima.

---

Trikovi ``clearfix`` su pomogli da reše problem nestajanja floatovanih elemenata sa stranice.
#### --answer--
Trik `clearfix` je pomogao da reši problem preklapanja i kolapsa u rasporedima kada su više elemenata sa `float` svojstvom postavljeno jedan pored drugog.
### --question--

#### --text--
Koji od sledećih predstavlja tačan primer korišćenja `clearfix` haka?
#### --distractors--

```css
.clearfix::before {
  position: fixed;
  top: 0;
  width: 100%;
  clear: both;
}
```

---

```css
.clearfix::after {
  position: relative;
  top: 30px;
  left: 30px;
  clear: all;
}
```

---

```css
.clearfix::before {
  top: 30px;
  clear: none;
}
```

#### --answer--

```css
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```

### --question--

#### --text--
Šta je statičko pozicioniranje?
#### --distractors--
Ovo se koristi za uklanjanje elementa iz njegovog normalnog protoka na stranici i automatsko pozicioniranje ga u gornjem desnom uglu web stranice.

---

To vam omogućava da izvučete element iz normalnog protoka dokumenta, čime se on ponaša nezavisno od drugih elemenata.

---

Ovo omogućava elementu da ostane fiksiran na definisanoj poziciji samo kada skrolujete preko određene tačke.
#### --answer--
Ovo je standardni tok za dokument. Elementi se postavljaju od vrha do dna i sa leve na desno, jedan za drugim.
### --question--

#### --text--
Koji od sledećih je primer postavljanja navigacionog bara (navbar) na vrh stranice korišćenjem fiksnog pozicioniranja?
#### --distractors--

```css
.navbar {
  fixed: top;
  top: 0;
  width: 100%;
}
```

---

```css
.navbar {
  upper: fixed;
  width: 100%;
}
```

---

```css
.navbar {
  position: fixed-top;
  top: 0;
  width: 100%;
}
```

#### --answer--

```css
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
}
```

### --question--

#### --text--
Koji od sledećih je važeća vrednost za svojstvo `z-index`?
#### --distractors--

`12.0`

---

`none`

---

`up`

#### --answer--

`1`

### --question--

#### --text--
Koju od sledećih je podrazumevana vrednost svojstva `position`?
#### --distractors--

`inherit`

---

`initial`

---

`relative`

#### --answer--

`static`

## --quiz--

### --question--

#### --text--
Koja `position` vrednost vam omogućava da prilagodite poziciju elementa sa `top` i `left` dok ga zadržavate u normalnom protoku dokumenta?
#### --distractors--

`position: absolute;`

---

`position: static;`

---

`position: fixed;`

#### --answer--

`position: relative;`

### --question--

#### --text--
Kako se element sa `position: sticky;` inicijalno ponaša?
#### --distractors--
Deluje kao element `fixed` sve dok dođe do pozicije skrolovanja.

---

Uvek je uklonjeno iz normalnog protoka dokumenta.

---

Ono se ponaša kao element `absolute` unutar svog roditelja.
#### --answer--
Ponaša se kao element `relative` sve do nego što se dostigne određena pozicija skrolovanja.
### --question--

#### --text--
Koja od sledećih demonstrira validnu i efikasnu upotrebu svojstva ``z-index`` da učini da ``.box-two`` bude prikazan preko ``.box-one``?
#### --distractors--

```css
.box-one {
  position: static;
  z-index: 2;
}
.box-two {
  position: static;
  z-index: 1;
}
```

---

```css
.box-one {
  position: absolute;
  stack-order: 1;
}
.box-two {
  position: absolute;
  stack-order: 2;
}
```

---

```css
.box-one {
  float: left;
  z-index: 1;
}
.box-two {
  float: left;
  z-index: 2;
}
```

#### --answer--

```css
.box-one {
  position: absolute;
  z-index: 1;
}
.box-two {
  position: absolute;
  z-index: 2;
}
```

### --question--

#### --text--
Za šta se ``z-index`` svojstvo koristi u CSS-u?
#### --distractors--
Postavlja nivo zumiranja stranice.

---

Kontroliše horizontalno poravnanje elemenata unutar flex kontejnera.

---

Definiše razmak između sadržaja elementa i njegove ivice.
#### --answer--
Kontroliše vertikalni redosled složenih pozicioniranih elemenata koji se preklapaju.
### --question--

#### --text--
Kada se `top: 10%;` primeni na element sa `position: fixed;`, u odnosu na šta je izračunano `10%`?
#### --distractors--
Visina samog elementa.

---

Visina njegovog roditeljskog kontejnera.

---

Širina vidokruga (viewport)
#### --answer--
Visina prozora gledišta.
### --question--

#### --text--
Koji od kod primera predstavlja pravilnu upotrebu svojstva ``z-index`` za postavljanje prekrivanja iznad drugog sadržaja?
#### --distractors--

```css
.overlay {
  z-index: 5;
  background-color: black;
}
```

---

```css
.overlay {
  display: block;
  z-layer: 1;
  background-color: black;
}
```

---

```css
.overlay {
  float: left;
  z-index: 2;
  background-color: black;
}
```

#### --answer--

```css
.overlay {
  position: absolute;
  z-index: 10;
  background-color: black;
}
```

### --question--

#### --text--
Koje CSS svojstvo se koristi za kontrolisanje da li treba elementu da bude pozicioniran ispod plutajućih elemenata?
#### --distractors--

`float`

---

`overflow`

---

`display`

#### --answer--

`clear`

### --question--

#### --text--
Kako će se element sa `position: relative;` i `bottom: 25px;` pomeriti?
#### --distractors--
Ono će se pomeriti za 25px nadole od svoje normalne pozicije.

---

Pomeriće se za 25px u odnosu na svoju normalnu poziciju.

---

Pozicioniraće se 25 piksela od dna prozora (viewport-a).
#### --answer--
Ono će se pomeriti za 25px više od svoje normalne pozicije.
### --question--

#### --text--
Svojstvo ``z-index`` će uticati samo na elemente koji imaju koje CSS svojstvo primenjeno?
#### --distractors--
Vrednost `float` različita od `none`.

---

Vrednost `display` od `inline-block`.

---

Jedan ``background-color`` skup.
#### --answer--
Vrednost `position` različita od `static`.
### --question--

#### --text--
Koji bi bio efekat primene `float: right;` na logo u zaglavlju?
#### --distractors--
Logo bi bio poravnat desno, ali bi ostao u normalnom protoku dokumenta, sprečavajući da se drugi sadržaj prelapa.

---

Logo bi trebalo da bude izvučen iz protoka i pozicioniran sa desne strane celog vidljivog dela pregledača (viewport), a ne njegovog kontejnera.

---

Logotip bi postao blokelement koji zauzima punu širinu zaglavlja, guranje drugih elemenata ispod sebe.
#### --answer--
Logo bi bilo uklonjeno iz svog normalnog toka i postavljeno na desnu stranu svog kontejnera, pri čemu će drugi sadržaj okruživati njega.
### --question--

#### --text--
Koji CSS kod će zadržati element fiksiran na vrhu vidokruga (viewport) nakon skrolovanja?
#### --distractors--

```css
.header {
  position: fixed;
  top: 0;
}
```

---

```css
.header {
  position: relative;
  top: 0;
}
```

---

```css
.header {
  position: absolute;
  top: 0;
}
```

#### --answer--

```css
.header {
  position: sticky;
  top: 0;
}
```

### --question--

#### --text--
Koja je specifična svrha `clear: both;` u CSS-u?
#### --distractors--
Poništava svojstvo `float` na samom elementu, vraćajući ga u normalan tok dokumenta.

---

Uklanja sve `clear` svojstva koja su nasleđena od roditeljskog elementa, obnavljajući podrazumevano ponašanje float-ovanja.

---

Čisti samo plovene elemente koji su desno postavljeni, omogućavajući da elementi sa levog dela ostanu nepromenjeni.
#### --answer--
Ovo osigurava da je element pomeren ispod svih plutajućih elemenata koji se pojavljuju pre njega, kako sa leve, tako i sa desne strane.
### --question--

#### --text--
S obziма na sledeći kod, kako će biti pozicioniran `.child`?

```css
.parent {
  /* No position property set */
  height: 200px;
}
.child {
  position: absolute;
  top: 10px;
}
```

#### --distractors--
Biće pozicionirano 10px od vrha elementa `.parent`, jer je pozicioniranje `absolute` uvek relativno u odnosu na direktnog roditelja.

---

Ostaće na svojoj podrazumevanoj statičkoj poziciji jer vrednost `absolute` je nevažeća bez svojstva `z-index`.

---

Biće pozicionirano 10px od vrha prozora pregledača, ostajući fiksirano na mestu čak i kada korisnik skroluje stranicu.
#### --answer--
Biće pozicionirano 10px od vrha početnog sadržajnog bloka, kao što je `<body>`, jer njegov roditelj nije pozicioniran.
### --question--

#### --text--
Koji će uticaj sledeći CSS imati na element `.box`?

```css
.box {
  position: absolute;
  top: 50px;
  left: 50px;
}
```

#### --distractors--
Element će ostati u svom normalnom protoku, ali će biti uvuknut za 50px od vrha i sa leve strane, guranje druge elemente dalje.

---

Element će biti fiksiran na *viewport* i ostati 50px od vrha i 50px od leve strane, čak i kada se stranica skroluje.

---

Element će biti pozicioniran relativno u odnosu na svoju početnu tačku, pomerajući se za 50px nadole i 50px udesno bez uticaja na tok dokumenta.
#### --answer--
Element će biti izvučen iz normalnog protoka i pozicioniran 50px od vrha i 50px od leve strane svog najbližeg predaka sa definisanom pozicijom.
### --question--

#### --text--
Koja od sledećih vrednosti `position` potpuno uklanja element iz normalnog toka dokumenta?
#### --distractors--

`position: static;`

---

`position: relative;`

---

`position: inherit;`

#### --answer--

`position: absolute;`

### --question--

#### --text--
S obziма da imate element `.parent` i element `.child`, koji će CSS isječak pravilno pozicionirati `.child` na 20px od gornjeg levog ugla elementa `.parent`?
#### --distractors--

```css
.parent {
  /* position: static; by default */
}
.child {
  position: absolute;
  top: 20px;
  left: 20px;
}
```

---

```css
.parent {
  position: relative;
}
.child {
  position: relative;
  top: 20px;
  left: 20px;
}
```

---

```css
.parent {
  position: relative;
}
.child {
  float: left;
  top: 20px;
  left: 20px;
}
```

#### --answer--

```css
.parent {
  position: relative;
}
.child {
  position: absolute;
  top: 20px;
  left: 20px;
}
```

### --question--

#### --text--
Koja je razlika između `static` i `relative` pozicioniranja?
#### --distractors--
``static`` pozicioniranje uklanja element iz protoka dokumenta, dok ``relative`` pozicioniranje zadržava element u toku.

---

Element sa `position: static;` može biti pomeren pomoću svojstava `top` i `left`, dok to za `position: relative;` nije moguće.

---

``static` positioning je za elemente na nivou bloka, dok je ``relative`` pozicioniranje namenjeno samo ugradnim elementima.`
#### --answer--
Oboje zadržavaju element u normalnom protoku dokumenta, ali `relative` omogućava da se element pomeri sa svoje originalne pozicije.
### --question--

#### --text--
Koji CSS kodčić pravilno postavlja (float-uje) sliku na lijevo, omogućavajući ostalom sadržaju da se oko nje savija?
#### --distractors--

```css
.image {
  position: absolute;
  left: 0;
}
```

---

```css
.image {
  display: inline-block;
}
```

---

```css
.image {
  text-align: left;
}
```

#### --answer--

```css
.image {
  float: left;
}
```

### --question--

#### --text--
Koja je razlika između `absolute` i `fixed` pozicioniranja?
#### --distractors--
``absolute`` pozicioniranje je relativno u odnosu na viewport, dok je ``fixed`` pozicioniranje relativno u odnosu na najbližeg pozicioniranog predaka.

---

Pozicioniranje ``absolute`` zadržava element u normalnom protoku dokumenta, dok pozicioniranje ``fixed`` ga uklanja iz tog protoka.

---

Oba su pozicionirana relativno na *viewport*, ali elementi sa ``fixed`` će se pomerati zajedno sa stranicom, dok elementi sa ``absolute`` neće.
#### --answer--
`absolute` pozicioniranje je relativno u odnosu na najbližeg pozicioniranog predaka, dok `fixed` pozicioniranje je relativno u odnosu na prozor pregledača.
### --question--

#### --text--
Koja `position` vrednost postavlja element u normalan tok dokumenta i sprečava da svojstva pomaka, kao što su `top` i `left`, imaju bilo kakav uticaj?
#### --distractors--

`position: relative;`

---

`position: absolute;`

---

`position: fixed;`

#### --answer--

`position: static;`

