---
id: 68f1196f0fedc6f6ecc9aba6
title: Korak 4
challengeType: 20
dashedName: step-4
---

# --description--

U Pythonu, tipska oznaka povratne vrednosti ukazuje na očekivani tip povratne vrednosti funkcije ili metode. To radite dodavanjem `-> return_type` nakon liste parametara u definiciji metode.

Evo primera metode sa tipskim oznakama i za parametre i za povratnu vrednost, čija je tip povratne vrednosti `bool`:

```py
def example_method(self, value: int) -> bool:
  pass
```

Drugi tipski oznake povratne vrednosti koje možete koristiti uključuju `str`, `None`, `float` i više.

U postojećoj metodi `__init__`, dodajte tipsku oznaku povratne vrednosti `None` jer konstruktori ne vraćaju vrednost.

# --hints--

Your `__init__` method should have a return type hint of `None`.

```js
({
  test: () => runPython(`assert _Node(_code).find_class("Product").find_function("__init__").has_returns("None")`)
})
```

# --seed--

## --seed-contents--

```py
--fcc-editable-region--
class Product:
    def __init__(self, name: str, price: float):
        self.name = name
        self.price = price
--fcc-editable-region--
    def __str__(self):
        return f'{self.name} - ${self.price}'
```
