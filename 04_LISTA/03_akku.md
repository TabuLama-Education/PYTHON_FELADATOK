## Feladat – Drónküldetés akkumulátoradatainak ellenőrzése

Egy iskolai drónverseny előtt a csapat ellenőrzi a drónok akkumulátorának töltöttségét. Az adatokat százalékban az `akkumulatorok` lista tartalmazza.

A listában egy `0` érték hibás mérésnek számít, mert egy bekapcsolt drón akkumulátora nem lehet 0%-os. A hibás adatot el kell távolítani. Ezután egy új drón adata bekerül a lista második helyére, majd egy tartalék akkumulátor értékét is rögzíteni kell a lista végén.

```python
akkumulatorok = [88, 0, 73, 95, 100, 47, 86]
```

Készíts programot, amely elvégzi az alábbi műveleteket.

1. Vizsgáld meg, hogy a legkisebb érték `0`-e.
2. Ha igen, keresd meg a helyét, majd töröld a listából.
3. Szúrd be a lista második helyére a `92` értéket.
4. Add hozzá a lista végéhez a `68` értéket.
5. Készíts másolatot a módosított listáról.
6. Rendezd a listát csökkenő sorrendbe.
7. Írd ki:

   * a módosított eredeti sorrendet,
   * a csökkenő sorrendbe rendezett listát,
   * az akkumulátorok számát,
   * az átlagos töltöttséget,
   * a legalacsonyabb és legmagasabb értéket,
   * hány akkumulátor van teljesen feltöltve.
8. Ha a legalacsonyabb érték kisebb, mint `50`, írd ki: `Van olyan drón, amelyet még tölteni kell.`
9. Egyébként, ha az átlag legalább `80`, írd ki: `A dróncsapat indításra kész.`
10. Más esetben írd ki: `A dróncsapat részleges előkészítést igényel.`


## Megoldás

```python
akkumulatorok = [88, 0, 73, 95, 100, 47, 86]

legkisebb_eredeti = min(akkumulatorok)

if legkisebb_eredeti == 0:
    hibas_adat_helye = akkumulatorok.index(0)
    torolt_adat = akkumulatorok.pop(hibas_adat_helye)
    print("Törölt hibás adat:", torolt_adat)

akkumulatorok.insert(1, 92)
akkumulatorok.append(68)

modositott_sorrend = akkumulatorok.copy()

akkumulatorok.sort()
akkumulatorok.reverse()

darab = len(akkumulatorok)
osszeg = sum(akkumulatorok)
atlag = osszeg / darab
legalacsonyabb = min(akkumulatorok)
legmagasabb = max(akkumulatorok)
teljesen_feltoltott = akkumulatorok.count(100)

print("Módosított eredeti sorrend:", modositott_sorrend)
print("Rendezett akkumulátoradatok:", akkumulatorok)
print("A vizsgált akkumulátorok száma:", darab)
print("Az átlagos töltöttség:", atlag)
print("A legalacsonyabb töltöttség:", legalacsonyabb)
print("A legmagasabb töltöttség:", legmagasabb)
print("Teljesen feltöltött akkumulátorok száma:", teljesen_feltoltott)

if legalacsonyabb < 50:
    print("Van olyan drón, amelyet még tölteni kell.")
elif atlag >= 80:
    print("A dróncsapat indításra kész.")
else:
    print("A dróncsapat részleges előkészítést igényel.")
```

## Expected output

```text
Törölt hibás adat: 0
Módosított eredeti sorrend: [88, 92, 73, 95, 100, 47, 86, 68]
Rendezett akkumulátoradatok: [100, 95, 92, 88, 86, 73, 68, 47]
A vizsgált akkumulátorok száma: 8
Az átlagos töltöttség: 81.125
A legalacsonyabb töltöttség: 47
A legmagasabb töltöttség: 100
Teljesen feltöltött akkumulátorok száma: 1
Van olyan drón, amelyet még tölteni kell.
```
