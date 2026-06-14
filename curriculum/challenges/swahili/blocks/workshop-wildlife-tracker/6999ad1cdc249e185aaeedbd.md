---
id: 6999ad1cdc249e185aaeedbd
title: Korak 8
challengeType: 1
dashedName: step-8
---

# --description--

U ovom koraku, kreiraćete funkciju koja dodaje novo svojstvo objektu.

Evo primera dodavanja svojstva unutar funkcije:

```js
const cat = {
  species: "Cat"
};

const addColor = (pet, color) => {
  pet.color = color; // add new property using dot notation
  return pet; // return the updated object
}

console.log(addColor(cat, "White")); 
// {
//   species: 'Cat',
//   color: 'White'
// }
```

U ovom primeru, svojstvo `color` dodaje se objektu `cat`.

Sada kreirajte funkciju nazvanu `addHabitat`. Funkcija treba da primi dva parametra: `animal` i `habitat`.

Unutar funkcije, dodajte novo svojstvo nazvano `habitat` objektu `animal`. Postavite mu vrednost jednaku parametru `habitat`.

Vratite ažurirani objekt `animal`.

Nakon kreiranja funkcije, koristite `console.log` da pozovete `addHabitat(tiger, "Rainforest")`, kako biste videli ažurirani objekt `tiger` u konzoli.

# --hints--

You should create a function named `addHabitat`.

```js
assert.isFunction(addHabitat);
```

The `addHabitat` function should have two parameters: `animal` and `habitat`.

```js
const regex = __helpers.functionRegex('addHabitat', ['animal', 'habitat']);
assert.match(__helpers.removeJSComments(code), regex);
```

`addHabitat` should use dot notation to add the `habitat` property.

```js
assert.match(code, /animal\.habitat\s*=\s*habitat/);
```

The `addHabitat` function should return the updated `animal` object.

```js
const testAnimal = { species: "Cat" };
const result = addHabitat(testAnimal, "Forest");
assert.strictEqual(result, testAnimal);
```

You should log `addHabitat(tiger, "Rainforest")` to the console.

```js
assert.match(
  code,
  /console\s*\.\s*log\s*\(\s*addHabitat\s*\(\s*tiger\s*,\s*["']Rainforest["']\s*\)\s*\)/
);
```

Calling `addHabitat(tiger, "Rainforest")` should add a habitat property to tiger.

```js
const updatedTiger = addHabitat(tiger, "Rainforest");

assert.deepEqual(updatedTiger, {
  species: "Tiger",
  age: 5,
  isEndangered: true,
  habitat: "Rainforest"
});
```

`addHabitat` should use the function parameters and work with any object.

```js
const lion = { species: "Lion" };
const updatedLion = addHabitat(lion, "Savanna");

assert.strictEqual(updatedLion.habitat, "Savanna");
```

# --seed--

## --seed-contents--

```js
const tiger = {
  species: "Tiger",
  age: 5,
  isEndangered: true
};

const elephant = {
  species: "Elephant",
  age: 10,
  isEndangered: true
};

const getSpecies = (animal) => {
  return animal.species;
};

console.log(getSpecies(tiger));

const getAge = (animal) => {
  return animal.age;
};

console.log(getAge(tiger));

--fcc-editable-region--

--fcc-editable-region--
```
