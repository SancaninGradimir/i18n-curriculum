---
id: 695cc8f280fef0cc3bed02cb
title: Šta je procesni modul i kako radi?
challengeType: 19
dashedName: what-is-the-process-module-and-how-does-it-work
---

# --description--

`process` je jedan od najvažnijih modula jezgra Node.js. Daje vam pristup informacijama o trenutnom procesu Node.js, i omogućava vam da ga kontrolišete dok vaša aplikacija radi.

Kada izvršite komandu poput `node script.js` u terminalu, Node.js pokreće proces, što je pokrenata instanca programa Node koji izvršava fajl `script.js`. Ovaj proces ima svoju memoriju, okruženje i kontekst izvršenja.

Trenutni proces je globalno izložen preko modula `process`, pa ne morate čak ni da ga uvozite. Sve dok imate instaliran Node.js, možete ga pozvati bilo gde.

Modul `process` izlaže svojstva i metode da biste dobili određene informacije o trenutnom kontekstu izvršenja.

`process.env` daje vam informacije o trenutnom okručenju na kojem Node radi. Ovo uvek vraća ogroman objekat sa mnogo parametara, pa evo kako možete direktno pristupiti nekim od najvažnijih informacija:

```js
// Gets all environment variables available to the current Node.js process
console.log(process.env);

// Gets the current Node.js environment mode (like 'development' or 'production')
console.log(process.env.NODE_ENV); // development

// Gets the path of the shell program running the Node.js process
console.log(process.env.SHELL); // /bin/bash

// Gets the system PATH variable where executables are searched for
console.log(process.env.PATH); // /usr/local/bin:/usr/bin:/bin

// Gets the present working directory from where the process was started
console.log(process.env.PWD); // /Users/johndoe/projects/myapp

// Gets the username of the user running the current process
console.log(process.env.USER); // johndoe
```

`process.argv` omogućava vam da pročitate argumente komandne linije:

```js
console.log(process.argv);
/*
script.js --watch
Hello world
[
  '/Users/user/.nvm/versions/node/v22.17.0/bin/node',
  '/Users/user/Desktop/fCC/script-code/node/node-process/script.js',
  '--watch'
]
*/
```

Metoda `cwd()` prikazuje trenutni radni direktorijum:

```js
console.log(process.cwd());
```

Događaji procesa su osnovna karakteristika Node.js koja omogućava vašoj aplikaciji da reaguje na ključne trenutke u svom životnom ciklusu, poput kada je pred izlazak, naiđe na grešku ili primi sistemski signal.

Događaj `exit`, na primer, pokreće se neposredno pre nego što proces Node.js završi:

```js
process.on("exit", (code) => {
  console.log(`Process exiting with code: ${code}`);
});

// Process exiting with code: 0
```

Događaj `uncaughtException` aktivira se kada greška nije uhvaćena u vašem kodu, što vam može pomoći da sprečite padove:

```js
process.on("uncaughtException", (err) => {
  console.error("Uncaught error:", err.message);
});
```

Napokon, događaj `warning` aktivira se kada Node.js emituje upozorenje procesa:

```js
process.on("warning", (warning) => {
  console.warn("Warning name:", warning.name);
  console.warn("Warning message:", warning.message);
});
```

Zatim možete koristiti metodu `emitWarning()` da biste pokrenuli prilagođeno upozorenje:

```js
// Example warning with the emitWarning() method
process.emitWarning('This is a custom warning message', 'CustomWarning');

/*
  Warning name: CustomWarning
  Warning message: This is a custom warning message
*/
```
# --questions--

## --text--

Šta radi metoda `process.emitWarning()`?
## --answers--

Zaustavlja proces kada se pojavi prilagođeno upozorenje.
### --feedback--

Razmislite o tome kako Node.js obrađuje prilagođena upozorenja putem događaja.
---

It triggers a custom warning event that can be handled by the warning listener.

---

It logs an error and exits the process immediately.

### --feedback--

Razmislite o tome kako Node.js obrađuje prilagođena upozorenja putem događaja.
---

It restarts the Node.js process after showing a warning.

### --feedback--

Razmislite o tome kako Node.js obrađuje prilagođena upozorenja putem događaja.
## --video-solution--

2

## --text--

Kako da koristite proces modul?
## --answers--

Pozivanjem ga direktno jer je globalni objekat.
---

By enabling it in the Node.js configuration file.

### --feedback--

Razmislite o tome zašto možete pristupiti procesu bilo gde, bez podešavanja.
---

By installing it manually using npm before calling it.

### --feedback--

Razmislite o tome zašto možete pristupiti procesu bilo gde, bez podešavanja.
---

By importing it using require('process') before each use.

### --feedback--

Razmislite o tome zašto možete pristupiti procesu bilo gde, bez podešavanja.
## --video-solution--

1

## --text--

Za šta se koriste događaji procesa?
## --answers--

Za definisanje varijabli okruženja za aplikaciju.
### --feedback--

Razmislite o tome kako Node.js reaguje na promene životnog ciklusa tokom izvršavanja.
---

To create new processes for parallel execution.

### --feedback--

Razmislite o tome kako Node.js reaguje na promene životnog ciklusa tokom izvršavanja.
---

To listen for and respond to important lifecycle moments like exit, errors, or system signals.

---

To manage file paths and extensions in the system.

### --feedback--

Razmislite o tome kako Node.js reaguje na promene životnog ciklusa tokom izvršavanja.
## --video-solution--

3
