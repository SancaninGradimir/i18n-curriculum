id: bd7188d8c242eddfaeb5bd13
title: Prikazivanje podataka na termičkoj mapi
challengeType: 3
forumTopicId: 301466
dashedName: visualize-data-with-a-heat-map
---

# --description--

**Cilj:** Napravite aplikaciju koja radi kao ovo: <a href="https://heat-map.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://heat-map.freecodecamp.rocks</a>.

Završite korisničke priče ispod i prođite sve testove. Koristite bilo koju biblioteku ili API koji vam je potreban. Kreirajte svoj jedinstveni stil.

Možete koristiti HTML, JavaScript, CSS i biblioteku D3 za crtanje SVG-a. Potrebni DOM elementi se traže tokom svakog testa. Ako koristite frontend framework (npr. Vue), rezultati testova mogu biti netačni za dinamički sadržaj. Očekujemo podršku uskoro, ali ovi sistemi trenutno ne podržavaju projekte sa D3.

**Korisnička priča #1:** Moja termička mapa mora imati naslov sa `id="title"` koji odgovara.

**Korisnička priča #2:** Moja termička mapa mora imati opis sa `id="description"` koji odgovara.

**Korisnička priča #3:** Moja termička mapa mora imati x-osu sa `id="x-axis"` koja odgovara.

**Korisnička priča #4:** Moja termička mapa mora imati y-osu sa `id="y-axis"` koja odgovara.

**Korisnička priča #5:** Moja termička mapa mora imati elemente `rect` sa `class="cell"` koji predstavljaju podatke.

**Korisnička priča #6:** Mora postojati najmanje 4 različite boje popunjanja za ćelije.

**Korisnička priča #7:** Svaka ćelija mora imati atribute `data-month`, `data-year`, `data-temp` sa odgovarajućim vrednostima `month`, `year` i `temperature`.

**Korisnička priča #8:** `data-month`, `data-year` svake ćelije moraju biti unutar opsega podataka.

**Korisnička priča #9:** Moja termička mapa mora imati ćelije koje odgovaraju određenom mesecu na y-osi.

**Korisnička priča #10:** Moja termička mapa mora imati ćelije koje odgovaraju određenoj godini na x-osi.

**Korisnička priča #11:** Moja termička mapa mora imati više oznaka na y-osi sa punim nazivima meseci.

**Korisnička priča #12:** Moja termička mapa mora imati više oznaka na x-osi za godine između 1754 i 2015.

**Korisnička priča #13:** Moja termička mapa mora imati legende sa `id="legend"` koji odgovara.

**Korisnička priča #14:** Moja legenda mora imati elemente `rect`.

**Korisnička priča #15:** Elementi `rect` u legendi moraju koristiti najmanje 4 različite boje popunjanja.

**Korisnička priča #16:** Mogu preći mišem preko područja i videti tooltip sa `id="tooltip"` koji prikazuje više informacija o tom području.

**Korisnička priča #17:** Moj tooltip mora imati atribut `data-year` koji odgovara `data-year` aktivnog područja.

Evo skupa podataka koje ćete želeti za završetak ovog projekta: `https://raw.githubusercontent.com/freeCodeCamp/ProjectReferenceData/master/global-temperature.json`

Možete izgraditi svoj projekat korišćenjem ovog CodePen šablona <a href='https://codepen.io/pen?template=MJjpwO' target="_blank" rel="noopener noreferrer nofollow"></a> i kliknuti na `Save` da kreirate sopstveni Pen. Ili možete koristiti ovaj CDN link za pokretanje testova u bilo okruženju koje preferirate: `https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js`

Kada završite, dostavite URL vašeg funkcionalnog projekta sa svim prođene testovima.

# --solutions--

```js
// solution required
```