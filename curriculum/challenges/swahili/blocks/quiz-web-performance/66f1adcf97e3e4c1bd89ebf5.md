---
id: 66f1adcf97e3e4c1bd89ebf5
title: Web Performanse Kviz
challengeType: 8
dashedName: quiz-web-performance
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koja je ključna razlika između stvarne performanse i percipirane performanse u web razvoju?
#### --distractors--
Stvarna performansa se fokusira na broj HTTP zahteva koje pravi pretraživač, dok je percipirana performansa zasnovana na brzini renderovanja CSS-a.

---

Stvarna performansa se tiču samo vremena učitavanja, dok se percipirana performansa odnosi na vizuelne elemente kao što su animacije i indikatori učitavanja.

---

Stvarna performansa obuhvata samo vreme obrade na strani servera, dok je percipirana performansa u potpunosti na strani klijenta.
#### --answer--
Stvarna performansa je brzina učitavanja sadržaja, dok su percipirane performanse to kako korisnici veruju da se stranica učitava.
### --question--

#### --text--
Koja metrika najbolje ukazuje koliko brzo sadržaj stiže na web stranicu?
#### --distractors--
Vreme do interaktivnosti (TTI)

---

Vreme učitavanja stranice (PLT)

---

Poslednji sadržajni render (LCP)
#### --answer--
Prvi sadržajni prikaz (FCP)
### --question--

#### --text--
Koji od sledećih nije način za smanjenje vremena učitavanja stranice?
#### --distractors--
Optimizacija medijskih resursa.

---

Iskorišćavanje keširanja u pregledaču.

---

Minifikovanje i komprimovanje fajlova.
#### --answer--
Korišćenje samo JPEG fajlova.
### --question--

#### --text--
Šta je „vreme do upotrebljivosti“?
#### --distractors--
Ovo je interval od trenutka kada korisnik zahteva stranicu do trenutka kada može da interaguje sa formularima na toj stranici.

---

To je vreme koje je potrebno da se sve slike i animacije učitaju i postanu dostupne za korišćenje.

---

Ovo je vreme potrebno za učitavanje svih CSS i JavaScript animacija na ekranu.
#### --answer--
To je interval od trenutka kada korisnik traži stranicu do trenutka kada može sa njom smisleno da interaguje.
### --question--

#### --text--
Šta meri First Contentful Paint (FCP)?
#### --distractors--
Ukupno vreme učitavanja svih JavaScript datoteka na stranici.

---

Kašnjenje pre nego što korisnik može da interaguje sa bilo kojim elementima na stranici.

---

Vreme potrebno da se svi stilovi u potpunosti učitaju i primene.
#### --answer--
Vreme potrebno da se prvi deo teksta ili slike prikaže.
### --question--

#### --text--
Koji od sledećih NIJE uobičajeno korišćen alat za merenje performansi?
#### --distractors--
Chrome DevTools

---

Lighthouse

---

WebPageTest
#### --answer--
WebMerenje
### --question--

#### --text--
Za šta se koriste Performance Web APIs?
#### --distractors--
Ovo se koristi isključivo za merenje performansi CSS animacija.

---

Koristi se za automatsko ubrzanje performansi veb stranice.

---

Pruža detaljnu tabelu metrika performansi za korisnika.
#### --answer--
Omogućava programerima da prate koliko efikasno se web stranica učitava i odgovara direktno iz koda.
### --question--

#### --text--
Koja strategija može efikasno da poboljša percipiranu performansu?
#### --distractors--
Korišćenje velikih slika za poboljšanje ukupnog vizuelnog kvaliteta.

---

Učitavanje CSS stilova poslednje radi prioritizacije prikaza sadržaja.

---

Unapred preuzimanje svih skripti kako bi se osigurala njihova spremnost kada su potrebne.
#### --answer--
Prikazivanje skeleta učitavanja dok se sadržaj preuzima.
### --question--

#### --text--
Koji od sledećih se odnosi na vreme koje je potrebno da zahtev putuje između pretraživača i servera?
#### --distractors--
renderovanje

---

INP

---

CDN
#### --answer--
latencija
### --question--

#### --text--
Kako optimizovanje CSS-a utiče na performanse stranice?
#### --distractors--
To sprečava pretraživač od izvršavanja nepotrebnog JavaScript-a.

---

Smanjuje ukupnu veličinu fajlova slika.

---

Uklanja potrebu za opuštenim učitavanjem slika.
#### --answer--
Ubrzava parsiranje HTML-a.
### --question--

#### --text--
Koji od sledećih pokazuje koliko dugo je glavni konac blokiran teškim JavaScript zadacima?
#### --distractors--
Izvorni redosled

---

Stopa odbijanja

---

WebPageTest
#### --answer--
Ukupno vreme blokiranja
### --question--

