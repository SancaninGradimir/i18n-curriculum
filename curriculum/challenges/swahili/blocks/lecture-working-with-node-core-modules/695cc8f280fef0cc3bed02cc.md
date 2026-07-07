---
id: 695cc8f280fef0cc3bed02cc
title: Moduli ya stream ni nini na inafanya kazi vipi?
challengeType: 19
dashedName: what-is-the-stream-module-and-how-does-it-work
---

# --description--

Najnoviji osnovni modul za Node.js koji proučavamo je `stream`. Ovaj modul vam pomaže da efikasno rukujete podacima, posebno kada su podaci preveliki za čitanje odjednom, kao što je čitanje velike tekstualne datoteke ili preuzimanje velikog videa.

Umesto da čekaš da pročitaš ili napišeš sve podatke pre nego što uradiš bilo šta, streamovi obrađuju delove dolaznih podataka, kao što možeš da počneš gledati YouTube video pre nego što je celokupan video završen sa učitavanjem.

Postoje četiri glavna tipa streamova u Node.js: čitljivi (readable), upisivi (writable), dupleksni (duplex) i transform (transform):

- Readable streams hukuruhusu kusoma data kwa vipande (kwa mfano, kusoma faili kubwa).
- Writable streams hukuruhusu kuandika data kwa vipande (kwa mfano, kuhifadhi faili).
- Duplex streams zinaweza kusoma na kuandika data.
- Transform streams ni aina maalum ya duplex stream inayoweza kubadilisha au kuchakata data inavyopita.

Unaweza import madarasa ya stream unayohitaji kwa kuyafumbua kutoka moduli ya stream:

```js
const { Readable, Writable, Transform } = require("stream");
```

Mara nyingi, huna haja ya kuunda madarasa ya stream maalum mwenyewe. Kwa shughuli za kawaida za faili, njia zilizojengwa ndani kama `fs.createReadStream()` na `fs.createWriteStream()` kawaida ndizo unazohitaji.

Njia hizi mbili zinachukua njia ya faili kusoma au kuandika. Hii inamaanisha pia unahitaji moduli za `fs` na `path` kutekeleza streaming mara nyingi.

Evo kako možete čitati podatke iz fajla, na primer iz fajla `input.txt`:

```js
const fs = require("fs");
const path = require("path");

const inputFilePath = path.join(__dirname, "input.txt");

// Readable stream
const readInputFileStream = fs.createReadStream(inputFilePath);
console.log(readInputFileStream);
```

Hii bado haitafanya chochote, kwa sababu unahitaji kutumia matukio kutoka kwa stream kusoma data. Kwa mfano, unaweza kusikiliza tukio la `data` kwa njia hii:

```js
readInputFileStream.on("data", (chunk) => {
  console.log(`Received ${chunk.length} bytes of data`);
}); // Received 622 bytes of data
```

Pia unaweza kuandika kipande cha data kwenye konsoli:

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

Kwa kuwa inarudisha kihifadhi cha muda, unaweza kuita njia ya `toString()` kuibadilisha kuwa maandishi yanayosomwa:

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

Da biste implementirali writable stream, posebno kada čitate iz jednog fajla i pišete u drugi, morate prvo kreirati read stream, a zatim write stream:

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

Zatim, koristi metod `.pipe()` za povezivanje *readable stream*-a i *writable stream*-a. Ovo omogućava Node.js da čita podatke iz izvora i piše ih na odredište, deo po deo:

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

Kasnije možete pratiti događaje za `finish` i `error` na writable streamu da biste znali kada je striming završen ili da li postoji problem:

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

Događaj `finish` vam govori da je stream završen i da nema više podataka za pisanje, dok vas događaj greške pomaže da otkrijete probleme koji mogu nastati tokom zapisa, kao što su problemi sa dozvolom ili nedostajućim direktorijumima.

# --questions--

## --text--

Da li su ovo četiri glavna tipa streamova?

## --answers--

Streamovi za Request, Response, Event, i Error.

### --feedback--

Zamislite kako Node.js obrađuje čitanje, pisanje i modifikovanje podataka.

[No Swahili text provided.]

Streamovi za Readable, Editable, Duplex i Transform.

### --feedback--

Razmislite kako Node.js obrađuje čitanje, pisanje i modifikovanje podataka.

[No Swahili text provided.]

Streamovi za Podatke, Datoteke, HTTP, u Buffer.

### --feedback--

Zamislite kako Node.js obrađuje čitanje, pisanje i modifikovanje podataka.

[No Swahili text provided.]

Streamovi za Readable, Writable, Duplex i Transform.

## --video-solution--

4

## --text--

Šta omogućava implementaciju specifičnog streama koji je čitljiv i upisan/zapisiv?

## --answers--

Moduli `stream` koristeći Readable i Writable klase.

[No Swahili text provided.]

Moduli ya `http`.

### --feedback--

Fikiria moduli inayotoa madarasa ya msingi kwa kuunda streams maalum.

[No Swahili text provided.]

Moduli `fs` koristeći `createReadStream()` i `createWriteStream()`.

### --feedback--

Zamislite kako Node.js obrađuje čitanje, pisanje i modifikovanje podataka.

[No Swahili text provided.]

Modul događaja.

### --feedback--

Zamislite kako Node.js obrađuje čitanje, pisanje i modifikovanje podataka.

## --video-solution--

1

## --text--

Ni matukio gani unaweza kutumia kwenye writable stream kujua wakati streaming imekamilika au tatizo limetokea?

## --answers--

`end` na `close`.

### --feedback--

Fikiria matukio ya writable stream yanayoashiria kukamilika na kushindwa.

[No Swahili text provided.]

`finish` na `error`.

[No Swahili text provided.]

`start` na `stop`.

### --feedback--

Razmislite o događajima *writable stream*-a koji signaliziraju završetak i neuspeh.

[No Swahili text provided.]

`done` i `fail`.

### --feedback--

Razmislite o događajima *writable stream*-a koji signaliziraju završetak i neuspeh.

## --video-solution--

2