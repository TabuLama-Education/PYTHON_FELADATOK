
# Tanulói adatbázis

Egy iskola egyszerű tanulói adatbázist vezet, amelyben a diákok azonosítója, neve, osztálya és jegyei szerepelnek. A program feladata, hogy egy megadott azonosító alapján megkeresse a megfelelő tanulót, majd megjelenítse a hozzá tartozó adatokat és kiszámítsa a jegyek átlagát.

A program forráskódját mentse `tanuloadatbazis` néven!

A program megírásakor a felhasználó által megadott adatok helyességét nem kell ellenőriznie, és feltételezheti, hogy a rendelkezésre álló adatok a leírtaknak megfelelnek.

A program a következő adatokat tartalmazza:

```python
azonositok = ["D101", "D102", "D103", "D104"]
nevek = ["Kiss Anna", "Nagy Péter", "Tóth Lili", "Szabó Márk"]
osztalyok = ["10.A", "10.B", "10.A", "10.C"]
jegyek = [
    [5, 4, 5],
    [3, 4, 2],
    [5, 5, 4],
    [2, 3, 4]
]
```

A képernyőre írást igénylő részfeladatok esetén a mintához hasonlóan írja ki a feladat sorszámát is!

1. Kérje be és tárolja el egy tanuló azonosítóját!

2. Határozza meg, hogy a megadott azonosító szerepel-e az `azonositok` listában! Ha nem található ilyen azonosító, a mintának megfelelően írja ki, hogy nincs ilyen diák az adatbázisban!

3. Amennyiben a megadott azonosító szerepel a listában, határozza meg a tanuló helyét az `index()` metódus segítségével!

4. A meghatározott index alapján írassa ki a tanuló azonosítóját, nevét, osztályát és jegyeit!

5. Számítsa ki a tanuló jegyeinek átlagát, majd jelenítse meg a mintának megfelelően!

## Minta a szöveges kimenet kialakításához:

### 1. példa

```text
1. feladat
Adja meg a diák azonosítóját: D101
2. feladat
A diák megtalálható az adatbázisban.
3. feladat
A diák adatai:
Azonosító: D101
Név: Kiss Anna
Osztály: 10.A
Jegyek: [5, 4, 5]
4. feladat
A tanuló átlaga: 4.67
```

### 2. példa

```text
1. feladat
Adja meg a diák azonosítóját: D999
2. feladat
Nincs ilyen diák az adatbázisban.
```
