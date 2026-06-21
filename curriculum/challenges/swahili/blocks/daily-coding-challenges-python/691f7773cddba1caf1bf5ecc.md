id: 691f7773cddba1caf1bf5ecc
title: "Challenge 133: Daylight Hours"
challengeType: 29
dashedName: challenge-133
---

# --description--

21. decembar je zimska solstic na severnom polu i letnja solstic na južnom polu. To znači da je dan sa najmanje dnevnog svetla na severu i najviše dnevnog svetla na jugu.

Datovanjem geografske širine od -90 do 90, vratite približnu procenu sati dnevnog svetla tokom solsticija koristeći sledeću tabelu:

|Latituda|Sati dnevnog svetla|
|-90|24|
|-75|23|
|-60|21|
|-45|15|
|-30|13|
|-15|12|
|0|12|
|15|11|
|30|10|
|45|9|
|60|6|
|75|2|
|90|0|

- Ako data širina nije tačno odgovarajuć elementu u tabeli, koristite najbližu vrednost širine.

# --hints--

`daylight_hours(45)` should return `9`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(45), 9)`)
}})
```

`daylight_hours(0)` should return `12`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(0), 12)`)
}})
```

`daylight_hours(-90)` should return `24`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(-90), 24)`)
}})
```

`daylight_hours(-10)` should return `12`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(-10), 12)`)
}})
```

`daylight_hours(23)` should return `10`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(23), 10)`)
}})
```

`daylight_hours(88)` should return `0`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(88), 0)`)
}})
```

`daylight_hours(-33)` should return `13`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(-33), 13)`)
}})
```

`daylight_hours(70)` should return `2`.

```js
({test: () => { runPython(`
from unittest import TestCase
TestCase().assertEqual(daylight_hours(70), 2)`)
}})
```

# --seed--

## --seed-contents--

```py
def daylight_hours(latitude):

    return latitude
```

# --solutions--

```py
def daylight_hours(latitude):
    table = [
        (-90, 24),
        (-75, 23),
        (-60, 21),
        (-45, 15),
        (-30, 13),
        (-15, 12),
        (0, 12),
        (15, 11),
        (30, 10),
        (45, 9),
        (60, 6),
        (75, 2),
        (90, 0)
    ]

    closest_lat, hours = table[0]

    for lat, h in table:
        if abs(lat - latitude) < abs(closest_lat - latitude):
            closest_lat, hours = lat, h

    return hours
```