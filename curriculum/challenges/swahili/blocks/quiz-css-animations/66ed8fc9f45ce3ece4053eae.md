---
id: 66ed8fc9f45ce3ece4053eae
title: CSS Animations Quiz
challengeType: 8
dashedName: quiz-css-animations
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koja je svrha svojstva ``transform`` u CSS?
#### --distractors--
Promena vidljivosti elementa.

---

Primena vizuelnog efekta na tekst.

---

Postavljanje dimenzija elementa.
#### --answer--
Modifikovanje pozicije, veličine i oblika elementa.
### --question--

#### --text--
Kako CSS svojstvo ``animation-direction`` utiče na animaciju?
#### --distractors--
Određuje da li će animacija biti ponovljena.

---

Ono određuje trajanje animacije.

---

Definiše brzinu animacije.
#### --answer--
Određuje kako animacija treba da radi.
### --question--

#### --text--
Koje CSS svojstvo čini da se animacija pokrene 3 puta?
#### --distractors--

`animation-repeat: 3`

---

`animation-loop: 3`

---

`animation-delay: 3`

#### --answer--

`animation-iteration-count: 3`

### --question--

#### --text--
Koja CSS timing funkcija omogućava da se animacija izvrši konstantnom brzinom od početka do kraja?
#### --distractors--

`ease`

---

`ease-in`

---

`ease-in-out`

#### --answer--

`linear`

### --question--

#### --text--
Šta at-pravilo ``@keyframes`` definiše u CSS?
#### --distractors--
Boje CSS gradijenta.

---

Ugle za CSS rotaciju.

---

Dimenzije elementa.
#### --answer--
Faze CSS animacije.
### --question--

#### --text--
Koja je svrha funkcije `translateX()` u CSS-u?
#### --distractors--
Menja opacitet elementa.

---

Rotira element.

---

Ponovno pozicionira element vertikalno.
#### --answer--
Ponovo pozicionira element horizontalno.
### --question--

#### --text--
Koja od sledećih NIJE potencijalna briga kod CSS animacija?
#### --distractors--
Mogu izazvati nelagodu ili fizičku štetu kod određenih korisnika.

---

Korisnici ih mogu smatrati ometajućim.

---

Prekomerna upotreba može dovesti do loših performansi.
#### --answer--
Mogu poboljšati korisničko iskustvo.
### --question--

#### --text--
Gde je definisan at-regel `@keyframes`?
#### --distractors--
Unutar elementa `body` u HTML fajlu.

---

Unutar elementa ``head`` u HTML fajlu.

---

Unutar definicije CSS klase.
#### --answer--
Na najvišem nivou, izvan bilo kojeg CSS selektora.
### --question--

#### --text--
Koji CSS atribut vam omogućava da pauzirate i ponovite animaciju?
#### --distractors--

`animation-timing-function`

---

`animation-delay`

---

`animation-direction`

#### --answer--

`animation-play-state`

### --question--

#### --text--
Koja vrednost bi trebalo dodeliti svojstvu `animation-name` u CSS-u?
#### --distractors--
Trajanje animacije u sekundama.

---

Funkcija za određivanje vremena koja se koristi za animaciju.

---

Kašnjenje pre nego što animacija počne, u sekundama.
#### --answer--
Ime animacije koje je definisano pomoću `@keyframes`.
### --question--

#### --text--
Šta ova ``@keyframe`` direktiva čini animiranom elementu?

```css
@keyframes animation {
  0% {
    transform: translateX(-50px);
  }
  100% {
    transform: translateX(100px);
  }
}
```

#### --distractors--
Rotira element za 90 stepeni u smeru kazaljke na satu.

---

Menja boju elementa u plavu.

---

Skalira element na 50% njegove početne veličine, a zatim i na 100% njegove početne veličine.
#### --answer--
Element se horizontalno pomera od -50px do 100px, relativno na svoju početnu tačku.
### --question--

#### --text--
Koje CSS svojstvo definiše kako animacija napreduje tokom vremena?
#### --distractors--

`animation-delay`

---

`animation-fill-mode`

---

`animation-iteration-count`

#### --answer--

`animation-timing-function`

### --question--

#### --text--
Koje CSS svojstvo se koristi za određivanje da animacija treba da traje 5 sekundi?
#### --distractors--

```css
animation-name: 5s;
```

---

```css
animation-delay: 5s;
```

---

```css
animation-timing-function: 5s;
```

#### --answer--

```css
animation-duration: 5s;
```

### --question--

#### --text--
Šta predstavlja `50%` u sledećoj CSS direktivi `@keyframe`?

