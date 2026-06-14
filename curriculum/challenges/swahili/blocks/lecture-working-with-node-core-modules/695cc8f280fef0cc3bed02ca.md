---
id: 695cc8f280fef0cc3bed02ca
title: Šta je Path modul i kako radi?
challengeType: 19
dashedName: what-is-the-path-module-and-how-does-it-work
---

# --description--

Modul Node.js `path` vam omogućava da radite sa fajlovima i putanjama direktorijuma. Pruža nekoliko korisnih metoda za rukovanje i transformisanje direktorijuma, uključujući spajanje, normalizovanje i rešavanje direktorijuma na različitim platformama i operativnim sistemima.

Da biste koristili modul `path`, možete ga uvesti na ovaj način:

```js
const path = require("path");
```

Pogledajmo neke od metoda koje pruža modul `path` i kako funkcionišu.

Prvo, trebalo bi da znate za Node.js globalne varijable `__filename` i `__dirname`, poznate kao "common JS" varijable. Ne trebate `path` modul da biste im pristupili, zbog čega se nazivaju globalne varijable.

`__filename` je apsolutni put do trenutne datoteke, a `__dirname` je apsolutni put do direktorijuma koji sadrži trenutnu datoteku.

Na primer, imam fajl `script.js` na kojem trenutno radim. Evo šta vraćaju dve metode:

```js
console.log(__filename);
// /Users/user/Desktop/fCC/script-code/node/node-path/script.js

console.log(__dirname);
// /Users/user/Desktop/fCC/script-code/node/node-path
```

Takođe biste trebalo da znate o relativnim i apsolutnim putanjama.

Relativna putanja ukazuje na fajl ili direktorijum zasnovan na vašem trenutnom radnom direktorijumu. Na primer, `./assets/src/text-files`.

Apsolutna putanja, s druge strane, daje potpunu adresu fajla ili foldera od korena vašeg sistema, kao što je `/Users/johndoe/projects/app/assets/src/text-files.`

``basename()`` metoda prikazuje poslednji deo fajla, što je ime fajla:

```js
console.log(path.basename(__filename)); // script.js
```

`dirname()` vraća naziv direktorijuma puta:

```js
console.log(path.dirname(__dirname)); // node-path
```

`extname()` vraća ekstenziju trenutne datoteke:

```js
console.log(path.extname(__filename)); // .js
```

Takođe možete navesti različitu datoteku za vraćanje ekstenzije:

```js
console.log(path.extname('text-files/text1.txt')); // .txt
```

Metoda ``join()`` uzima sve segmente puta koje prosledite i spaja ih u jednu čistu, normalizovanu putanju.

Ovo bi moglo biti korisno ako želite da spojite povezane fajlove u različitim folderima kako biste mogli da radite sa njima zajedno:

```js
const joinedPath = path.join("src", "assets", "text-files");
console.log(joinedPath); // src/assets/text-files
```

Windows koristi povratne kosove da razdvoji direktorijume, pa će rezultat biti `src\assets\text-files`.

Pored toga, metoda `join()` automatski popravlja pogrešne kose crte i uklanja višak:

```js
const wrongPath = path.join("/src//", "assets", "text-files");
console.log(wrongPath); // /src/assets/text-files
```

Metoda ``resolve()`` pretvara sekvencu segmenata puta u apsolutni put. Kreće se od vašeg trenutnog radnog direktorijuma i rezultira punim putem koji ukazuje na tačnu lokaciju na uređaju:

```js
const absolutePath = path.resolve("assets", "src", "text-files");
console.log(absolutePath);
// /Users/user/Desktop/fCC/script-code/node/node-path/assets/src/text-files
```

Razlika između ``join()`` i ``resolve()`` je u tome što ``join()`` kreira relativnu putanju, dok ``resolve()`` vraća apsolutnu putanju.

Konačno, postoje `parse()` i `format()` metode.

`parse()` uzima direktorijum ili fajl i vraća objekat koji sadrži razlaganje njegovih delova, kao što su sistemski koren, njegov direktorijum, ekstenzija i ime fajla:

```js
const parsedFile = path.parse(__filename);

console.log(parsedFile);
/*
{
 root: '/',
 dir: '/Users/user/Desktop/fCC/script-code/node/node-path',
 base: 'script.js',
 ext: '.js',
 name: 'script'
}
*/
```

`format()`, s druge strane, kreira putanju iz objekta koji sadrži direktorijum, ime i ekstenziju:

```js
const formattedDirectory = path.format({
  dir: "/users/johndoe/docs",
  name: "file",
  ext: ".txt",
});

console.log(formattedDirectory); // /users/johndoe/docs/file.txt
```

# --questions--

## --text--

Koja je razlika između `path.dirname()` i `path.extname()` u Node.js-u?
## --answers--

`dirname()` uklanja ekstenziju fajla, dok `extname()` uklanja naziv direktorijuma.
### --feedback--

Obratite pažnju na koji se od njih bavi direktorijumima, a koji ekstenzijama fajlova.
---

`dirname()` returns the full file path, while `extname()` returns the directory name.

### --feedback--

Obratite pažnju na koji se od njih bavi direktorijumima, a koji ekstenzijama fajlova.
---

`dirname()` returns the directory name of a path, while `extname()` returns the file's extension.

---

`dirname()` and `extname()` both return the same value but in different formats.

### --feedback--

Obratite pažnju na koji se od njih bavi direktorijumima, a koji ekstenzijama fajlova.
## --video-solution--

3

## --text--

Koji metod ``path`` gradi kompletan putanju fajla iz objekta koji sadrži svojstva direktorijuma, imena i ekstenzije?
## --answers--

`path.parse()`

### --feedback--

Razmislite o tome šta je suprotnost `parse()`.
---

`path.format()`

---

`path.resolve()`

### --feedback--

Razmislite o tome šta je suprotnost `parse()`.
---

`path.join()`

### --feedback--

Razmislite o tome šta je suprotnost `parse()`.
## --video-solution--

2

## --text--

Na šta globalne varijable Node.js ``__filename`` i ``__dirname`` pružaju pristup?
## --answers--

Apsolutna putanja trenutne datoteke i njenog sadržajnog direktorijuma.
---

The name of the current module and its dependencies.

### --feedback--

Razmislite o varijablama koje vam automatski daju pune putanje do fajlova i foldera bez korišćenja `path` modula.
---

The relative path to the Node.js installation directory.

### --feedback--

Razmislite o varijablama koje vam automatski daju pune putanje do fajlova i foldera bez korišćenja `path` modula.
---

The URL of the running web server and its hostname.

### --feedback--

Razmislite o varijablama koje vam automatski daju pune putanje do fajlova i foldera bez korišćenja `path` modula.
## --video-solution--

1
