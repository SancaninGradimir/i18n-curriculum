---
id: 686fdcfe055bcda9f651dd2e
title: Izgradite konverter od liste susednosti u matricu
challengeType: 27
dashedName: build-an-adjacency-list-to-matrix-converter
---

# --description--

U ovom laboratorijumu, kreiraćete funkciju koja konvertuje predstavljanje liste susednosti grafa u matricu susednosti. Lista susednosti je rečnik gde svaki ključ predstavlja čvor, a odgovarajuća vrednost je lista čvorova sa kojima je ključni čvor povezan. Matrica susednosti je 2D niz gde je unos na poziciji `[i][j]` jednak `1` ako postoji ivica od čvora `i` ka čvoru `j`, i `0` u suprotnom.

Na primer, dato lista susednosti:

```py
{
    0: [1, 2],
    1: [2],
    2: [0, 3],
    3: [2]
}
```

Odgovarajuća matrica susednosti bi bila:

```py
[
    [0, 1, 1, 0],
    [0, 0, 1, 0],
    [1, 0, 0, 1],
    [0, 0, 1, 0]
]
```

**Cilj:** Ispunite priče korisnika ispod i učinite da svi testovi prođu kako biste završili laboratorijum.

**Priče korisnika:**

1. Trebalo bi da definišete funkciju pod nazivom `adjacency_list_to_matrix` za konverziju liste susednosti u matricu susednosti.
2. Funkcija bi trebalo da primi rečnik koji predstavlja listu susednosti neponderisanog (ili nedirektnog ili usmerenog) grafa kao argument.
3. Funkcija bi trebalo da:
   - Konvertuje listu susednosti u matricu susednosti.
   - Ispiše svaki red u matrici susednosti.
   - Vrati matricu susednosti.

Na primer, `adjacency_list_to_matrix({0: [2], 1: [2, 3], 2: [0, 1, 3], 3: [1, 2]})` bi trebalo da ispisa:

```md
[0, 0, 1, 0]
[0, 0, 1, 1]
[1, 1, 0, 1]
[0, 1, 1, 0]
```

i vrati `[[0, 0, 1, 0], [0, 0, 1, 1], [1, 1, 0, 1], [0, 1, 1, 0]]`.

# --hints--

You should define a function named `adjacency_list_to_matrix`.

```js
({ 
    test: () => assert(runPython(`
    _Node(_code).has_function("adjacency_list_to_matrix")
    `)) 
})
```

The `adjacency_list_to_matrix` function should have one parameter.

```js
({ test: () => assert(runPython(`
    import inspect 
    sig = inspect.signature(adjacency_list_to_matrix)
    len(sig.parameters) == 1
  `))
})
```

The function should correctly determine the number of nodes from the adjacency list.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [1], 1: [0], 2: []}
        result = adjacency_list_to_matrix(adj_list)
        assert len(result) == 3
        assert len(result[0]) == 3
    `) 
})
```

The function should correctly set matrix values to `1` for existing edges.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [1], 1: [0]}
        result = adjacency_list_to_matrix(adj_list)
        assert result[0][1] == 1
        assert result[1][0] == 1
        assert result[0][0] == 0
        assert result[1][1] == 0
    `) 
})
```

The function should print each row of the matrix.

```js
({ 
    test: () => runPython(`
        import io
        import sys
        
        captured_output = io.StringIO()
        sys.stdout = captured_output
        
        adj_list = {0: [1], 1: []}
        adjacency_list_to_matrix(adj_list)
        
        sys.stdout = sys.__stdout__
        output = captured_output.getvalue()
        
        assert "[0, 1]" in output
        assert "[0, 0]" in output
    `) 
})
```

The function should return the adjacency matrix.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [1], 1: []}
        result = adjacency_list_to_matrix(adj_list)
        assert result == [[0, 1], [0, 0]]
    `) 
})
```

When given the adjacency list `{0: [1, 2], 1: [2], 2: [0, 3], 3: [2]}`, the function should return `[[0, 1, 1, 0], [0, 0, 1, 0], [1, 0, 0, 1], [0, 0, 1, 0]]`.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [1, 2], 1: [2], 2: [0, 3], 3: [2]}
        result = adjacency_list_to_matrix(adj_list)
        expected = [[0, 1, 1, 0], [0, 0, 1, 0], [1, 0, 0, 1], [0, 0, 1, 0]]
        assert result == expected
    `) 
})
```

When given the adjacency list `{0: [1], 1: [0]}`, the function should return `[[0, 1], [1, 0]]`.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [1], 1: [0]}
        result = adjacency_list_to_matrix(adj_list)
        expected = [[0, 1], [1, 0]]
        assert result == expected
    `) 
})
```

When given the adjacency list `{0: [], 1: [], 2: []}`, the function should return `[[0, 0, 0], [0, 0, 0], [0, 0, 0]]`.

```js
({ 
    test: () => runPython(`
        adj_list = {0: [], 1: [], 2: []}
        result = adjacency_list_to_matrix(adj_list)
        expected = [[0, 0, 0], [0, 0, 0], [0, 0, 0]]
        assert result == expected
    `) 
})
```

# --seed--

## --seed-contents--

```py

```

# --solutions--

```py
def adjacency_list_to_matrix(adj_list):
    n = len(adj_list)
    
    adj_matrix = [[0] * n for _ in range(n)]

    for src_node, neighbors in adj_list.items(): 
        for dest_node in neighbors:
            adj_matrix[src_node][dest_node] = 1

    for row in adj_matrix:
        print(row)

    return adj_matrix

adj_list = {
    0: [1, 2],
    1: [2],
    2: [0, 3],
    3: [2]
}

matrix = adjacency_list_to_matrix(adj_list)
```
