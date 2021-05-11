# IO oder CPU-gebundene Last klären 

![top](Bildschirmfoto%202021-05-11%20um%2009.29.03.png)

```
Fall 1
======
CPU-gebundene Last: in Zeile CPU:
nur 'sy' und 'us' ist hoch 

Fall 2:
=======
IO-gebundene Last
(d.h. egal, ob man eine bessere hat, es bringt nicht mehr,
weil die Festplatte entscheidend ist (in diesem Fal)) 
Die Festplatte ist hier der begrenzende Faktor

sy und wa hoch (wa = waiting, cpu wartet auf das io-subsystem (Festplatte or Storage) 
```
