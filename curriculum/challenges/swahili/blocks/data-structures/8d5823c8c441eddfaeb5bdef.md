id: 8d5823c8c441eddfaeb5bdef
title: Kreiraj strukturu podataka mape
challengeType: 1
forumTopicId: 301629
dashedName: create-a-map-data-structure
---

# --description--

Sljedeće izazove će se baviti mapama i hash tabelama. Mapa je struktura podataka koja čuva parove ključ-vrednost. U JavaScriptu, dostupne su nam kao objekti. Mapa pruža brći pristup pohranjenim podacima na osnovu vrednosti ključa i predstavlja veoma koristan i često korišćenski struktur podataka.

# --instructions--

Hajde da započnemo vežbanje kreiranja sopstvene mape. Pošto JavaScript objekti pružaju efikasniji model mape od bilo čega što možemo napisati ovde, ovo je više namenjeno kao vežba u učenju. Međutim, JavaScript objekti nam daju samo neke operacije. Da li bismo želeli da definišemo specifične operacije? Koristite `Map` klasu dataženu ovde kao omot (wrapper) za JavaScript `object`. Kreirajte sledeće metode i operacije na Map objektu:

<ul>
<li><code>add</code> prima par <code>ključ, vrednost</code> za dodavanje u mapu.</li>
<li><code>remove</code> prima ključ i briše povezani par <code>ključ, vrednost</code></li>
<li><code>get</code> prima <code>ključ</code> i vraća sačuvanu <code>vrednost</code></li>
<li><code>has</code> prima <code>ključ</code> i vraća <dfn>true</dfn> ako ključ postoji ili <dfn>false</dfn> ako ne postoji.</li>
<li><code>values</code> vraća niz svih vrednosti sadržanih u mapi</li>
<li><code>size</code> vraća broj elemenata u mapi</li>
<li><code>clear</code> briše celu mapu</li>
</ul>

# --hints--

Struktura podataka `Map` mora postojati.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    return typeof test == 'object';
  })()
);
```

Map objekat mora imati sledeće metode: `add`, `remove`, `get`, `has`, `values`, `clear` i `size`.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    return (
      typeof test.add == 'function' &&
      typeof test.remove == 'function' &&
      typeof test.get == 'function' &&
      typeof test.has == 'function' &&
      typeof test.values == 'function' &&
      typeof test.clear == 'function' &&
      typeof test.size == 'function'
    );
  })()
);
```

Metoda `add` mora dodati elemente u mapu.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    test.add(5, 6);
    test.add(2, 3);
    test.add(2, 5);
    return test.size() == 2;
  })()
);
```

Metoda `has` mora vratiti `true` za dodate elemente i `false` za nepostojeće.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    test.add('test', 'value');
    return test.has('test') && !test.has('false');
  })()
);
```

Metoda `get` mora primiti ključ kao ulaz i vratiti odgovarajuću vrednost.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    test.add('abc', 'def');
    return test.get('abc') == 'def';
  })()
);
```

Metoda `values` mora vratiti sve vrednosti sačuvane u mapi kao niz karaktera u nizu podataka.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    test.add('a', 'b');
    test.add('c', 'd');
    test.add('e', 'f');
    var vals = test.values();
    return (
      vals.indexOf('b') != -1 &&
      vals.indexOf('d') != -1 &&
      vals.indexOf('f') != -1
    );
  })()
);
```

Metoda `clear` mora obrisati mapu, a metoda `size` mora vratiti broj elemenata u mapi.

```js
assert(
  (function () {
    var test = false;
    if (typeof Map !== 'undefined') {
      test = new Map();
    }
    test.add('b', 'b');
    test.add('c', 'd');
    test.remove('asdfas');
    var init = test.size();
    test.clear();
    return init == 2 && test.size() == 0;
  })()
);
```

# --seed--

## --seed-contents--

```js
var Map = function() {
  this.collection = {};
  // Only change code below this line
  
  // Only change code above this line
};
```

# --solutions--

```js
var Map = function() {
    this.collection = {};
    // Only change code below this line

    this.add = function(key,value) {
      this.collection[key] = value;
    }

    this.remove = function(key) {
      delete this.collection[key];
    }

    this.get = function(key) {
      return this.collection[key];
    }

    this.has = function(key) {
      return this.collection.hasOwnProperty(key)
    }

    this.values = function() {
      return Object.values(this.collection);
    }

    this.size = function() {
      return Object.keys(this.collection).length;
    }

    this.clear = function() {
      for(let item of Object.keys(this.collection)) {
        delete this.collection[item];
      }
    }
    // Only change code above this line
};
```