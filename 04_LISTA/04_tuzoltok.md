## Feladat – Tűzoltóautók vízkészletének ellenőrzése

Egy tűzoltóállomáson a szolgálat végén ellenőrzik, hogy a bevetésből visszaérkező gépjárműfecskendők tartályában hány liter víz maradt. Az adatokat egy Python-listában tárolják. A lista minden eleme egy-egy jármű aktuális vízkészletét jelenti literben.

### Kiinduló adat

```python
vizkeszletek = [3200, 1800, 2500, 4100, 900, 3600]
```

### Feladat

1. Hozd létre a `vizkeszletek` nevű listát a megadott értékekkel.

2. A szolgálat végén még egy jármű visszaérkezett, amelynek tartályában `2800` liter víz maradt. Add hozzá ezt az értéket a lista végéhez.

3. A lista elejére szúrd be a `5000` értéket, mert a tartalék jármű teljesen feltöltött állapotban áll készenlétben.

4. Távolítsd el a listából a `900` értéket, mert az adott jármű adata hibásan került rögzítésre.

5. Számítsd ki és írasd ki az összes rendelkezésre álló vízmennyiséget, a legnagyobb vízkészletet, a legkisebb vízkészletet és az átlagos vízkészletet.

6. Rendezd a listát növekvő sorrendbe, majd írasd ki a rendezett listát.

7. Elágazással döntsd el, hogy az átlagos vízkészlet eléri-e a `3000` litert. Ha igen, írd ki: `A járművek vízkészlete megfelelő.`, különben írd ki: `A járművek vízkészletét pótolni kell.`

### Elvárt kimenet

```text
Összes vízkészlet: 23000 liter
Legnagyobb vízkészlet: 5000 liter
Legkisebb vízkészlet: 1800 liter
Átlagos vízkészlet: 3285.71 liter
Rendezett vízkészletek: [1800, 2500, 2800, 3200, 3600, 4100, 5000]
A járművek vízkészlete megfelelő.
```

