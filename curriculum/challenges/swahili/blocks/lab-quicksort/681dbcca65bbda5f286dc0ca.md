---
id: 681dbcca65bbda5f286dc0ca
title: Implementiraj Quicksort Algoritam
challengeType: 27
dashedName: implement-the-quicksort-algorithm
---

# --description--

**Cilj:** Ispunite priče korisnika ispod i osigurajte da svi testovi prođu kako biste završili laboratoriju.

**Priče korisnika:**

1. Trebalo bi da definišete funkciju pod nazivom `quick_sort` za implementaciju algoritma quicksort.

1. Funkcija `quick_sort` treba da primi listu celih brojeva kao ulaz i vrati novu listu ovih celih brojeva u sortiranom redosledu od najmanjeg do najvećeg.

1. Da biste implementirali algoritam, trebalo bi da:
   - Izaberite vrednost pivota iz elemenata ulazne liste (koristite prvi ili poslednji element liste).
   - Podelite ulaznu listu na tri podliste: jednu sa elementima manjim od pivota, jednu sa elementima jednakim pivotu i jednu sa elementima većim od pivota.
   - Rekurzivno pozovite `quick_sort` za sortiranje podlista i konkatenizujte sortirane podliste kako biste proizveli konačnu sortiranu listu.

# --hints--

You should have a function named `quick_sort`.

```js
({ test: () => runPython(`assert _Node(_code).has_function("quick_sort")`) })
```

Your `quick_sort` function should take a single parameter.

```js
({ test: () => runPython(`
from inspect import signature
sig = signature(quick_sort)
assert len(sig.parameters) == 1
`) })
```

`quick_sort([])` should return an empty list.

```js
({ test: () => runPython(`assert quick_sort([]) == []`) })
```

Your `quick_sort` function should not modify the list passed to it as the argument.

```js
({ test: () => runPython(`
_test_list = [20, 3, 14, 1, 5]
quick_sort(_test_list)
assert _test_list == [20, 3, 14, 1, 5]
`) })
```

`quick_sort([20, 3, 14, 1, 5])` should return `[1, 3, 5, 14, 20]`.

```js
({ test: () => runPython(`assert quick_sort([20, 3, 14, 1, 5]) == [1, 3, 5, 14, 20]`) })
```

`quick_sort([83, 4, 24, 2])` should return `[2, 4, 24, 83]`.

```js
({ test: () => runPython(`assert quick_sort([83, 4, 24, 2]) == [2, 4, 24, 83]`) })
```

`quick_sort([4, 42, 16, 23, 15, 8])` should return `[4, 8, 15, 16, 23, 42]`.

```js
({ test: () => runPython(`assert quick_sort([4, 42, 16, 23, 15, 8]) == [4, 8, 15, 16, 23, 42]`) })
```

`quick_sort([87, 11, 23, 18, 18, 23, 11, 56, 87, 56])` should return `[11, 11, 18, 18, 23, 23, 56, 56, 87, 87]`.

```js
({ test: () => runPython(`assert quick_sort([87, 11, 23, 18, 18, 23, 11, 56, 87, 56]) == [11, 11, 18, 18, 23, 23, 56, 56, 87, 87]`) })
```

You should not import any module or use built-in sorting methods in your code.

```js
({ test: () => runPython(`
    assert len(_Node(_code).find_imports()) == 0
    assert not _Node(_code).block_has_call("sort")
    assert not _Node(_code).block_has_call("sorted")
`)})
```

# --seed--

## --seed-contents--

```py

```

# --solutions--

```py
def quick_sort(numbers):
    if not numbers:
        return []
    pivot = numbers[0]
    lesser = []
    equal = []
    greater = []
    for number in numbers:
        if number < pivot:
            lesser.append(number)
        elif number > pivot:
            greater.append(number)
        else:
            equal.append(number)
    return quick_sort(lesser) + equal + quick_sort(greater)
```
