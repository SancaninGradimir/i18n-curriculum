---
id: 695cc8f280fef0cc3bed02cc
title: Šta je Stream modul i kako funkcioniše?
challengeType: 19
dashedName: what-is-the-stream-module-and-how-does-it-work
---

# --description--

Poslednji osnovni Node.js modul na koji ćemo pogledati je `stream`. Ovaj modul vam pomaže da efikasno rukujete podacima, posebno kada su podaci preveliki za učitavanje svih odjednom, kao što je čitanje velike tekstualne datoteke ili preuzimanje velikog videa.

Umesto čekanja da se pročita ili napiše sve podatke pre nego što se bilo šta uradi, streamovi obrađuju delove podataka kako dolaze, slično tome kako možete početi gledati YouTube video pre nego što ceo video završi učitavanje.

Postoje četiri glavne vrste streamova u Node.js-u: čitljivi (readable), upisivi (writable), dupleksni (duplex) i transform (transform):

- Čitljivi tokovi vam omogućavaju da čitate podatke u paketima (na primer, čitanje velikog fajla).
- Upisivi tokovi vam omogućavaju da pišete podatke u paketima (na primer, čuvanje fajla).
- Dupleks tokovi mogu da čitaju i pišu podatke.
- Transformacioni tokovi su poseban tip dupleks tokova koji mogu da menjaju ili obrađuju podatke dok prolaze kroz njih.

Možete uvesti klase streama koje vam trebaju dekonstruišući ih iz modula streama:

```js
const { Readable, Writable, Transform } = require("stream");
```

U većini slučajeva, ne morate sami kreirati prilagođene stream klase. Za svakodnevne operacije sa fajlovima, ugrađene metode kao što su `fs.createReadStream()` i `fs.createWriteStream()` obično su sve što vam treba.

Ova dva metoda uzimaju putanju fajla za čitanje ili pisanje. To znači da vam takođe trebaju moduli `fs` i `path` za implementaciju striminga u mnogim prilikama.

Evo kako možete da pročitate podatke iz fajla, recimo fajl sa `input.txt`:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");

// Readable stream
const readInputFileStream = fs.createReadStream(inputFilePath);
console.log(readInputFileStream);
```

Ovo neće ništa učiniti još, jer morate koristiti događaje iz streama da biste pročitali podatke. Na primer, možete slušati događaj `data` na ovaj način:

```js
readInputFileStream.on("data", (chunk) => {
  console.log(`Received ${chunk.length} bytes of data`);
}); // Received 622 bytes of data
```

Takođe možete logovati blok podataka u konzolu:

```js
readInputFileStream.on("data", (chunk) => {
  console.log(`Received ${chunk.length} bytes of data`);
  console.log("Received data:", chunk);
});

/*
Received 622 bytes of data
Received data: <Buffer 4c 6f 72 65 6d 20 69 70 73 75 6d 
20 64 6f 6c 6f 72 20 73 69 74 20 61 6d 65 74 20 63 6f 6e
73 65 63 74 65 74 75 72 20 61 64 69 70 69 73 69 63 69 6e 67 ... 572 more bytes>
*/
```

Pošto vraća buffer, možete pozvati metodu `toString()` da ga pretvorite u čitljiv tekst:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");

// Readable stream
const readInputFileStream = fs.createReadStream(inputFilePath);

readInputFileStream.on("data", (chunk) => {
  console.log(`Received ${chunk.length} bytes of data`);
  console.log("Received data:", chunk.toString());
});
/*
Received 622 bytes of data
Received data: Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus sint facilis
aliquid. Odio voluptatibus veniam saepe consectetur alias modi non fuga in,
tempore explicabo numquam maiores quod inventore quibusdam! Nam cumque repellat
facere voluptatem nulla aliquam atque ratione numquam ea aperiam porro ducimus
animi tempora laboriosam, labore quae voluptatum? Nam, hic quas dolore
repudiandae placeat eius! Voluptate reiciendis totam hic expedita tenetur. Nisi
ipsa ad facere optio sint debitis. Magni nostrum sit ipsa saepe suscipit facilis
eaque doloribus assumenda, minima fuga tempore, porro, debitis rem harum in
*/
```

