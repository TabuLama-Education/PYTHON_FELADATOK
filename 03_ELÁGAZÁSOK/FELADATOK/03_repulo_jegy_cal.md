# Feladat – Repülőjegy végösszegének kiszámítása

Készíts programot, amely kiszámítja egy repülőjegy végösszegét az utas adatai alapján.

A program kérje be a felhasználótól az alábbi adatokat:

* az alapjegy árát forintban
* az utas életkorát
* az út hosszát kilométerben
* a feladott poggyász tömegét kilogrammban
* szeretne-e elsőbbségi beszállást (`igen` vagy `nem`)
* nemzetközi járatra utazik-e (`igen` vagy `nem`)

A program a következő szabályok alapján számoljon:

## 1. Kedvezmény az életkor alapján

A program az életkor alapján határozza meg a kedvezmény mértékét:

* 2 év alatt: 90% kedvezmény
* 2–11 év között: 50% kedvezmény
* 12–64 év között: nincs kedvezmény
* 65 évtől: 20% kedvezmény

## 2. Távolsági illeték

A program az út hossza alapján számítson fel illetéket:

* 0–999 km: 0 Ft
* 1000–2999 km: 8000 Ft
* 3000 km vagy több: 15000 Ft

## 3. Poggyászdíj

A feladott poggyász díja:

* 20 kg-ig: 0 Ft
* 21–30 kg között: 6000 Ft
* 30 kg felett: 12000 Ft

## 4. Elsőbbségi beszállás

Ha az utas elsőbbségi beszállást kér, akkor a program adjon hozzá még **4000 Ft**-ot a végösszeghez.

## 5. Nemzetközi járat kezelési díja

Ha az utas nemzetközi járatra utazik, akkor a program adjon hozzá még **7000 Ft** kezelési díjat.

A program végül írja ki:

* a kedvezmény összegét
* a távolsági illetéket
* a poggyászdíjat
* az extra szolgáltatások összegét
* a fizetendő végösszeget

---

# Expected output – példa

**Bemenet:**

```text
Add meg az alapjegy árát Ft-ban: 50000
Add meg az utas életkorát: 70
Add meg az út hosszát km-ben: 3200
Add meg a feladott poggyász tömegét kg-ban: 24
Kér elsőbbségi beszállást? (igen/nem): igen
Nemzetközi járat? (igen/nem): igen
```

**Számítás:**

* 20% kedvezmény a 50000 Ft-ból = 10000 Ft
* kedvezményes jegyár = 40000 Ft
* távolsági illeték = 15000 Ft
* poggyászdíj = 6000 Ft
* extra díj = 4000 + 7000 = 11000 Ft

**Kimenet:**

```text
Kedvezmény összege: 10000.0 Ft
Távolsági illeték: 15000 Ft
Poggyászdíj: 6000 Ft
Extra szolgáltatások összege: 11000 Ft
Fizetendő végösszeg: 72000.0 Ft
```


