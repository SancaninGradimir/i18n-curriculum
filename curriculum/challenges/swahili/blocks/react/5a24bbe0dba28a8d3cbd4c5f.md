---
id: 5a24bbe0dba28a8d3cbd4c5f
title: Prikaži HTML elemente u DOM-u
challengeType: 6
forumTopicId: 301406
dashedName: render-html-elements-to-the-dom
---

# --description--

Sada ste naučili da je JSX jednostavan alat za pisanje HTML koji se čita unutar JavaScript. Koristeći React, možemo prikazati ovaj JSX direktno na HTML DOM koristeći renderujući API od React poznat kao ReactDOM.

ReactDOM pruža jednostavan način za prikazivanje komponenti od React u DOM, što izgleda ovako: `ReactDOM.render(componentToRender, targetNode)`, gde je prvi argument komponenta za React ili deo koji želite prikazati, a drugi argument je čvor od DOM u kojem želite da prikažete taj deo.

Kama unavyotarajia, `ReactDOM.render()` lazima iitwe baada ya tamko la vipengele vya JSX, kama vile unavyotakiwa kutangaza vigezo kabla ya kuvitumia.

# --instructions--

Editor koda ima jednostavnu sekciju za JSX. Koristite metodu ``ReactDOM.render()`` da prikažete ovaj deo na stranici. Možete proslediti deklarisane JSX komponente direktno kao prvi argument i koristiti ``document.getElementById()`` za odabir čvora `DOM` kako biste prikazali te komponente unutar njega. Dostupan je ``div`` sa ``id='challenge-node'`` za vašu upotrebu. Uverite se da ne menjate konstantu ``JSX``.

# --hints--

Stabilno `JSX` mora da vrati funkcionalnost od `div`.

```js
assert(JSX.type === 'div');
```

`div` inapaswa kuwa na lebo ya `h1` kama kipengele cha kwanza.

```js
assert(JSX.props.children[0].type === 'h1');
```

`div` treba da ima oznaku od `p` kao drugi element.

```js
assert(JSX.props.children[1].type === 'p');
```

Kipengele cha JSX kilichotolewa kinapaswa kuonyeshwa kwenye nodi ya DOM yenye kitambulisho `challenge-node`.

```js
assert(
  document.getElementById('challenge-node').childNodes[0].innerHTML ===
    '<h1>Hello World</h1><p>Lets render this to the DOM</p>'
);
```

# --seed--

## --seed-contents--

```jsx
const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);
// Add your code below this line
```

# --solutions--

```jsx
const JSX = (
<div>
  <h1>Hello World</h1>
  <p>Lets render this to the DOM</p>
</div>
);
// Add your code below this line
ReactDOM.render(JSX, document.getElementById('challenge-node'));
```
