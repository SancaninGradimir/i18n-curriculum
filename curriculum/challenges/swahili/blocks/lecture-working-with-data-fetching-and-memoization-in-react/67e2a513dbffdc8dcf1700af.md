---
id: 67e2a513dbffdc8dcf1700af
title: Šta je `useOptimistic` hook, i kako funkcioniše?
challengeType: 19
dashedName: what-is-the-useoptimistic-hook-and-how-does-it-work
---

# --description--

Novije verzije React-a uveli su server komponente i server akcije kako bi prebacile deo odgovornosti za renderovanje i logiku na server.

Uz te ažuriranja, React je dodao novi hook pod nazivom `useOptimistic` da bi održavao korisničke interfejse (UI) reaktivnim dok čekaju da se asinhrona akcija završi u pozadini.

Iako se ovo često koristi za preuzimanje podataka sa servera, nije ograničeno samo na to. Hook je generalno koristan za rukovanje asinhronim operacijama, osiguravajući da UI ostane glatok i interaktivan dok akcija radi.

Pogledajmo šta je `useOptimistic` hook i kako doprinosi stvaranju brstih i reaktivnih UI-ja.

`useOptimistic` hook pomaže u upravljanju "optimističkim ažuriranjima" (optimistic updates) u UI-u, strategijom po kojoj pružate trenutna ažuriranja UI-u na osnovu očekivanog ishoda akcije, kao što je čekanje odgovora sa servera.

Evo osnovne sintakse `useOptimistic` hook-a:

```js
const [optimisticState, addOptimistic] = useOptimistic(actualState, updateFunction);
```

- `optimisticState` je privremeni stanje koje se ažurira odmah radi boljeg korisničkog iskustva.

- `addOptimistic` je funkcija koja primenjuje optimističko ažuriranje pre nego što se stvarni stanja promene.

- `actualState` je stvarna vrednost stanja koja dolazi iz rezultata akcije, kao što je preuzimanje podataka sa servera.

- `updateFunction` je funkcija koja određuje kako bi optimistično stanje trebalo da se ažurira kada se pozove.

Na prvi pogled, može delovati da je `useOptimistic` hook samo još jedan način za rukovanje stanjima učitavanja u Reactu. Ali to je više od toga.

Stanje učitavanja kontroli da li vidite spinner, poruku ili neki drugi indikator u UI-u dok se nešto dešava u pozadini.

Međutim, `useOptimistic` hook ažurira UI trenutno na osnovu očekivanog ishoda, čak i pre nego što, recimo, napravite poziv ka API-ju. Ovaj hook vam daje šansu da prikažete indikator učitavanja ili poruku, graceful (graciozno) rukujete potencijalnim greškama i pokažete trenutnu povratnu informaciju kako bi se UI osećao brže.

Ovo će postati jasnije dok prolazimo kroz nekoliko primera koji pokazuju kako radi `useOptimistic` hook.

Evo akcije koja simulira čuvanje zadatka na serveru. Vraća zadatak nakon kašnjenja od 1 sekundu, jer se to može desiti sa stvarnim API zahtevom:

```js
export async function saveTask(task) {
  await new Promise((res) => setTimeout(res, 1000));

  return task;
}
```

Evo koda koji postavlja `useOptimistic` hook uvesti i inicijalizovati, sa funkcijom `handleSubmit` koja šalje unos akciji:

```jsx
"use client";

import { useOptimistic } from "react";

export default function TaskList({ tasks, addTask }) {
  const [optimisticTasks, addOptimisticTask] = useOptimistic(
    tasks,
    (state, newTask) => [...state, { text: newTask, pending: true }]
  );

  async function handleSubmit(e) {
    e.preventDefault();
    const formData = new FormData(e.target);

    addOptimisticTask(formData.get("task"));

    addTask(formData);
    e.target.reset();
  }

  return <>{/* UI */}</>;
}
```

U kodu, `useOptimistic` hook održava privatan spisak zadataka koji se odmah ažurira kada dodate novi zadatak.

Linija, `(state, newTask) => [...state, { text: newTask, pending: true }]` osigurava da novi zadatak se pojavi sa statusom čekanja čak i pre nego što server potvrdi nešto iz forme.

Kada se forma pošalje, funkcija `handleSubmit` izvlači zadatak i dodaje ga "optimistički" pomoću parametra `addOptimisticTask`. Zatim je `addTask` prosleđen kao prop koji šalje zadatak na server. Konačno, forma se resetuje pozivom `e.target.reset()`.

Evo komponente `TaskList`:

```jsx
"use client";
import { useOptimistic, startTransition } from "react";

export default function TaskList({ tasks, addTask }) {
  const [optimisticTasks, addOptimisticTask] = useOptimistic(
    tasks,
    (state, newTask) => [...state, { text: newTask, pending: true }]
  );

  async function handleSubmit(e) {
    e.preventDefault();
    const formData = new FormData(e.target);

    startTransition(() => {
      addOptimisticTask(formData.get("task"));
    });

    addTask(formData);
    e.target.reset();
  }

  return (
    <div className="max-w-md mx-auto p-4">
      <h3 className="text-xl font-medium mb-3">Tasks</h3>

      <ul className="space-y-2 mb-4">
        {optimisticTasks.map((task, index) => (
          <li key={index} className="p-2 border-b">
            {task.text}
            {task.pending && (
              <small className="ml-2 text-gray-500 text-sm">
                Adding Task...
              </small>
            )}
          </li>
        ))}
      </ul>

      <form onSubmit={handleSubmit} className="flex gap-2">
        <input
          type="text"
          name="task"
          placeholder="Type in a task..."
          className="flex-1 p-2 border"
        />
        <button type="submit" className="bg-gray-200 px-3 py-2 cursor-pointer">
          Submit
        </button>
      </form>
    </div>
  );
}
```

