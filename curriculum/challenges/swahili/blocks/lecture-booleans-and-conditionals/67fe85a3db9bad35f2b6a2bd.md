---
id: 67fe85a3db9bad35f2b6a2bd
title: Kako funkcionišu uslovne izjave i logički operateri?
challengeType: 19
dashedName: how-do-conditional-statements-and-logical-operators-work
---

# --description--

Uslovne izjave, ili kondicionali, omogućavaju vam da kontrolišete tok vašeg programa na osnovu toga da li su određeni uslovi istiniti ili netačni.

Ali pre nego što uđemo u sve to, hajde da pregledamo osnovne građevinske blokove uslovnih izjava, počevši od operatora poređenja. Operatori poređenja su operateri koji vam omogućavaju da uporedite dve ili više vrednosti i vraćaju booleanski (boolean) vrednost.

U prethodnoj lekciji ste naučili da su booleani jedan od tipova podataka u Pythonu i mogu biti samo `True` ili `False`.

Evo tabele sa operatorima poređenja u Pythonu:


# --questions--

## --text--

Šta rade operatori poređenja?
## --answers--

Izvršite matematičke proračune sa booleovim vrednostima
### --feedback--

Ovi operateri proveravaju stvari kao što su jednakost ili koja je vrednost veća, a rezultat je ili `True` ili `False`.
---

Convert strings to boolean values.

### --feedback--

Ovi operateri proveravaju stvari kao što su jednakost ili koja je vrednost veća, a rezultat je ili `True` ili `False`.
---

Compare two values and return a boolean value.

---

Create loops and iterations.

### --feedback--

Ovi operateri proveravaju stvari kao što su jednakost ili koja je vrednost veća, a rezultat je ili `True` ili `False`.
## --video-solution--

3

## --text--

Koji će biti rezultat za sledeći kod?

```python
age = 12

if age >= 18:
    print('You are an adult')
elif age >= 13:
    print('You are a teenager')
else:
    print('You are a child') 
```

## --answers--

`You are an adult` će biti odštampano na konzolu.
### --feedback--

Pregledajte poslednji deo lekcije za tačan odgovor.
---

`You are a teenager` will be printed to the console.

### --feedback--

Pregledajte poslednji deo lekcije za tačan odgovor.
---

`You are a child` will be printed to the console.

---

An error will be printed to the console.

### --feedback--

Pregledajte poslednji deo lekcije za tačan odgovor.
## --video-solution--

3

## --text--

Na šta će izraz `3 >= 4` da se izračuna?
## --answers--

`True`

### --feedback--

3 nije veće ili jednako od 4.
---

`SyntaxError`

### --feedback--

3 nije veće ili jednako od 4.
---

`None`

### --feedback--

3 nije veće ili jednako od 4.
---

`False`

## --video-solution--

4
