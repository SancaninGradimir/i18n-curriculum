id: 691f7773cddba1caf1bf5ece
title: "Challenge 135: Re: Fwd: Fw: Count"
challengeType: 29
dashedName: challenge-135
---

# --description--

Kada dobijete niz znakova koji predstavlja redak teme e-mail poruke, utvrdite koliko puta je ta e-mail poruka ponovo poslata ili odgovorjena.

Jednostavno rečeno, smatrate da je e-mail poruka ponovo poslata ili odgovorjena ako sadrži jedan od sledećih prefiksa (bez obzira na veličinu slova):

- `"fw:"`
- `"fwd:"`
- `"re:"`

Vratite ukupan broj puta kada su ovi prefiksi pronađeni.

# --hints--

`email_chain_count("Re: Meeting Notes")` should return `1`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(email_chain_count("Meeting Notes"), 1)`)
}})
```

`email_chain_count("Meeting Notes")` should return `0`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(email_chain_count("Meeting Notes"), 0)`)
}})
```

`email_chain_count("Re: re: RE: rE: Meeting Notes")` should return `4`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(email_chain_count("Meeting Notes"), 4)`)
}})
```

`email_chain_count("Re: Fwd: Re: Fw: Re: Meeting Notes")` should return `5`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(email_chain_count("Meeting Notes"), 5)`)
}})
```

`email_chain_count("re:Ref:fw:re:review:FW:Re:fw:report:Re:FW:followup:re:summary:Fwd:Re:fw:NextStep:RE:fw:re:Project:Fwd:Re:fw:Notes:RE:re:Update:FWD:Re:fw:Summary")` should return `23`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(email_chain_count("Meeting Notes"), 23)`)
}})
```

# --seed--

## --seed-contents--

```py
def email_chain_count(subject):

    return subject
```

# --solutions--

```py
def email_chain_count(subject):
    markers = ["re:", "fwd:", "fw:"]
    lower = subject.lower()
    count = 0

    for marker in markers:
        start = 0
        while True:
            idx = lower.find(marker, start)
            if idx == -1:
                break
            count += 1
            start = idx + len(marker)

    return count
```