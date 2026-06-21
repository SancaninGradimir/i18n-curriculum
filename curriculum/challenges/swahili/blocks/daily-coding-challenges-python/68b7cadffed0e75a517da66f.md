id: 68b7cadffed0e75a517da66f
title: "Challenge 50: Longest Word"
challengeType: 29
dashedName: challenge-50
---

# --description--

Kada dobiješ rečenicu, vrati najduže reč iz te rečenice.

- Ignoriši tačke (`.`) prilikom određivanja dužine reči.
- Ako više reči ima iste dužine kao najduža reč, vrati prvu pojavljenu reč.

# --hints--

`get_longest_word("coding is fun")` should return `"coding"`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(get_longest_word("coding is fun"), "coding")`)
}})
```

`get_longest_word("Coding challenges are fun and educational.")` should return `"educational"`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(get_longest_word("Coding challenges are fun and educational."), "educational")`)
}})
```

`get_longest_word("This sentence has multiple long words.")` should return `"sentence"`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(get_longest_word("This sentence has multiple long words."), "sentence")`)
}})
```

# --seed--

## --seed-contents--

```py
def get_longest_word(sentence):

    return sentence
```

# --solutions--

```py
def get_longest_word(sentence):
    words = sentence.split()
    longest = ''
    for word in words:
        clean_word = word.replace('.', '')
        if len(clean_word) > len(longest):
            longest = clean_word
    return longest
```