```css
@keyframes animation {
  0% {
    transform: translateX(-50px);
  }
  50% {
    transform: translateX(25px);
  }
  100% {
    transform: translateX(100px);
  }
}
```

#### --distractors--
Početna tačka animacije.

---

Tačka završetka animacije.

---

Brzina animacije.
#### --answer--
Sredina animacije.
### --question--

#### --text--
Šta će se desiti kada se svojstvo ``transform: translateX(200px);`` primeni?
#### --distractors--
Element će se pomeriti za 200px ulevo.

---

Element će se pomeriti za 200px nadole.

---

Element će se rotirati za 200 stepeni u smeru po godini kazaljke.
#### --answer--
Element će se pomeriti za 200px udesno.
### --question--

#### --text--
Kako će animacija se ponašati ako `animation-iteration-count` je podešen na `infinite`?
#### --distractors--
Radiće samo jednom i zaustaviće se.

---

Pauzirati će se nakon prve iteracije.

---

Zaustaviće se nakon tri iteracije.
#### --answer--
Ponovo će se ponavljati neograničeno.
### --question--

#### --text--
Koji `@keyframes` selektor određuje početnu tačku animacije?
#### --distractors--

`50%`

---

`25%`

---

`100%`

#### --answer--

`0%`

### --question--

#### --text--
Koja svojstva mogu se definisati korišćenjem skraćenog CSS svojstva `animation`?
#### --distractors--
Samo ime animacije.

---

Ime i trajanje animacije.

---

Ime, trajanje i kašnjenje animacije.
#### --answer--
Sve svojstva animacije.
### --question--

#### --text--
Koje CSS svojstvo se koristi za primenu animacije definisane sa ``@keyframes`` at-pravilom?
#### --distractors--

`animation-duration`

---

`apply`

---

`translate`

#### --answer--

`animation`

### --question--

#### --text--
Koji CSS atribut vam omogućava da postavite vreme pre nego što animacija počne?
#### --distractors--

`animation-fill-mode`

---

`animation-timing-function`

---

`animation-iteration-count`

#### --answer--

`animation-delay`

## --quiz--

### --question--

#### --text--
Šta radi svojstvo CSS `animation-delay`?
#### --distractors--
Postavlja koliko dugo animacija traje.

---

Definiše funkciju za određivanje vremena.

---

Definiše pravac animacije.
#### --answer--
Odlaže početak animacije.
### --question--

#### --text--
Koje svojstvo animacije određuje kako će se element stilizovati pre i posle animacije?
#### --distractors--

`animation-delay`

---

`animation-direction`

---

`animation-iteration-count`

#### --answer--

`animation-fill-mode`

### --question--

#### --text--
Zašto bi se CSS animacije trebalo koristiti umereno?
#### --distractors--
Previše CSS animacija može dovesti do toga da se stili pokvare, kao i da budu nekonzistentni u različitim pretraživačima.

---

Previše CSS animacija može dovesti do nižeg ili nepostojećeg rangiranja u rezultatima pretrage.

---

Previše CSS animacija može automatski da sruši server i povećati rizik od sigurnosnih problema.
#### --answer--
Previše CSS animacija može dovesti do loših performansi i može biti odvraćajuće ili problematično za korisnike sa određenim potrebama pristupačnosti.
### --question--

#### --text--
Koje svojstvo animacije određuje da li će animacija biti reprodukovana napred, unazad ili alternativno?
#### --distractors--

`animation-fill-mode`

---

`animation-delay`

---

`animation-timing-function`

#### --answer--

`animation-direction`

### --question--

#### --text--
Koja CSS media query utvrđuje da li je korisnik zahtevao minimalne animacije ili efekte kretanja?
#### --distractors--

`reduce-motion`

---

`min-motion-preference`

---

`motion-preferences`

#### --answer--

`prefers-reduced-motion`

### --question--

#### --text--
Koje svojstvo određuje koliko puta se `animation` ponavlja?
#### --distractors--

`animation-duration`

---

`animation-count`

---

`animation-delay`

#### --answer--

`animation-iteration-count`

### --question--

#### --text--
Koje CSS pravilo se koristi za definisanje faza i stilova animacije na različitim tačkama tokom njenog trajanja?
#### --distractors--

`@style`

---

`@transition`

---

`@transform`

#### --answer--

`@keyframes`

### --question--

#### --text--
Unutar ``reduced‑motion`` media query-ja, koja deklaracija onemogućava tranzicije?
#### --distractors--

`animation: none;`

---

`transition: remove;`

---