Ovde iteriramo kroz parametar `optimisticTask` da bismo prikazali zadatak. Kada je `task.pending` `true`, pored teksta se prikazuje "Adding Task...", potvrđujući da je zadatak optimistički dodan pre nego što ga server potvrdi.

Evo komponente `Task` koja upravlja stanjem za formu. Poziva funkciju `saveTask` iz akcije kako bi mogla dodati zadatak, i spaja novi zadatak kada mu server primi:

```jsx
"use client";

import { useState } from "react";
import TaskList from "./TaskList";
import { saveTask } from "./actions";

export default function Tasks() {
  const [tasks, setTasks] = useState([]);

  async function addTask(formData) {
    const newTaskText = formData.get("task");

    const savedTask = await saveTask(newTaskText);
    setTasks((prev) => [...prev, { text: savedTask, pending: false }]);
  }

  return <TaskList tasks={tasks} addTask={addTask} />;
}
```

Ovo osigurava brze ažuriranja UI-ja prikazujući trenutnu povratnu informaciju umesto čekanja na odgovor. Kada se zadatak sačuva, svojstvo `pending` se uklanja i konačni spisak zadataka odgovarajuće se ažurira.

U UI-u, dešavaju se dve stvari koje ne bi trebalo da se dogode. Prvo, ne možete videti tekst "Adding Task..." jer se pojavljuje i nestaje prebrzo. Sledeći, postoji greška koja nastaje nakon dodavanja zadatka.

Dve stvari moramo da uradimo kako bismo rešili te probleme.

Prvo, moramo uvesti `startTransition` iz React-a i koristiti ga za obmotavanje linije `addOptimisticTask(formData.get('task'))`:

```js
startTransition(() => {
  addOptimisticTask(formData.get("task"));
});
```

Drugo, moramo učiniti tekst "Adding Task..." vidljivim neko vreme pre nego što nestane.

Da bismo to uradili, možemo modifikovati funkciju `addTask` sa stanjem čekanja i simulirati kašnjenje od nekoliko sekundi pre označavanja zadatka kao završenog. `setTimeout()` je idealan za ovo:

```js
async function addTask(formData) {
  const newTaskText = formData.get("task");

  // Add an optimistic task with a pending state
  const tempTask = { id: Date.now(), text: newTaskText, pending: true };
  setTasks((prev) => [...prev, tempTask]);

  // Simulate a 3 seconds delay before marking the task as completed
  setTimeout(async () => {
    const savedTask = await saveTask(newTaskText);

    setTasks((prev) =>
      prev.map((task) =>
        task.id === tempTask.id
          ? { ...task, text: savedTask, pending: false }
          : task
      )
    );
  }, 3000);
}
```

I kada to učinite, sve radi kako treba.
# --questions--

## --text--

Koja je svrha `useOptimistic` hook-a?
## --answers--

Omogućava komponentama da dohvate podatke sa servera pre renderovanja korisničkog interfejsa.
### --feedback--

Ovaj hak osigurava da se korisnički interfejs (UI) odražaju očekivane promene pre nego što asinhrona operacija završi.
---

It helps manage optimistic updates by updating the UI immediately while waiting for an async operation, like a server response.

---

It enables automatic error handling and rollback for failed API requests in React applications.

### --feedback--

Ovaj hak osigurava da se korisnički interfejs (UI) odražaju očekivane promene pre nego što asinhrona operacija završi.
---

It optimizes state updates by batching them together to improve performance.

### --feedback--

Ovaj hak osigurava da se korisnički interfejs (UI) odražaju očekivane promene pre nego što asinhrona operacija završi.
## --video-solution--

2

## --text--

Kako se kuka ``useOptimistic`` razlikuje od stanja učitavanja?
## --answers--

Stanje učitavanja prikazuje povratnu informaciju korisničkog interfejsa dok čeka odgovora, dok ``useOptimistic`` ažurira UI odmah na osnovu očekivanog ishoda.
---

A loading state modifies server data instantly while `useOptimistic` only updates the client UI.

### --feedback--

Jedinica ažurira korisnički interfejs pre nego što server čak sazna za zahtev.
---

The `useOptimistic` hook is used for handling errors, whereas a loading state is only for showing spinners.

### --feedback--

Jedinica ažurira korisnički interfejs pre nego što server čak sazna za zahtev.
---

Both are the same, but `useOptimistic` provides automatic retries for failed requests.

### --feedback--

Jedinica ažurira korisnički interfejs pre nego što server čak sazna za zahtev.
## --video-solution--

1

## --text--

Šta radi ``addOptimistic`` u sintaksi okidača ``useOptimistic`` ispod?

```js
const [optimisticState, addOptimistic] = useOptimistic(actualState, updateFunction);
```

## --answers--

Primjenjuje optimističko ažuriranje prije stvarnih promjena stanja, pružajući bolji korisnički doživljaj.
---

It fetches the real state from the server and updates the UI accordingly.

### --feedback--

Ova funkcija ažurira korisnički interfejs pre stvarnih promena stanja.
---

It replaces the actual state with a temporary state after receiving a server response.

### --feedback--

Ova funkcija ažurira korisnički interfejs pre stvarnih promena stanja.
---

It validates server data before applying the optimistic update to the UI.

### --feedback--

Ova funkcija ažurira korisnički interfejs pre stvarnih promena stanja.
## --video-solution--

1
