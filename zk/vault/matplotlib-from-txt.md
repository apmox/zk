# `matplotlib` import vectors from `.txt` file
Le righe sono separate da spazi e formano colonne.
``` txt
0.000 1.000 2.000
3.000 4.000 5.000
6  7  8
```

Per importare in python da file dove `x` e `y` sono i vettori colonna uso[^1]:
``` python
with open('file.txt') as f:
    lines = f.readlines()
    x = [line.split()[0] for line in lines]
    y = [line.split()[1] for line in lines]
```
```python
>>> x
['0.000', '3.000', '6']
```

Tuttavia `x` e `y` sono liste di stringhe, quindi per `matplotlib` devo convertire
in `float` o `int`, usando l'accorgimento[^2]:
``` python
import matplotlib.pyplot as plt
with open('file.txt', 'r') as f:
    lines = f.readlines()
    x = [float(line.split()[0]) for line in lines]
    y = [float(line.split()[1]) for line in lines]
plt.plot(x, y)
plt.show()
```

[^1]: https://stackoverflow.com/a/38532516
[^2]: https://stackoverflow.com/a/54531290