Da biste implementirali upisivi tok, posebno kada čitate iz jednog fajla i pišete u drugi, morate prvo kreirati tok za čitanje, a zatim i tok za pisanje:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");
const outputFilePath = path.join(__dirname, "output.txt");

// Create the read stream first
const readInputFileStream = fs.createReadStream(inputFilePath);

// Create the write stream
const writeOutputFileStream = fs.createWriteStream(outputFilePath);
```

Zatim, koristite metod `.pipe()` za povezivanje čitljivog streama sa upisivim streamom. Ovo omogućava da Node.js automatski pročita podatke iz izvora i napiše ih na odredište, deo po deo:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");
const outputFilePath = path.join(__dirname, "output.txt");

// Create the read stream first
const readInputFileStream = fs.createReadStream(inputFilePath);

// Create the write stream
const writeOutputFileStream = fs.createWriteStream(outputFilePath);

// Pipe the read stream to the write stream
readInputFileStream.pipe(writeOutputFileStream);
```

Zatim možete slušati događaje `finish` i `error` na upisni tok da znate kada je striming završen ili ako nešto pođe po zlu:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");
const outputFilePath = path.join(__dirname, "output.txt");

// Create the read stream first
const readInputFileStream = fs.createReadStream(inputFilePath);

// Create the write stream
const writeOutputFileStream = fs.createWriteStream(outputFilePath);

readInputFileStream.pipe(writeOutputFileStream);

writeOutputFileStream.on("finish", () => {
  console.log("All data has been written to the file");
});

writeOutputFileStream.on("error", (err) => {
  console.error("Error writing to file:", err);
});
```

Događaj `finish` vam govori da je tok završen i da nema više podataka za pisanje, dok događaj greške pomaže u hvatanju problema koji se mogu desiti tokom pisanja, poput problema sa dozvolama ili nedostajućih direktorijuma.
# --questions--

## --text--

Koje su ovo četiri glavne vrste potoka?
## --answers--

Tokovi zahteva, odgovora, događaja i grešaka.
### --feedback--

Razmislite o tome kako Node.js obrađuje čitanje, pisanje i transformisanje podataka.
---

Readable, Editable, Duplex, and Transform streams.

### --feedback--

Razmislite o tome kako Node.js obrađuje čitanje, pisanje i transformisanje podataka.
---

Data, File, HTTP, and Buffer streams.

### --feedback--

Razmislite o tome kako Node.js obrađuje čitanje, pisanje i transformisanje podataka.
---

Readable, Writable, Duplex, and Transform streams.

## --video-solution--

4

## --text--

Šta vam omogućava da implementirate prilagođeni čitljiv i upisiv tok (stream)?
## --answers--

Modul `stream` koji koristi klase Readable i Writable.
---

The `http` module.

### --feedback--

Razmislite o modulu koji pruža osnovne klase za kreiranje prilagođenih streamova.
---

The `fs` module using `createReadStream()` and `createWriteStream()`.

### --feedback--

Razmislite o tome kako Node.js obrađuje čitanje, pisanje i transformisanje podataka.
---

The events module.

### --feedback--

Razmislite o tome kako Node.js obrađuje čitanje, pisanje i transformisanje podataka.
## --video-solution--

1

## --text--

Koje događaje možete koristiti na upisivi stream da znate kada striming završi ili kada dođe do greške?
## --answers--

`end` i `close`.
### --feedback--

Razmislite o događajima upisivog streama koji signaliziraju završetak i neuspeh.
---

`finish` and `error`.

---

`start` and `stop`.

### --feedback--

Razmislite o događajima upisivog streama koji signaliziraju završetak i neuspeh.
---

`done` and `fail`.

### --feedback--

Razmislite o događajima upisivog streama koji signaliziraju završetak i neuspeh.
## --video-solution--

2
