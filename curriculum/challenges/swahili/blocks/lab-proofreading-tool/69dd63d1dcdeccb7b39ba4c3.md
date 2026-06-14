---
id: 69dd63d1dcdeccb7b39ba4c3
title: Izgradite alat za korekturu teksta
challengeType: 26
dashedName: build-a-proofreading-tool
---

# --description--

U ovom laboratorijumu, kreiraćete alat za proveru teksta koji analizira niz reči na palindrome i ponavljene fraze.

Palindrom je reč koja se čita isto napred i nazad. Na primer, `"racecar"` i `"level"` su palindromi, ali `"hello"` nije.

Fraza je sekvenca uzastopnih reči. Na primer, u `["the", "cat", "sat", "the", "cat"]`, fraza `"the cat"` (sekvenca od 2 reči) pojavljuje se na pozicijama 0 i 3.

**Cilj:** Ispunite korisničke priče ispod i osigurajte da svi testovi prođu kako biste završili laboratorijum.

**Korisničke priče:**

1. Trebalo bi da definišete funkciju pod nazivom `isPalindrome` koja uzima string `word` kao argument. Trebalo bi da vrati `true` ako se reč čita isto napred i nazad (bez razличиja između velikih i malih slova), i `false` inače.

2. Trebalo bi da definišete funkciju pod nazivom `findPalindromeBreaks` koja uzima niz `words` kao argument. Trebalo bi da vrati niz indeksa reči koje nisu palindromi. Trebalo bi da vrati prazan niz ako je ulaz prazan.

3. Trebalo bi da definišete funkciju pod nazivom `findRepeatedPhrases` koja uzima niz `words` i broj `phraseLength` kao argumente. Trebalo bi da vrati niz svih početnih indeksa gde se sekvenca od `phraseLength` uzastopnih reči pojavljuje više puta u nizu — uključujući indeks prvog pojavljivanja. Trebalo bi da vrati prazan niz ako je `phraseLength` veći ili jednak dužini `words`. Preklapajuće sekvence takođe treba računati.

4. Trebalo bi da definišete funkciju pod nazivom `analyzeTexts` koja uzima niz `texts` i broj `phraseLength` kao argumente. Trebalo bi da obradi svaki element `texts` (svaki je niz reči) i vrati niz objekata, od kojih svaki ima svojstva `repeatedPhrases` i `palindromeBreaks`. Trebalo bi da vrati prazan niz ako je `texts` prazan.

# --hints--

`isPalindrome` should be a function.

```js
assert.isFunction(isPalindrome);
```

`isPalindrome` should return `true` for a palindrome.

```js
assert.isTrue(isPalindrome("racecar"));
assert.isTrue(isPalindrome("a"));
```

`isPalindrome` should return `true` regardless of case.

```js
assert.isTrue(isPalindrome("Level"));
```

`isPalindrome` should return `false` for a non-palindrome.

```js
assert.isFalse(isPalindrome("hello"));
```

`findPalindromeBreaks` should be a function.

```js
assert.isFunction(findPalindromeBreaks);
```

`findPalindromeBreaks` should return an empty array for empty input.

```js
assert.sameDeepOrderedMembers(findPalindromeBreaks([]), []);
```

`findPalindromeBreaks` should return the indices of non-palindromes.

```js
assert.sameDeepOrderedMembers(findPalindromeBreaks(["racecar", "hello", "level"]), [1]);
```

`findPalindromeBreaks` should return an empty array when all words are palindromes.

```js
assert.sameDeepOrderedMembers(findPalindromeBreaks(["racecar", "level", "aba"]), []);
```

`findRepeatedPhrases` should be a function.

```js
assert.isFunction(findRepeatedPhrases);
```

`findRepeatedPhrases` should return an empty array when `phraseLength` is greater than or equal to the length of `words`.

```js
assert.sameDeepOrderedMembers(findRepeatedPhrases(["the", "cat"], 2), []);
```

`findRepeatedPhrases` should return an empty array when `phraseLength` is greater than the length of `words`.

```js
assert.sameDeepOrderedMembers(findRepeatedPhrases(["the"], 2), []);
```

`findRepeatedPhrases` should return all start indices where the phrase repeats, including the first occurrence.

```js
assert.sameDeepOrderedMembers(findRepeatedPhrases(["the", "cat", "sat", "the", "cat"], 2), [0, 3]);
```

`findRepeatedPhrases` should return all start indices for overlapping repeated phrases.

```js
assert.sameDeepOrderedMembers(findRepeatedPhrases(["ba", "ba", "ba"], 2), [0, 1]);
```

`analyzeTexts` should be a function.

```js
assert.isFunction(analyzeTexts);
```

`analyzeTexts` should return an empty array for empty input.

```js
assert.sameDeepOrderedMembers(analyzeTexts([], 2), []);
```

`analyzeTexts` result objects should have `repeatedPhrases` and `palindromeBreaks` properties.

```js
const result = analyzeTexts([["racecar", "hello"]], 2);
assert.property(result[0], "repeatedPhrases");
assert.property(result[0], "palindromeBreaks");
```

`analyzeTexts` should correctly aggregate results for each text.

```js
const result = analyzeTexts([["racecar", "hello", "level", "hello"]], 1);
assert.sameDeepOrderedMembers(result[0].repeatedPhrases, [1, 3]);
assert.sameDeepOrderedMembers(result[0].palindromeBreaks, [1, 3]);
```

`analyzeTexts` should process multiple texts and return a result for each.

```js
const result = analyzeTexts([["racecar", "hello"], ["level", "world", "level"]], 1);
assert.lengthOf(result, 2);
assert.sameDeepOrderedMembers(result[1].palindromeBreaks, [1]);
assert.sameDeepOrderedMembers(result[1].repeatedPhrases, [0, 2]);
```

# --seed--

## --seed-contents--

```js

```

# --solutions--

```js
function isPalindrome(word) {
  const lower = word.toLowerCase();
  for (let i = 0; i < Math.floor(lower.length / 2); i++) {
    if (lower[i] !== lower[lower.length - 1 - i]) {
      return false;
    }
  }
  return true;
}

function findPalindromeBreaks(words) {
  const breaks = [];
  if (words.length === 0) return breaks;
  for (let i = 0; i < words.length; i++) {
    if (!isPalindrome(words[i])) {
      breaks.push(i);
    }
  }
  return breaks;
}

function findRepeatedPhrases(words, phraseLength) {
  const result = [];
  if (phraseLength >= words.length) return result;

  for (let i = 0; i <= words.length - phraseLength; i++) {
    const phrase = words.slice(i, i + phraseLength).join(" ");
    let found = false;

    for (let j = 0; j <= words.length - phraseLength; j++) {
      if (i === j) continue;
      if (words.slice(j, j + phraseLength).join(" ") === phrase) {
        found = true;
        break;
      }
    }

    if (found) result.push(i);
  }

  return result;
}

function analyzeTexts(texts, phraseLength) {
  const results = [];
  if (texts.length === 0) return results;

  for (let i = 0; i < texts.length; i++) {
    results.push({
      repeatedPhrases: findRepeatedPhrases(texts[i], phraseLength),
      palindromeBreaks: findPalindromeBreaks(texts[i])
    });
  }

  return results;
}
```
