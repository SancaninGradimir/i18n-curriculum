id: bd7168d8c242eddfaeb5bd13
title: Prikazivanje podataka pomoću bar grafikona
challengeType: 3
forumTopicId: 301464
dashedName: visualize-data-with-a-bar-chart
---

# --description--

**Cilj:** Izgradite aplikaciju koja funkcionalno odgovara ovom: <a href="https://bar-chart.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://bar-chart.freecodecamp.rocks</a>.

Popunite korisničke priče ispod i prođite sve testove. Možete koristiti bilo koju biblioteku ili API koji vam je potreban. Dodajte svoj lični stil.

Možete koristiti HTML, JavaScript, CSS i D3 SVG vizualizacijsku biblioteku. Testovi zahtevaju da se osa kreira korišćenjem D3 axis atributa, što automatski generiše tačke (ticks) duž ose. Ove tačke su neophodne za prolaz testova D3 jer se njihove pozicije koriste za određivanje skalarnosti elemenata na grafikonu. Informacije o kreiranju osa možete pronaći na <https://d3js.org/d3-axis>. DOM elementi koji su potrebni traže se tokom svakog testa. Ako koristite framework funkcionisanja (kao što je Vue), rezultati testova mogu biti nepouzdani za dinamički sadržaj. Nadamo se da ćemo ovo uskoro podržati, ali ovi sistemi trenutno ne podržavaju D3 projekte.

**Korisnička priča #1:** Moj grafikon treba da ima naslov sa `id="title"` koji odgovara.

**Korisnička priča #2:** Moj grafikon treba da ima element `g` za x-osu sa `id="x-axis"` koji odgovara.

**Korisnička priča #3:** Moj grafikon treba da ima element `g` za y-osu sa `id="y-axis"` koji odgovara.

**Korisnička priča #4:** Obje ose moraju imati više tačaka (ticks), svaka sa odgovarajućim `class="tick"`.

**Korisnička priča #5:** Moj grafikon treba da ima element `rect` za svaku tačku podataka sa `class="bar"` koja prikazuje te podatke.

**Korisnička priča #6:** Svaki `.bar` mora imati atribute `data-date` i `data-gdp` sa vrednostima datuma i BDP-a.

**Korisnička priča #7:** Atributi `.bar` za elemente `data-date` moraju odgovarati redosledu podataka koji se izvlače.

**Korisnička priča #8:** Atributi `.bar` za elemente `data-gdp` moraju odgovarati redosledu podataka koji se izvlače.

**Korisnička priča #9:** Svaki element `.bar` mora imati visinu koja tačno predstavlja BDP podatke.

**Korisnička priča #10:** Atribut `data-date` i njegov element `.bar` moraju biti povezani sa odgovarajućom vrednošću na x-osi.

**Korisnička priča #11:** Atribut `data-gdp` i njegov element `.bar` moraju biti povezani sa odgovarajućom vrednošću na y-osi.

**Korisnička priča #12:** Treba mi da pređem mišem preko područja i vidim tooltip vremenske oznake sa `id="tooltip"` koji prikazuje više informacija o tom području.

**Korisnička priča #13:** Moj tooltip mora imati atribut `data-date` koji odgovara `data-date` aktivnog područja.

Ovo je set podataka koji ćete trebati za završetak ovog projekta: `https://raw.githubusercontent.com/freeCodeCamp/ProjectReferenceData/master/GDP-data.json`

Možete izgraditi svoj projekat korišćenjem ovog CodePen šablona <a href='https://codepen.io/pen?template=MJjpwO' target="_blank" rel="noopener noreferrer nofollow"></a> i kliknuti na `Save` da kreirate svoj Pen. Ili možete koristiti ovaj CDN link za pokretanje testova u bilo okruženju koje preferirate: `https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js`.

Kada završite, dostavite URL vašeg funkcionalnog projekta sa prođetim svim testovima.

# --solutions--

```js
// solution required
```