#Note
27-05-2024
Tags: [[Mathe]] [[Grundlagen-&-Infinitesimalrechnung]] [[Python]] [[Data-Science]]


Mit Sigma $ \Sigma $ wird impliziert, dass die angegebenen Elemente ***summiert*** werden.

Möchte man die Zahlen 1 bis 8 durchlaufen und jede Zahl dabei mit 5 multiplizieren, würde die Formel lauten:    $\sum^{8}_{i=1}5i$
Das lässt sich natürlich auch in Python umsetzen.


```python
summation = sum(5*i for i in range(1, 9))
print(summation) # Ausgabe 180
```

Allgemein geschrieben sieht sie so aus: $\sum^{n}_{i=1}x_i$   Dabei ist $n$ die *Anzahl der Elemente* und $x_i$ ein iteriertes Element. $i=1$ gibt die *Schrittweite* 1 an.





---
## Info

[[Mathe Basics für Data Scientists]]