`animation-play-state: paused;`

#### --answer--

`transition: none;`

### --question--

#### --text--
Šta vam omogućava svojstvo ``animation-play-state``?
#### --distractors--
Postavite koliko puta se animacija ponavlja.

---

Odredite koliko dugo će animacija trajati do završetka.

---

Utvrdite smer u kojem se animacija reprodukuje.
#### --answer--
Pauzirajte i nastavite animaciju.
### --question--

#### --text--
Koja je dobra praksa prilikom rada sa animacijama?
#### --distractors--
Koristite što je moguće više treperajućih boja i brzih pokreta da biste privukli pažnju.

---

Izbegavajte testiranje animacija na različitim uređajima ili veličinama ekrana.

---

Povećajte trajanje animacija koliko god je moguće kako biste osigurali da ih korisnici primețe.
#### --answer--
Izbegavajte sadržaj koji treperi više od tri puta u sekundi kako biste sprečili izazivanje napada ili nelagodnosti.
### --question--

#### --text--
Zašto je deklaracija ``!important`` korišćena u CSS pravilima?
#### --distractors--
Da bi se sprečilo učitavanje drugih medijskih upita (media queries).

---

Da se stili ograniče na prvi element deteta.

---

Za lakše debagovanje CSS-a.
#### --answer--
Da bi se osiguralo da ova pravila imaju prioritet nad drugim stilovima.
### --question--

#### --text--
Šta `animation-iteration-count: 1 !important;` osigurava u CSS?
#### --distractors--
Animacije su pauzirane.

---

Te animacije se izvršavaju beskonačno.

---

Animacije menjaju smer tokom svakog ciklusa.
#### --answer--
Da sve animacije koje se ponavljaju (looping) prođu samo jednom.
### --question--

#### --text--
Koje CSS svojstvo se koristi za određivanje trajanja animacije?
#### --distractors--

`animation-delay`

---

`animation-timing-function`

---

`animation-iteration-count`

#### --answer--

`animation-duration`

### --question--

#### --text--
Koji atribut NIJE deo skraćenice za `animation`?
#### --distractors--

`animation-delay`

---

`animation-timing-function`

---

`animation-direction`

#### --answer--

`animation-transform`

### --question--

#### --text--
Šta definiše pravilo `@keyframes`?
#### --distractors--
Funkcija vremena animacije.

---

Podrazumevano stanje elementa.

---

Upiti medija za animacije.
#### --answer--
Sekvenca stilova u različitim tačkama animacije.
### --question--

#### --text--
Šta ova ``@keyframe`` direktiva čini animiranom elementu?

```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

#### --distractors--
Skalira element sa 0% do 100%.

---

Element se kreće iz levog udesnoga pravca.

---

Menja boju teksta u crnu.
#### --answer--
Element postaje vidljiv postupnim smanjenjem njegove prozirnosti.
### --question--

#### --text--
U pravilu keyframes-a, šta predstavlja `100%`?
#### --distractors--
Početak animacije.

---

Poluputna tačka.

---

Funkcija za ublažavanje (Easing function)
#### --answer--
Kraj animacije.
### --question--

#### --text--
Koje svojstvo kontroliše tempo `animation` tokom njegovog trajanja?
#### --distractors--

`animation-duration`

---

`animation-delay`

---

`animation-iteration-count`

#### --answer--

`animation-timing-function`

### --question--

#### --text--
Šta bi razvojnici trebalo da razmotre prilikom implementacije animacija kako bi održali pristupačnost?
#### --distractors--
Koristite isključivo JavaScript za sve animacije.

---

Dodajte česte i intenzivne animacije radi veće snage/uticaja.

---

Uključite samo podebljane, brze i iznenađujuće efekte.
#### --answer--
Koristite suptilne, namerne efekte, poštujte preferencije i ponudite korisničku kontrolu.
### --question--

#### --text--
Koja je ispravna sintaksa za klizanje elementa sa leve strane?
#### --distractors--

```css
@keyframes slide-in {
  0 { 
    transform: translate(-100%); 
  }
  100 { 
    transform: translate(0); 
  }
}
```

---

```css
@keyframes slide-in {
  from { 
    translateX(-100%); 
  }
  to { 
    translateX(0); 
  }
}
```

---

```css
@keyframes slide-in {
  start { 
    transform: moveX(-100%); 
  }
  end { 
    transform: moveX(0); 
  }
}
```

#### --answer--

```css
@keyframes slide-in {
  0% { 
    transform: translateX(-100%); 
  }
  100% { 
    transform: translateX(0); 
  }
}
```
