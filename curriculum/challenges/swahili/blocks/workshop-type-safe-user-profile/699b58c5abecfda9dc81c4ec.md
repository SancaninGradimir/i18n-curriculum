---
id: 699b58c5abecfda9dc81c4ec
title: Korak 3
challengeType: 1
dashedName: step-3
---

# --description--

Trenutno objekat `profile` ima samo tri svojstva. Ali bilo bi lepo imati još nekoliko.

Dodajte svojstvo nazvano `mood` objektu `profile`. Njegova vrednost bi trebalo da bude `null`.

# --hints--

Your `profile` object should have a `mood` property.

```js
assert.property(profile, "mood");
```

Your `mood` property should have a value of `null`.

```js
assert.isNull(profile?.mood);
```

# --seed--

## --seed-contents--

```ts
const profile = {
  username: "codeLearner",
  age: 25,
  isLoggedIn: false,
--fcc-editable-region--
  
--fcc-editable-region--
}

console.log(profile);
```
