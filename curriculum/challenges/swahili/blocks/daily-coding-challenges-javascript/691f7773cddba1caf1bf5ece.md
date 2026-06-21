id: 691f7773cddba1caf1bf5ece
title: "Vežba 135: Re: Fwd: Fw: Računanje"
challengeType: 28
dashedName: challenge-135
---

# --description--

Kada dobijete niz znakova koji predstavlja liniju teme e-pošte, utvrdite koliko puta je ta e-pošta ponovo poslata ili odgovorjena.

Jednostavno, smatrate da je e-pošta ponovno poslata ili odgovorjena ako niz znakova sadrži bilo jedan od sledećih prefiksa (bez obzira na velika ili mala slova):

- `"fw:"`
- `"fwd:"`
- `"re:"`

Vratite ukupan broj puta kada su se ovi prefiksi pojavili.

# --hints--

`emailChainCount("Re: Meeting Notes")` bi trebalo da vrati `1`.

```js
assert.equal(emailChainCount("Re: Meeting Notes"), 1);
```

`emailChainCount("Meeting Notes")` bi trebalo da vrati `0`.

```js
assert.equal(emailChainCount("Meeting Notes"), 0);
```

`emailChainCount("Re: re: RE: rE: Meeting Notes")` bi trebalo da vrati `4`.

```js
assert.equal(emailChainCount("Re: re: RE: rE: Meeting Notes"), 4);
```

`emailChainCount("Re: Fwd: Re: Fw: Re: Meeting Notes")` bi trebalo da vrati `5`.

```js
assert.equal(emailChainCount("Re: Fwd: Re: Fw: Re: Meeting Notes"), 5);
```

`emailChainCount("re:Ref:fw:re:review:FW:Re:fw:report:Re:FW:followup:re:summary:Fwd:Re:fw:NextStep:RE:FW:re:Project:Fwd:Re:fw:Notes:RE:re:Update:FWD:Re:fw:Summary")` bi trebalo da vrati `23`.

```js
assert.equal(emailChainCount("re:Ref:fw:re:review:FW:Re:fw:report:Re:FW:followup:re:summary:Fwd:Re:fw:NextStep:RE:FW:re:Project:Fwd:Re:fw:Notes:RE:re:Update:FWD:Re:fw:Summary"), 23);
```

# --seed--

## --seed-contents--

```js
function emailChainCount(subject) {

  return subject;
}
```

# --solutions--

```js
function emailChainCount(subject) {
  const markers = ["re:", "fwd:", "fw:"];
  const lower = subject.toLowerCase();
  let count = 0;

  for (const marker of markers) {
    let index = 0;
    while ((index = lower.indexOf(marker, index)) !== -1) {
      count++;
      index += marker.length;
    }
  }

  return count;
}
```