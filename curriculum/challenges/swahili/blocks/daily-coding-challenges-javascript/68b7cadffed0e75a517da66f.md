id: 68b7cadffed0e75a517da66f
title: "Vežba 50: Najduže reči"
challengeType: 28
dashedName: challenge-50
---

# --description--

Kada dobijete rečenicu, vratite najdužu reč u toj rečenici.

- Ignorišite tačke (.) prilikom određivanja dužine reči.
- Ako više reči ima istu dužinu najduže reči, vratite prvu pojavljenu reč.

# --hints--

`getLongestWord("coding is fun")` bi trebalo da vrati `"coding"`.

```js
assert.equal(getLongestWord("coding is fun"), "coding");
```

`getLongestWord("Coding challenges are fun and educational.")` bi trebalo da vrati `"educational"`.

```js
assert.equal(getLongestWord("Coding challenges are fun and educational."), "educational");
```

`getLongestWord("This sentence has multiple long words.")` bi trebalo da vrati `"sentence"`.

```js
assert.equal(getLongestWord("This sentence has multiple long words."), "sentence");
```

# --seed--

## --seed-contents--

```js
function getLongestWord(sentence) {

  return sentence;
}
```

# --solutions--

```js
function getLongestWord(sentence) {
  const words = sentence.split(' ');

  let longest = '';
  for (let word of words) {
    const cleanWord = word.replace(/\./g, '');
    if (cleanWord.length > longest.length) {
      longest = cleanWord;
    }
  }

  return longest;
}
```