#### --text--
Prilikom merenja Interaction to Next Paint (INP), šta se procenjuje?
#### --distractors--
Vreme potrebno da stranica u potpunosti učita sve stilove i slike nakon interakcije korisnika.

---

Kašnjenje između interakcije korisnika i sposobnosti pregledača da registruje sledeći unos korisnika.

---

Interval između izvršavanja JavaScript-a i osvežavanja sadržaja stranice u pretraživaču.
#### --answer--
Vreme koje teče između interakcije korisnika i odgovora pretraživača, koji renderuje sledeći kadar.
### --question--

#### --text--
Koji od sledećih API-ja pruža vremenske oznake visoke preciznosti (u milisekundama) za merenje koliko dugo različiti delovi vašeg sajta traže za učitavanje?
#### --distractors--

`performance.delay()`

---

`performance.previous()`

---

`performance.next()`

#### --answer--

`performance.now()`

### --question--

#### --text--
Koji od sledećih API-ja pruža detaljan pregled svakog koraka učitavanja stranice, od DNS upita do `DOMContentLoaded`?
#### --distractors--
API za dozvolu određivanja vremena

---

Performanse Tekst API

---

Izvršite Timing API
#### --answer--
**API za merenje vremena performansi**
### --question--

#### --text--
Koji od sledećih prati performansne događaje, kao što su pomeranja rasporeda (layout shifts), dugi zadaci i interakcije korisnika?
#### --distractors--

```js
const observer = new PermitObserve((list) => {  
  list.getEntries().forEach((entry) => {  
    console.log(`Long task detected: ${entry.duration}ms`);  
  });  
});  

observer.observe({ type: "longtask", buffered: true });
```

---

```js
const observer = new PerformObserver((list) => {  
  list.getEntries().forEach((entry) => {  
    console.log(`Long task detected: ${entry.duration}ms`);  
  });  
});  

observer.observe({ type: "longtask", buffered: true });
```

---

```js
const observer = new PermitObserver((list) => {  
  list.getEntries().forEach((entry) => {  
    console.log(`Long task detected: ${entry.duration}ms`);  
  });  
});  

observer.observe({ type: "longtask", buffered: true });
```

#### --answer--

```js
const observer = new PerformanceObserver((list) => {  
  list.getEntries().forEach((entry) => {  
    console.log(`Long task detected: ${entry.duration}ms`);  
  });  
});  

observer.observe({ type: "longtask", buffered: true });
```

### --question--

#### --text--
Kako leno učitavanje slika poboljšava performanse stranice?
#### --distractors--
Obezbeđuje da se sve slike učitaju odmah za bolje korisničko iskustvo.

---

Smanjuje veličinu slika radi bržeg učitavanja.

---

Predmemorira slike kako bi sprečio bilo kakva kašnjenja prilikom učitavanja.
#### --answer--
Odlaže učitavanje nebitnih slika sve dok ih korisnik ne vidi (ili: dok dođu u vidokrug).
### --question--

#### --text--
Šta je *code splitting*?
#### --distractors--
Uključuje podelu vašeg React koda na module koji obavljaju samo ključne zadatke.

---

Uključuje razdvajanje vašeg HTML koda na module koji obavljaju samo nekritične zadatke.

---

Uključuje razdvajanje vašeg CSS koda u module koji obavljaju kritične i nekritične zadatke/funkcije.
#### --answer--
Uključuje podelu vašeg JavaScript koda na module koji obavljaju kritične i nekritične zadatke.
### --question--

#### --text--
Koji od sledećih načina je ispravan za opušteno učitavanje slike?
#### --distractors--

```html
<img src="placeholder.jpg" lazy="loading">
```

---

```html
<img src="placeholder.jpg" load="lazy">
```

---

```html
<img src="placeholder.jpg" lazy="load">
```

#### --answer--

```html
<img src="placeholder.jpg" loading="lazy">
```

### --question--

#### --text--
Koja od sledećih NIJE način za poboljšanje INP?
#### --distractors--
Smanjenje opterećenja glavnog niti tako što se dugački JavaScript zadaci dele na manje delove.

---

Optimizacija rukovaoca događaja.

---

Odlaganje ili lenjo učitavanje teških resursa.
#### --answer--
Korišćenje samo PNG i JPEG slika.
### --question--

#### --text--
Zašto je energetska efikasnost ključni aspekt web performansi?
#### --distractors--
Ono poboljšava opšti vizuelni izgled web stranice.

---

Minimizira količinu JavaScripta korišćenog na web stranici.

---

Smanjuje broj potrebnih CSS fajlova i čini da vaš CSS radi brže.
#### --answer--
Smanjuje opterećenje hardvera, štedeći energiju i poboljšavajući održivost.

