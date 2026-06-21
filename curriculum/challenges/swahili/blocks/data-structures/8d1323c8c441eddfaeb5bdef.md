id: 8d1323c8c441eddfaeb5bdef
title: Kreiraj klasu za skupove
challengeType: 1
forumTopicId: 301632
dashedName: create-a-set-class
---

# --description--

U ovom vežbama ćemo kreirati klasu objekata nazvanu `Set` koja imitira apstraktni tip podataka poznat kao "skup". Skup je poput niza podataka, ali ne može sadržavati ponovljene vrednosti. Uobičajena upotreba skupa je samo proveravanje prisutnosti elementa. Možemo videti kako ES6 `Set` radi na primeru ispod:

```js
const set1 = new Set([1, 2, 3, 5, 5, 2, 0]);
console.log(set1);
// output: {1, 2, 3, 5, 0}
console.log(set1.has(1));
// output: true
console.log(set1.has(6));
// output: false
```

Prvo, kreiraćemo metodu `add` koja dodaje vrednost u naš skup ako ta vrednost još nije prisutna u skupu. Zatim ćemo kreirati metodu `remove` koja uklanja vrednost iz skupa ako je već tu. I na kraju, kreiraćemo metodu `size` koja vraća broj elemenata unutar skupa.

# --instructions--

Kreirajte metodu `add` koja dodaje jedinstvenu vrednost u skup i vraća `true` ako je vrednost uspešno dodata i `false` inače.

Kreirajte metodu `remove` koja prima vrednost i proverava da li je prisutna u skupu. Ako jeste, ova metoda bi trebalo da je ukloni iz skupa i vrati `true`. Inače, bi trebalo da vrati `false`. Kreirajte metodu `size` koja vraća veličinu (broj elemenata) skupa.

# --hints--

Vaša klasa `Set` treba da ima metodu `add`.

```js
assert(
  (function () {
    var test = new Set();
    return typeof test.add === 'function';
  })()
);
```

Metoda `add` ne bi trebalo da dodaje ponovljive vrednosti.

```js
assert(
  (function () {
    var test = new Set();
    test.add('a');
    test.add('b');
    test.add('a');
    var vals = test.values();
    return vals[0] === 'a' && vals[1] === 'b' && vals.length === 2;
  })()
);
```

Metoda `add` bi trebalo da vrati `true` kada se vrednost uspešno doda.

```js
assert(
  (function () {
    var test = new Set();
    var result = test.add('a');
    return result != undefined && result === true;
  })()
);
```

Metoda `add` bi trebalo da vrati `false` kada se dodaje ponovljiva vrednost.

```js
assert(
  (function () {
    var test = new Set();
    test.add('a');
    var result = test.add('a');
    return result != undefined && result === false;
  })()
);
```

Vaša klasa `Set` treba da ima metodu `remove`.

```js
assert(
  (function () {
    var test = new Set();
    return typeof test.remove === 'function';
  })()
);
```

Metoda `remove` bi trebalo da uklanja samo elemente koji postoje u skupu.

```js
assert.deepEqual(
  (function () {
    var test = new Set();
    test.add('a');
    test.add('b');
    test.remove('c');
    return test.values();
  })(),
  ['a', 'b']
);
```

Metoda `remove` bi trebalo da ukloni element koji je uklonjen iz skupa.

```js
assert(
  (function () {
    var test = new Set();
    test.add('a');
    test.add('b');
    test.remove('a');
    var vals = test.values();
    return vals[0] === 'b' && vals.length === 1;
  })()
);
```

Vaša klasa `Set` treba da ima metodu `size`.

```js
assert(
  (function () {
    var test = new Set();
    return typeof test.size === 'function';
  })()
);
```

Metoda `size` bi trebalo da vrati veličinu kolekcije.

```js
assert(
  (function () {
    var test = new Set();
    test.add('a');
    test.add('b');
    test.remove('a');
    return test.size() === 1;
  })()
);
```

# --seed--

## --seed-contents--

```js
class Set {
  constructor() {
    // Dictionary will hold the items of our set
    this.dictionary = {};
    this.length = 0;
  }

  // This method will check for the presence of an element and return true or false
  has(element) {
    return this.dictionary[element] !== undefined;
  }

  // This method will return all the values in the set
  values() {
    return Object.values(this.dictionary);
  }

  // Only change code below this line
  
  // Only change code above this line
}
```

# --solutions--

```js
class Set {
  constructor() {
    this.dictionary = {};
    this.length = 0;
  }

  has(element) {
    return this.dictionary[element] !== undefined;
  }

  values() {
    return Object.values(this.dictionary);
  }

  add(element) {
    if (!this.has(element)) {
      this.dictionary[element] = element;
      this.length++;
      return true;
    }

    return false;
  }

  remove(element) {
    if (this.has(element)) {
      delete this.dictionary[element];
      this.length--;
      return true;
    }

    return false;
  }

  size() {
    return this.length;
  }
}
```