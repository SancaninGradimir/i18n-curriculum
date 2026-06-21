id: bd7178d8c242eddfaeb5bd13
title: Prikazivanje podataka pomoću scatter plot grafikona
challengeType: 3
forumTopicId: 301467
dashedName: visualize-data-with-a-scatterplot-graph
---

# --description--

**Cilj:** Napravite aplikaciju koja funkcioniše kao ovo: <a href="https://scatterplot-graph.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://scatterplot-graph.freecodecamp.rocks</a>.

Popunite korisničke priče ispod i prođite sve testove. Koristite bilo koju biblioteku ili API koji vam je potreban. Dajte svoj lični stil.

Možete koristiti HTML, JavaScript, CSS i SVG biblioteku za vizualizaciju D3. Testovi zahtevaju da se osi (axes) kreiraju korišćenjem D3 axis svojstva, što automatski stvara oznake (ticks) duž ose. Ove oznake su potrebne za prolazak D3 testova jer se njihove pozicije koriste za određivanje usklađenosti elemenata na grafikonu. Pronađićete informacije o tome kako napraviti ose na <https://d3js.org/d3-axis>. Potrebni DOM elementi se traže tokom svakog testa. Ako koristite framework za prednji deo (npr. Vue), rezultati testova mogu biti netačni za dinamički sadržaj. Očekujemo da ćemo ovo uskoro podržavati, ali ovi sistemi trenutno ne podržavaju D3 projekte.

**Korisnička priča #1:** Vidim element naslova sa `id="title"` koji odgovara.

**Korisnička priča #2:** Vidim x osu sa `id="x-axis"` koja odgovara.

**Korisnička priča #3:** Vidim y osu sa `id="y-axis"` koja odgovara.

**Korisnička priča #4:** Vidim tačke, svaka sa klasom `dot`, koje predstavljaju prikazane podatke.

**Korisnička priča #5:** Svaka tačka mora imati atribute `data-xvalue` i `data-yvalue` koji odgovaraju njenim vrednostima x i y.

**Korisnička priča #6:** `data-xvalue` i `data-yvalue` svake tačke moraju biti unutar opsega stvarnih podataka i u ispravnom formatu podataka. Za `data-xvalue`, prihvatljivi su celobrojni brojevi (pune godine) ili `Date` objekti za evaluaciju testa. Za `data-yvalue` (minute), koristite `Date` objekte.

**Korisnička priča #7:** `data-xvalue` i njegova tačka moraju odgovarati odgovarajućoj poziciji/vrednosti na x osi.

**Korisnička priča #8:** `data-yvalue` i njegova tačka moraju odgovarati odgovarajućoj poziciji/vrednosti na y osi.

**Korisnička priča #9:** Vidim više oznaka za ticke na y osi u formatu vremena `%M:%S`.

**Korisnička priča #10:** Vidim više oznaka za ticke na x osi koje prikazuju godinu.

**Korisnička priča #11:** Vidim da je opseg oznaka x ose unutar opsega stvarnih podataka x ose.

**Korisnička priča #12:** Vidim da je opseg oznaka y ose unutar opsega stvarnih podataka y ose.

**Korisnička priča #13:** Vidim legendu sa tekstualnim opisom sa `id="legend"`.

**Korisnička priča #14:** Mogu preći mišem preko područja i videti tooltip sa `id="tooltip"` koji prikazuje više informacija o tom području.

**Korisnička priča #15:** Moj tooltip mora imati atribut `data-year` koji odgovara `data-xvalue` radnog područja.

Ovo je set podataka koji ćete želeti za završetak ovog projekta: `https://raw.githubusercontent.com/freeCodeCamp/ProjectReferenceData/master/cyclist-data.json`

Možete izgraditi svoj projekat koristeći <a href='https://codepen.io/pen?template=MJjpwO' target="_blank" rel="noopener noreferrer nofollow">ovu CodePen šablon</a> i kliknuti na `Save` da kreirate sopstvenu Pen. Ili možete koristiti ovaj CDN link za pokretanje testova u bilo kom okruženju koje preferirate: `https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js`

Kada završite, dostavite URL vašeg funkcionalnog projekta sa svim prođene testovima.

# --solutions--

```js
// solution required
```