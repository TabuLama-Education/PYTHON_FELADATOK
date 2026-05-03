## Feladat – Halgazdasági értékesítés elszámolása

Egy halgazdaság a reggeli lehalászás után ládákba rendezve készíti elő az eladásra szánt halakat. A ládák tömegét kilogrammban mérték le. Az adatokat egy Python-listában tárolják.

Az értékesítés előtt az adatokat javítani kell, majd ki kell számítani a várható bevételt, a költségeket és a napi eredményt.

### Kiinduló adat

```python
lada_tomegek = [12.5, 8.0, 15.2, 6.8, 10.4, 4.5]
```

## Feladat

1. Hozd létre a `lada_tomegek` nevű listát a megadott értékekkel.

2. Add hozzá a lista végéhez a `9.6` értéket, mert egy újabb ládát is lemértek.

3. Szúrd be a lista elejére a `13.2` értéket, mert az elsőként előkészített láda kimaradt a rögzítésből.

4. Távolítsd el a listából a `4.5` értéket, mert az a láda nem kerül értékesítésre.

5. Számítsd ki az összes eladható halmennyiséget, a legkönnyebb láda tömegét, a legnehezebb láda tömegét és az átlagos ládatömeget.

6. Számítsd ki a bruttó árbevételt, a jégköltséget, a szállítási költséget és a nettó eredményt az alábbi adatok alapján:

   * 1 kg hal eladási ára: `1850` Ft
   * 1 kg hal hűtéséhez szükséges jég költsége: `90` Ft
   * egy láda szállítási költsége: `1200` Ft

7. Rendezd a listát növekvő sorrendbe, majd értékeld az eredményt:

   * ha a legkönnyebb láda tömege kisebb, mint `7` kg, írd ki, hogy `Van olyan láda, amelyet külön át kell vizsgálni.`
   * ha a legnehezebb láda tömege nagyobb, mint `15` kg, írd ki, hogy `A legnehezebb ládát külön kell jelölni.`
   * ha a nettó eredmény legalább `120000` Ft és az átlagos ládatömeg legalább `10` kg, írd ki, hogy `A szállítmány gazdaságosan értékesíthető.`
   * különben írd ki, hogy `A szállítmány eredményessége nem megfelelő.`

## Elvárt kimenet

```text
Összes eladható halmennyiség: 75.7 kg
Ládák száma: 7
Legkönnyebb láda: 6.8 kg
Legnehezebb láda: 15.2 kg
Átlagos ládatömeg: 10.81 kg
Bruttó árbevétel: 140045 Ft
Jégköltség: 6813 Ft
Szállítási költség: 8400 Ft
Nettó eredmény: 124832 Ft
Rendezett ládatömegek: [6.8, 8.0, 9.6, 10.4, 12.5, 13.2, 15.2]
Van olyan láda, amelyet külön át kell vizsgálni.
A legnehezebb ládát külön kell jelölni.
A szállítmány gazdaságosan értékesíthető.
```
