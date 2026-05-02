## Feladat – Heti hőmérsékleti adatok vizsgálata

Egy meteorológiai állomás egy hét reggeli hőmérsékleti adatait rögzítette Celsius-fokban. Az adatokat a `homersekletek` lista tartalmazza.

```python id="8b7o1l"
homersekletek = [12, 9, 15, 11, 7, 13, 16]
```

Készíts programot, amely elvégzi az alábbi műveleteket.

1. Írd ki, hány nap hőmérsékleti adata szerepel a listában.
2. Számítsd ki és írd ki a hőmérsékletek összegét.
3. Számítsd ki és írd ki az átlaghőmérsékletet.
4. Írd ki a legalacsonyabb és a legmagasabb hőmérsékletet.
5. Számold meg, hányszor szerepel a listában a `7` fokos érték.
6. Adj hozzá a listához egy később rögzített, `10` fokos adatot, majd rendezd növekvő sorrendbe a listát.
7. Ha az átlaghőmérséklet legalább `12` fok, írd ki, hogy `A hét hőmérséklete enyhének tekinthető.`, különben írd ki, hogy `A hét hőmérséklete hűvösnek tekinthető.`



## Expected output – Heti hőmérsékleti adatok vizsgálata

```text
A rögzített napok száma: 7
A hőmérsékletek összege: 83
Az átlaghőmérséklet: 11.857142857142858
A legalacsonyabb hőmérséklet: 7
A legmagasabb hőmérséklet: 16
A 7 fokos érték előfordulásainak száma: 1
A rendezett hőmérsékleti adatok: [7, 9, 10, 11, 12, 13, 15, 16]
A hét hőmérséklete hűvösnek tekinthető.
```
