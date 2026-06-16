---
id: 66edc31c44f1b9c1d5c5ebca
title: JavaScript Stringovi Quiz
challengeType: 8
dashedName: quiz-javascript-strings
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 18 od 20 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koja je povratna vrednost za metodu `includes()`?
#### --distractors--
Ako se podstring pronađe unutar stringa, metoda vraća taj string. U suprotnom, vraća `undefined`.

---

Ako se podstring pronađe unutar stringa, metoda vraća ``true``. U suprotnom, vraća prazan string.

---

Ako se podstring pronađe unutar stringa, metoda vraća taj string. Inače, vraća `null`.
#### --answer--
Ukoliko se podstring pronađe unutar stringa, metoda vraća ``true``. Inače, vraća ``false``.
### --question--

#### --text--
Koja opcija demonstrira interpolaciju stringa?
#### --distractors--

`"Hello, " + user + "!"`

---

`"Hello, $user!"`

---

`` `Zdravo, {user}!` ``
#### --answer--
`` `Zdravo, ${user}!` ``
### --question--

#### --text--
Koji od sledećih opcija predstavlja karakter znaka novog reda?
#### --distractors--

`\newline`

---

`\new`

---

`\line`

#### --answer--

`\n`

### --question--

#### --text--
Koji od sledećih tvrdnji je tačan za stringove?
#### --distractors--
Stringovi su mutabilni i mogu se promeniti nakon kreiranja.

---

Stringovi su neprimitivni tipovi podataka.

---

Stringove se mogu kreirati samo korišćenjem jednolinečnih navodnika.
#### --answer--
Stringovi su nepromenljivi.
### --question--

#### --text--
Šta predstavlja ASCII?
#### --distractors--
Američki standardni kod za internet informacije

---

Napredni Sistematski Kod za Internu Razmenu

---

Automatski standardni kod za interne informacije
#### --answer--
Kod američkog standarda za razmenu informacija
### --question--

#### --text--
Koja od sledećih metoda ekstrahuje deo niza karaktera (string) i vraća novi niz karaktera?
#### --distractors--

`trim()`

---

`indexOf()`

---

`prompt()`

#### --answer--

`slice()`

### --question--

#### --text--
Koja je svrha metode `prompt()`?
#### --distractors--
Prikazuje poruku u konzoli.

---

Prikazuje dijalog kutiju sa porukom.

---

Prikazuje prozor za potvrdu sa porukom.
#### --answer--
Prikazuje dijalog okvir koji čeka na unos korisnika.
### --question--

#### --text--
Koji od sledećih je tačan način za pristup trećem karakteru niza?
#### --distractors--

```js
const developer = "Jessica";
developer[3];
```

---

```js
const developer = "Jessica";
developer[-1];
```

---

```js
const developer = "Jessica";
developer[0];
```

#### --answer--

```js
const developer = "Jessica";
developer[2];
```

### --question--

#### --text--
Kako možete dobiti ASCII vrednost prvog karaktera u stringu `"hello"`?
#### --distractors--

`"hello".charCode(0)`

---

`"hello".codeAt(0)`

---

`"hello".getCharIndex(0)`

#### --answer--

`"hello".charCodeAt(0)`

### --question--

#### --text--
Koja metoda se koristi za dobijanje karaktera koji odgovara ASCII vrednosti?
#### --distractors--

`toASCII()`

---

`toChar()`

---

`toCode()`

#### --answer--

`fromCharCode()`

### --question--

#### --text--
Koji od sledećih primera `indexOf` će logovati `-1` u konzolu?
#### --distractors--

```js
const organization = "freeCodeCamp";
console.log(organization.indexOf("e"));
```

---

```js
const organization = "freeCodeCamp";
console.log(organization.indexOf("f"));
```

---

```js
const organization = "freeCodeCamp";
console.log(organization.indexOf("C"));
```

#### --answer--

```js
const organization = "freeCodeCamp";
console.log(organization.indexOf("c"));
```

### --question--

#### --text--
Kako možete proveriti da li string ``"JavaScript"`` sadrži ``"Script"``?
#### --distractors--

`"JavaScript".has("Script")`

---

`"JavaScript".contains("Script")`

---

`"JavaScript".exists("Script")`

#### --answer--

`"JavaScript".includes("Script")`

### --question--

#### --text--
Koji od sledećih izvlači podstring `"Script"` iz stringa `"JavaScript"`?
#### --distractors--

`"JavaScript".find(5)`

---

`"JavaScript".extract(4)`

---

`"JavaScript".cut(5)`

#### --answer--

`"JavaScript".slice(4)`

### --question--

#### --text--
Kako konvertujete string `"JavaScript"` u veliko slovo?
#### --distractors--

`"JavaScript".upper()`

---

`"JavaScript".toUpper()`

---

`"JavaScript".convertUpper()`

#### --answer--

`"JavaScript".toUpperCase()`

### --question--

#### --text--
Kako konvertujete string `"JavaScript"` u mala slova?
#### --distractors--

`"JavaScript".lower()`

---

`"JavaScript".toLower()`

---

`"JavaScript".convertLower()`

#### --answer--

`"JavaScript".toLowerCase()`

### --question--

#### --text--
Koji od sledećih će zameniti `"dogs"` sa `"cats"` u stringu `"I love dogs"`.
#### --distractors--

`"I love dogs".slice("dogs", "cats")`

---

`"I love dogs".replaceWith("dogs", "cats")`

---

`"I love dogs".find("dogs", "cats")`

#### --answer--

`"I love dogs".replace("dogs", "cats")`

### --question--

#### --text--
Koji metod se koristi za ponavljanje string-a određeni broj puta?
#### --distractors--

`times()`

---

`repeatTimes()`

---

`repeatNumber()`

#### --answer--

`repeat()`

### --question--

#### --text--
Šta će sledeći kod vratiti: `"abc".repeat(3)`?
#### --distractors--

`"abcabc"`

---

`"abcabcabcabc"`

---

Izbacće grešku.
#### --answer--

`"abcabcabc"`

### --question--

#### --text--
Koji metod će ukloniti razmake sa početka i kraja stringa?
#### --distractors--

`strip()`

---

`removeWhitespace()`

---

`trimWhitespace()`

#### --answer--

`trim()`

### --question--

#### --text--
Koja od sledećih opcija predstavlja ispravnu sintaksu za bekovanje navodnika?
#### --distractors--

```js
"She said, ?"Hello!?""
```

---

```js
"She said, ."Hello!.""
```

---

```js
"She said, //"Hello!//""
```

#### --answer--

```js
"She said, \"Hello!\""
```

