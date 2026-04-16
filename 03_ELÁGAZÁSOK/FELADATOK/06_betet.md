# Bankbetét kezelő rendszer

Egy bank egyszerű betétkezelő rendszert használ az ügyfelek betéteinek rögzítésére. A program feladata, hogy egy ügyfél azonosítója, a választott betéttípus és az elhelyezni kívánt összeg alapján ellenőrizze a megadott adatokat, majd kiszámítsa a kamatot és a lejáratkor kivehető összeget.

Készítsen programot, amely elvégzi a betét rögzítését és kiértékelését! A program forráskódját mentse `bankbetet` néven!

A program megírásakor a felhasználó által megadott adatok helyességét, érvényességét nem kell ellenőriznie, és feltételezheti, hogy a rendelkezésre álló adatok a leírtaknak megfelelnek.

A program a következő adatokat tartalmazza:

```python
ugyfelek = ["U101", "U102", "U103", "U104", "U105"]
betet_tipusok = ["Látra szóló", "1 éves betét", "2 éves betét", "Prémium betét"]
betetek = []
```

Statikus változók:

```python
minimum_osszeg = 10000
kamat_szazalek = 5
```

A képernyőre írást igénylő részfeladatok esetén a mintához hasonlóan írja ki a feladat sorszámát, valamint utaljon a kiírt tartalomra is!

1. Kérje be és tárolja el az ügyfél azonosítóját, a választott betéttípust, valamint az elhelyezni kívánt összeget!

2. Vizsgálja meg, hogy a megadott ügyfélazonosító szerepel-e az `ugyfelek` listában! Amennyiben az azonosító nem található a listában, írja ki a mintának megfelelően, hogy „Nincs ilyen ügyfél.”, majd a program fejeződjön be!

3. Vizsgálja meg, hogy a megadott betéttípus szerepel-e a `betet_tipusok` listában! Amennyiben a betéttípus nem található a listában, írja ki a mintának megfelelően, hogy „Nincs ilyen betéttípus.”, majd a program fejeződjön be!

4. Ellenőrizze, hogy a megadott összeg eléri-e a `minimum_osszeg` értékét! Ha az összeg kisebb ennél, írja ki a mintának megfelelően, hogy „A betét összege túl alacsony.”, majd a program fejeződjön be!

5. Amennyiben minden adat megfelelő, rögzítse a betétet a `betetek` listában `[azonosító, betéttípus]` formában!

6. Számítsa ki a kamat összegét a `kamat_szazalek` alapján, majd határozza meg a lejáratkor kivehető teljes összeget!

7. Írassa ki a mintának megfelelően a sikeres betételhelyezés tényét, a kamat összegét, a lejáratkor kivehető teljes összeget, valamint azt, hogy melyik ügyfél milyen betéttípust választott!

## Minta a szöveges kimenet kialakításához:

### 1. példa

```text
1. feladat
Adja meg az ügyfél azonosítóját: U101
Adja meg a betét típusát: 1 éves betét
Adja meg az elhelyezni kívánt összeget: 50000
2. feladat
Az ügyfél azonosítója érvényes.
3. feladat
A betéttípus érvényes.
4. feladat
A megadott összeg megfelelő.
5. feladat
Sikeres betételhelyezés.
6. feladat
Kamat: 2500 Ft
Lejáratkor kivehető összeg: 52500 Ft
7. feladat
Ügyfél: U101 - Betét típusa: 1 éves betét
```

### 2. példa

```text
1. feladat
Adja meg az ügyfél azonosítóját: U999
Adja meg a betét típusát: 1 éves betét
Adja meg az elhelyezni kívánt összeget: 50000
2. feladat
Nincs ilyen ügyfél.
```

### 3. példa

```text
1. feladat
Adja meg az ügyfél azonosítóját: U102
Adja meg a betét típusát: Diák extra
Adja meg az elhelyezni kívánt összeget: 50000
2. feladat
Az ügyfél azonosítója érvényes.
3. feladat
Nincs ilyen betéttípus.
```

### 4. példa

```text
1. feladat
Adja meg az ügyfél azonosítóját: U103
Adja meg a betét típusát: Látra szóló
Adja meg az elhelyezni kívánt összeget: 5000
2. feladat
Az ügyfél azonosítója érvényes.
3. feladat
A betéttípus érvényes.
4. feladat
A betét összege túl alacsony.
```

### 5. példa

```text
1. feladat
Adja meg az ügyfél azonosítóját: U104
Adja meg a betét típusát: Prémium betét
Adja meg az elhelyezni kívánt összeget: 100000
2. feladat
Az ügyfél azonosítója érvényes.
3. feladat
A betéttípus érvényes.
4. feladat
A megadott összeg megfelelő.
5. feladat
Sikeres betételhelyezés.
6. feladat
Kamat: 5000 Ft
Lejáratkor kivehető összeg: 105000 Ft
7. feladat
Ügyfél: U104 - Betét típusa: Prémium betét
```
