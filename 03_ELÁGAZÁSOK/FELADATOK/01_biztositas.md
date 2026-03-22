# Feladat – Biztosítási kockázatértékelés

Készíts programot, amely egy ügyfél adatai alapján meghatározza a biztosítási kockázati besorolását.

A program kérje be a felhasználótól az alábbi adatokat:

* életkor
* hány éves vezetői gyakorlata van
* okozott-e már balesetet (`igen` vagy `nem`)
* az autó életkora évben
* az autó értéke forintban

A program a következő szabályok alapján végezze el a minősítést:

* Ha az ügyfél életkora kisebb mint 18, akkor a minősítés: **nem köthető biztosítás**
* Ha a vezetői gyakorlata kisebb mint 1 év, akkor a minősítés: **magas kockázat**
* Ha már okozott balesetet **és** az autó értéke nagyobb mint 8000000 Ft, akkor a minősítés: **magas kockázat**
* Ha az ügyfél életkora legfeljebb 25 év **és** az autó életkora kisebb mint 5 év, akkor a minősítés: **emelt kockázat**
* Ha nem okozott balesetet **és** legalább 5 év vezetői gyakorlata van **és** az autó legalább 10 éves, akkor a minősítés: **alacsony kockázat**
* Minden más esetben a minősítés: **átlagos kockázat**

A program a végén írja ki a biztosítási kockázati besorolást.

---


# Expected output – példák

## 1. eset – Nem köthető biztosítás

**Bemenet:**

```text
Add meg az életkort: 17
Add meg a vezetői gyakorlat hosszát évben: 1
Okozott már balesetet? (igen/nem): nem
Add meg az autó korát évben: 8
Add meg az autó értékét forintban: 2500000
```

**Kimenet:**

```text
Minősítés: nem köthető biztosítás
```

---

## 2. eset – Magas kockázat

**Bemenet:**

```text
Add meg az életkort: 30
Add meg a vezetői gyakorlat hosszát évben: 0
Okozott már balesetet? (igen/nem): nem
Add meg az autó korát évben: 6
Add meg az autó értékét forintban: 3000000
```

**Kimenet:**

```text
Minősítés: magas kockázat
```

---

## 3. eset – Emelt kockázat

**Bemenet:**

```text
Add meg az életkort: 24
Add meg a vezetői gyakorlat hosszát évben: 3
Okozott már balesetet? (igen/nem): nem
Add meg az autó korát évben: 2
Add meg az autó értékét forintban: 6500000
```

**Kimenet:**

```text
Minősítés: emelt kockázat
```

---

## 4. eset – Alacsony kockázat

**Bemenet:**

```text
Add meg az életkort: 42
Add meg a vezetői gyakorlat hosszát évben: 12
Okozott már balesetet? (igen/nem): nem
Add meg az autó korát évben: 11
Add meg az autó értékét forintban: 2200000
```

**Kimenet:**

```text
Minősítés: alacsony kockázat
```

---

## 5. eset – Átlagos kockázat

**Bemenet:**

```text
Add meg az életkort: 33
Add meg a vezetői gyakorlat hosszát évben: 4
Okozott már balesetet? (igen/nem): nem
Add meg az autó korát évben: 7
Add meg az autó értékét forintban: 4200000
```

**Kimenet:**

```text
Minősítés: átlagos kockázat
```
