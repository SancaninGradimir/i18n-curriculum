---
id: 67d1ad82cff954a854bcbcaa
title: Šta je prop drilling?
challengeType: 19
dashedName: what-is-prop-drilling
---

# --description--

Prop drilling je najosnovniji pristup upravljanju stanjem u React aplikacijama. Izgleda jednostavno, ali brzo može postati neuredno i veoma je teško skalirati.

Pogledajmo šta je prop drilling, zašto predstavlja problem i kakva je dobra zamena za njega kako vaša aplikacija raste.

Prop drilling je proces prosleđivanja props-ova od roditeljskog komponenta ka duboko ugnježdene detiljne komponente, čak i kada neke od tih detilnih komponenti ne zahtevaju te props-ove.

Na primer, recimo da imate tri komponente nazvane `Parent`, `Child` i `Grandchild`. Ako želite da koristite neke podatke u `Grandchild` komponenti, ali se ti podaci nalaze u `Parent` komponenti, morali biste ih proslediti od `Parent`-a ka `Child` komponenti, a zatim od `Child`-a ka `Grandchild` komponenti.

Ili ako su podaci još više na lancu, možda će biti potrebno da se proslede i ka `Parent` komponenti.

Ovde je podatak koji želim da prikažem string `Hello, Prop Drilling!`. On je dodeljen promenljivoj `greeting` u korenom `App` komponentu:

```jsx
import "./App.css";
import Parent from "./Parent";

function App() {
  const greeting = "Hello, Prop Drilling!";

  return <Parent greeting={greeting} />;
}

export default App;
```

Možete videti da `Parent` komponenta takođe prima promenljivu `greeting` kao vrednost `greeting` prop-a. Evo kako `Parent` komponenta prosleđuje to u `Child` komponentu kao vrednost drugog `greeting` prop-a u `Child`-u:

```jsx
import Child from "./Child";

const Parent = ({ greeting }) => {
  return <Child greeting={greeting} />;
};

export default Parent;
```

A evo `Child` komponente koja ga prosleđuje ka `Grandchild` komponenti:

```jsx
import Grandchild from "./Grandchild";

const Child = ({ greeting }) => {
  return <Grandchild greeting={greeting} />;
};

export default Child;
```

I konačno, `Grandchild` komponenta prima pozdrav i koristi ga kao sadržaj `h1` elementa:

```jsx
const Grandchild = ({ greeting }) => {
  return <h1>{greeting}</h1>;
};

export default Grandchild;
```

U pretraživaču ćete videti stranicu sa jednim `h1` elementom koji ima tekst `Hello, Prop Drilling!`.

Na prvi pogled, prop drilling možda ne deluje kao veliki problem. Ali kako vaša aplikacija raste, postaje sve teže za razumevanje, debagovanje i održavanje.

Ako morate da prosleđujete props-ove, pokušajte da ih zadržite u jednoj roditeljskoj komponenti. Ovaj pristup centralizovanja svih potrebnih podataka naziva se "single source of truth" (jedinstveni izvor istine).

Na primer, recimo da želite dodati novi `response` koji ide uz vaš `greeting`, i da želite da koristite oba u `Grandchild` komponenti. Pošto je `greeting` već u `App` komponenti, ima smisla staviti i `response` tamo, i proslediti ih obe niz lanac:

```jsx
function App() {
  const greeting = "Hello, Prop Drilling!";
  const response = "I'm not here to play!";

  return <Parent greeting={greeting} response={response} />;
}

const Parent = ({ greeting, response }) => {
  return <Child greeting={greeting} response={response} />;
};

const Child = ({ greeting, response }) => {
  return <Grandchild greeting={greeting} response={response} />;
};

const Grandchild = ({ greeting, response }) => {
  return (
    <>
      <h1>{greeting}</h1>
      <h2>{response}</h2>
    </>
  );
};

export default App;
```

U pretraživaču ćete videti stranicu sa `h1` elementom koji ima tekst `Hello, Prop Drilling!` i `h2` elementom koji ima tekst `I'm not here to play!`.

Da biste izbegli prop drilling, posebno u velikim, kompleksnim aplikacijama, razmislite o korišćenju Context API-ja ili biblioteka za upravljanje stanjem kao što su Redux i Redux Toolkit, Zustand, Recoil i drugi.

Ovo ćete saznati više u narednim lekcijama.
# --questions--

## --text--

Kako bi se prop preneo od roditeljskog dočeka komponenta?
## --answers--

Definisanjem prop-a unutar komponente praunuka.
### --feedback--

Prop mora proći kroz dete pre nego što stigne do unuka.
---

By passing it from parent to child, then from child to grandchild.

---

By using the `useEffect` hook to fetch the prop dynamically.

### --feedback--

Prop mora proći kroz dete pre dolaska do unuka.
---

By using the `useState` hook in the grandchild.

### --feedback--

Prop mora proći kroz dete pre dolaska do unuka.
## --video-solution--

2

## --text--

Šta je "prop drilling" u Reactu?
## --answers--

Direktno prosleđivanje propova samo komponentama kojima su potrebni.
### --feedback--

To se dešava kada propovi se nepotrebno prosleđuju kroz više nivoa.
---

Using context to share state between components.

### --feedback--

To se dešava kada propovi se nepotrebno prosleđuju kroz više nivoa.
---

Passing props from a parent to deeply nested child components.

---

Drilling down into component state using hooks.

### --feedback--

To se dešava kada propovi se nepotrebno prosleđuju kroz više nivoa.
## --video-solution--

3

## --text--

Zašto se „prop drilling“ smatra problemom u većim aplikacijama?
## --answers--

Olakšava upravljanje stanjem.
### --feedback--

Previše propova koji prolaze kroz više komponenti može učiniti kod neurednim.
---

It improves performance by reducing re-renders.

### --feedback--

Previše propova koji prolaze kroz više komponenti može učiniti kod neurednim.
---

It makes the code harder to read, debug, and maintain.

---

It eliminates the need for state management libraries.

### --feedback--

Previše propova koji prolaze kroz više komponenti može učiniti kod neurednim.
## --video-solution--

3
