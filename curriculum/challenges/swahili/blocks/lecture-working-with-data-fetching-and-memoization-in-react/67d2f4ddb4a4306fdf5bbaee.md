---
id: 67d2f4ddb4a4306fdf5bbaee
title: Šta je memoizacija i kako funkcioniše `useMemo` hook?
challengeType: 19
dashedName: what-is-memoization-and-how-does-the-usememo-hook-work
---

# --description--

Kako vaša React aplikacija raste, nepotrebni ponovni renderi i skupi proračuni mogu usporiti performanse, što dovodi do sporih ažuriranja korisničkog interfejsa i povećane potrošnje resursa.

Ovo može biti posebno problematično u aplikacijama sa kompleksnim upravljanjem stanjem, velikim listama, funkcijama koje zahtevaju te proračune i mnogim komponentama sa jedinim roditeljem.

Iz toga proizlazi potreba da optimizujete svoju React aplikaciju za bolju performansu minimalizovanjem redundantnih računanja i osiguravanjem glatkijih interakcija.

React rešava ovaj problem procesom koji se zove memorizacija, tehnikom koja kešira vrednosti i funkcije kako bi sprečila nepotrebne ponovne proračune, tako da vaša aplikacija može biti brža i reaktivnija.

Po definiciji, memoizacija je tehnika optimizacije u kojoj su rezultati skupih poziva funkcija kešovani (zapamćeni) na osnovu specifičnih argumenata. Kada se ponovo pruže isti argumenti, vraćan je kešovani rezultat umesto ponovnog izračunavanja funkcije.

Proces memorizacije se dešava na ovaj način:

- Sačuvati rezultate poziva funkcija zajedno sa njihovim ulaznim argumentima.

- Pre izvršavanja funkcije, proverite da li rezultat za trenutne argumente već postoji u kešu.

- Ako postoji, vratite keširani rezultat umesto ponovnog izvođenja proračuna.

- Ako ne postoji, izračunaj rezultat, sačuvaj ga u keš, i zatim ga vrati.

Kako bi se poboljšalo iskustvo razvoja sa memorizacijom, React pruža tri alata – `React.memo` (ili `memo`), `useMemo` i `useCallback`.

Kao što možda pogađate, oba `useMemo` i `useCallback` su hookovi, ali je `React.memo` omotač komponente, komponenta višeg reda (HOC).

U sledećoj lekciji, pogledaćemo kako se `useCallback` hook i `React.memo` funkcionišu.

`useMemo` vam omogućava da memoizujete izračunate vrednosti, dok `useCallback` radi isto i za reference funkcija.

Ako se pitate šta su izračunate vrednosti i reference na funkcije, izračunate vrednosti se odnose na rezultat izvršavanja funkcije, dok su reference na funkcije pokazivači na funkcije – objekat funkcije u memoriji.

Pogledaćemo kako da koristimo `useMemo` hak prvo. Evo osnovne sintakse `useMemo` haka:

```js
const memoizedValue = useMemo(
  function () {
    return computeExpensiveValue(a, b);
  },
  [a, b]
);
```

Možete videti da je potrebno samo obaviti hook ``useMemo`` oko funkcije.

Ovaj `ExpensiveSquare` komponenta će primiti `num` prop koji će koristiti za izračunavanje kvadrata:

```jsx
function ExpensiveSquare({ num }) {
  function calculateSquare(n) {
    console.log("Calculating square...");
    return n * n;
  }

  const squared = calculateSquare(num);
  return (
    <p>
      Square of {num}: {squared}
    </p>
  );
}
export default ExpensiveSquare;
```

Evo `App` komponente gde se koristi `ExpensiveSquare`:

```jsx
import { useState, useEffect } from "react";
import ExpensiveSquare from "./components/ExpensiveSquare";

function App() {
 const [timer, setTimer] = useState(0);
 const [num, setNum] = useState(0);

 useEffect(() => {
   const interval = setInterval(() => setTimer((c) => c + 1), 1000);
   return () => clearInterval(interval);
 }, []);

 return (
   <div>
     <h1>Timer: {timer} seconds gone</h1>
     <ExpensiveSquare num={num} />
     <button onClick={() => setNum((n) => n + 1)}>Increase Number</button>
   </div>
 );
}

export default App;
```

``timer`` u ``useEffect``, koji radi svake sekunde, naterać će funkciju ``calculateSquare`` da se pokrene svaki put kada se pokrene, čak i kada ne povećate stacionarnu varijablu ``num``.

Da bismo rešili ovaj problem, možemo da koristimo kuku ``useMemo`` tako što ćemo poziv funkcije u nju umotati i navesti varijablu ``num`` kao zavisnost:

```jsx
// import the useMemo hook
import { useMemo } from "react";

function ExpensiveSquare({ num }) {
  function calculateSquare(n) {
    console.log("Calculating square...");
    return n * n;
  }

  // const squared = calculateSquare(num);
  // Wrap the function call in useMemo instead
  const squared = useMemo(() => calculateSquare(num), [num]);

  return (
    <p>
      Square of {num}: {squared}
    </p>
  );
}

export default ExpensiveSquare;
```

Ovo će osigurati da je funkcija memorizovana keširanjem rezultata. Iako se komponenta `ExpensiveSquare` i dalje ponovo renderuje svaki put kada se stanje roditeljskog `timer` ažurira, izračunavanje `calculateSquare` se ponovo pokreće samo pri inicijalnom renderovanju i kada se `num` promeni.
# --questions--

## --text--

Šta je memoizacija u Reactu?
## --answers--

Tehnika koja kešira vrednosti i funkcije kako bi sprečila nepotrebne ponovne proračune.
---

A technique that lets you manage component state updates to prevent unnecessary recalculations.

### --feedback--

Pomaže u optimizaciji performansi čuvanjem prethodno izračunatih rezultata.
---

A process of reconciling the Virtual DOM with the actual DOM.

### --feedback--

Pomaže u optimizaciji performansi čuvanjem prethodno izračunatih rezultata.
---

A way to handle side effects in functional components.

### --feedback--

Pomaže u optimizaciji performansi čuvanjem prethodno izračunatih rezultata.
## --video-solution--

1

## --text--

Koja je razlika između izračunatih vrednosti i referenci funkcija?
## --answers--

Izračunate vrednosti su objekti funkcija, dok su funkcione reference rezultati izvršavanja.
### --feedback--

Jedan je izlaz funkcije, dok drugi je samo pokazivač na njega.
---

Computed values are the result of executing a function, while function references are the function objects in memory.

---

Computed values and function references are the same thing.

### --feedback--

Jedan je izlaz funkcije, dok drugi je samo pokazivač na njega.
---

Function references store computed values.

### --feedback--

Jedan je izlaz funkcije, dok drugi je samo pokazivač na njega.
## --video-solution--

2

## --text--

Koja od ovih nije jedan od alata koje React pruža za memorizaciju?
## --answers--

`React.memo`

### --feedback--

Alati za memoizaciju fokusiraju se na keširanje vrednosti i funkcija, dok ovaj opcija rukuje sa nuspojavama.
---

`useMemo`

### --feedback--

Alati za memoizaciju fokusiraju se na keširanje vrednosti i funkcija, dok ovaj opcija rukuje sa nuspojavama.
---

`useCallback`

### --feedback--

Alati za memoizaciju fokusiraju se na keširanje vrednosti i funkcija, dok ovaj opcija rukuje sa nuspojavama.
---

`useEffect`

## --video-solution--

4
