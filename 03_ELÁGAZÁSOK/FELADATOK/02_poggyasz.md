# Feladat – Repülőutas poggyász- és beszállási minősítés

Készíts programot, amely egy utas adatai alapján eldönti, hogy felszállhat-e a gépre, kell-e extra díjat fizetnie, vagy további ellenőrzés szükséges.

A program kérje be a felhasználótól az alábbi adatokat:

* az utas életkora
* a kézipoggyász tömege kilogrammban
* a feladott poggyász tömege kilogrammban
* rendelkezik-e beszállókártyával (`igen` vagy `nem`)
* rendelkezik-e érvényes személyazonosító okmánnyal (`igen` vagy `nem`)
* nemzetközi járatra utazik-e (`igen` vagy `nem`)

A program a következő szabályok alapján végezze el a minősítést:

* Ha az utas nem rendelkezik beszállókártyával, akkor az eredmény: **nem szállhat be**
* Ha az utas nem rendelkezik érvényes okmánnyal, akkor az eredmény: **nem szállhat be**
* Ha a kézipoggyász tömege nagyobb mint 10 kg, akkor az eredmény: **kézipoggyász túl nehéz**
* Ha a feladott poggyász tömege nagyobb mint 25 kg, akkor az eredmény: **túlsúlydíj fizetendő**
* Ha az utas nemzetközi járatra utazik **és** 18 év alatti, akkor az eredmény: **további ellenőrzés szükséges**
* Ha minden feltétel megfelelő, akkor az eredmény: **beszállhat**

A program a végén írja ki a megfelelő minősítést.

---



# Expected output – példák

## 1. eset – Nem szállhat be

**Bemenet:**

```text
Add meg az utas életkorát: 34
Add meg a kézipoggyász tömegét kg-ban: 8
Add meg a feladott poggyász tömegét kg-ban: 20
Van beszállókártya? (igen/nem): nem
Van érvényes okmány? (igen/nem): igen
Nemzetközi járat? (igen/nem): nem
```

**Kimenet:**

```text
Minősítés: nem szállhat be
```

---

## 2. eset – Kézipoggyász túl nehéz

**Bemenet:**

```text
Add meg az utas életkorát: 29
Add meg a kézipoggyász tömegét kg-ban: 13
Add meg a feladott poggyász tömegét kg-ban: 18
Van beszállókártya? (igen/nem): igen
Van érvényes okmány? (igen/nem): igen
Nemzetközi járat? (igen/nem): nem
```

**Kimenet:**

```text
Minősítés: kézipoggyász túl nehéz
```

---

## 3. eset – Túlsúlydíj fizetendő

**Bemenet:**

```text
Add meg az utas életkorát: 45
Add meg a kézipoggyász tömegét kg-ban: 7
Add meg a feladott poggyász tömegét kg-ban: 28
Van beszállókártya? (igen/nem): igen
Van érvényes okmány? (igen/nem): igen
Nemzetközi járat? (igen/nem): nem
```

**Kimenet:**

```text
Minősítés: túlsúlydíj fizetendő
```

---

## 4. eset – További ellenőrzés szükséges

**Bemenet:**

```text
Add meg az utas életkorát: 16
Add meg a kézipoggyász tömegét kg-ban: 6
Add meg a feladott poggyász tömegét kg-ban: 17
Van beszállókártya? (igen/nem): igen
Van érvényes okmány? (igen/nem): igen
Nemzetközi járat? (igen/nem): igen
```

**Kimenet:**

```text
Minősítés: további ellenőrzés szükséges
```

---

## 5. eset – Beszállhat

**Bemenet:**

```text
Add meg az utas életkorát: 38
Add meg a kézipoggyász tömegét kg-ban: 8
Add meg a feladott poggyász tömegét kg-ban: 22
Van beszállókártya? (igen/nem): igen
Van érvényes okmány? (igen/nem): igen
Nemzetközi járat? (igen/nem): nem
```

**Kimenet:**

```text
Minősítés: beszállhat
```
