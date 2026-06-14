---
id: 67329fbcfaf5ff5cdaa38a42
title: Šta je ključna reč `var`, i zašto se više ne preporučuje njeno korišćenje?
challengeType: 19
dashedName: what-is-the-var-keyword-and-why-is-it-no-longer-suggested-to-use-it
---

# --interactive--

Ključna reč ``var`` u JavaScriptu je jedan od prvobitnih načina za deklarisanje promenljivih. Bila je deo jezika otkako je nastao i godinama je ostala primarni metod za kreiranje promenljivih. Međutim, kako je JavaScript evoluirao i programeri su stekli više iskustva sa jezikom, određeni nedostaci korišćenja ``var`` postali su vidljivi, što je dovelo do uvođenja ``let`` i ``const`` 2015. godine.

Kada deklariš varijablu sa `var`, ona postaje funkciono opsežna ili globalno opsežna. To znači da ako deklariš varijablu unutar funkcije koristeći `var`, ona je dostupna samo unutar te funkcije. Međutim, ako je deklariš izvan bilo koje funkcije, postaje globalna varijabla dostupna u celom tvom skriptu. Ovo ponašanje ponekad može dovesti do neočekivanih rezultata i učiniti vaš kod teže razumljivim.

Problem sa `var` jeste što vam omogućava da ponovo deklarišete istu varijablu više puta bez bacanja greške. Ovo može dovesti do slučajnog prepisivanja i otežati debagovanje.

:::interactive_editor

```js
var num = 5;
console.log(num); // 5

// This is allowed and doesn't throw an error
var num = 10;
console.log(num); // 10
```

:::

Najznačajniji problem sa `var` je nedostatak blok opsega. Varijable deklarisane sa `var` unutar bloka kao što je izjava `if` ili petlja `for` i dalje su dostupne van tog bloka.

:::interactive_editor

```js
if (true) {
  var num = 5;
}
console.log(num); // 5
```

:::

Ovo ponašanje može dovesti do neželjenog curenja varijabli i učiniti vaš kod sklonijim greškama.

Zbog ovih problema, moderno JavaScript razvijanje se u velikoj meri udaljilo od `var` umesto `let` i `const`. Ove ključne reči pružaju blok opsega (block scoping) što je u skladu sa načinom na koji funkcioniše opseg u mnogim drugim programskim jezicima.

Takođe ne dozvoljavaju ponovno deklarisanje unutar istog opsega, što pomaže u sprečavanju slučajnih nadjačavanja.

Iako je `var` i dalje deo JavaScript-a i radi u svim pregledačima, generalno se preporučuje korišćenje `let` i `const` u modernom JavaScript razvoju. Oni pružaju jasna pravila obima (scoping), pomažu sprečavanju uobičajenih zamki i čine ponašanje vašeg koda predvidljivijim.
# --questions--

## --text--

Koji je opseg varijable deklarisane sa `var` izvan bilo koje funkcije?
## --answers--

Blok opseg.
### --feedback--

Razmislite o tome gde se varijabla `var` deklarisana izvan funkcije može pristupiti.
---

Function scope.

### --feedback--

Razmislite o tome gde se varijabla `var` deklarisana izvan funkcije može pristupiti.
---

Global scope.

---

Module scope.

### --feedback--

Razmislite o tome gde se varijabla `var` deklarisana izvan funkcije može pristupiti.
## --video-solution--

3

## --text--

Koji će biti izlaz sledećeg koda?

```js
var x = 10;

if (true) {
  var x = 20;
  console.log(x);
}

console.log(x);
```

## --answers--

```js
10
10
```

### --feedback--

Zapamtite da ``var`` je funkciono-opsegovan ili globalno-opsegovan, i omogućava ponovno deklarisanje unutar istog opsega.
---

```js
20
20
```

---

```js
10
20
```

### --feedback--

Zapamtite da ``var`` je funkciono-opsegovan ili globalno-opsegovan, i omogućava ponovno deklarisanje unutar istog opsega.
---

```js
20
10
```

### --feedback--

Zapamtite da ``var`` je funkciono-opsegovan ili globalno-opsegovan, i omogućava ponovno deklarisanje unutar istog opsega.
## --video-solution--

2

## --text--

Koja od sledećih nije razlog za izbegavanje korišćenja `var` u modernom JavaScript-u?
## --answers--

`var` omogućava ponovno deklarisanje promenljivih u istom opsegu.
### --feedback--

Razmislite koji je tvrdnja netačna o ponašanju ili podršci '`var`'.
---

`var` is not supported in modern browsers.

---

`var` variables are function-scoped, not block-scoped.

### --feedback--

Razmislite koji je tvrdnja netačna o ponašanju ili podršci '`var`'.
---

`var` variables are hoisted.

### --feedback--

Razmislite koji je tvrdnja netačna o ponašanju ili podršci '`var`'.
## --video-solution--

2
