

# Bankbetét kezelő rendszer

Készíts Python programot egy egyszerű banki betétkezelő rendszer szimulálására! A program a következők szerint működjön:

## Adatok

```python
ugyfelek = ["U101", "U102", "U103", "U104", "U105"]
betet_tipusok = ["Látra szóló", "1 éves betét", "2 éves betét", "Prémium betét"]
betetek = []
```

Statikus változók:

```python
minimum_osszeg = 10000    # ennyi forinttól lehet betétet elhelyezni
kamat_szazalek = 5        # a betét éves kamata 5%
```

## A program működése

1. **Adatbekérés**

   * Kérd be az **ügyfél azonosítóját** (pl. `U101`).
   * Kérd be a **betét típusát** (pl. `"1 éves betét"`).
   * Kérd be, **mekkora összeget** szeretne elhelyezni (egész szám).

2. **Banki ellenőrzések (azonnali validálás)**

   * Ha a megadott **ügyfél azonosító nincs** az `ugyfelek` listában:

     * írd ki: `"Nincs ilyen ügyfél."`
     * és **azonnal lépjen ki** a program (pl. `exit()` segítségével).
   * Ha a megadott **betét típus nincs** a `betet_tipusok` listában:

     * írd ki: `"Nincs ilyen betéttípus."`
     * és **azonnal lépjen ki** a program.
   * Ha a megadott **összeg kisebb, mint `minimum_osszeg`**:

     * írd ki: `"A betét összege túl alacsony."`
     * és **azonnal lépjen ki** a program.

3. **Betét rögzítése**

   * Ha az ügyfél, a betét típus és az összeg is érvényes:

     * adj hozzá a `betetek` listához egy új bejegyzést: `[azonosító, betéttípus]` formátumban.

4. **Kamat számítás**

   * Számold ki a kamatot a következő képlettel:

     * `kamat = osszeg * kamat_szazalek / 100`
   * Ezután számold ki a lejáratkor kivehető teljes összeget:

     * `vegosszeg = osszeg + kamat`

5. **Kimenet (outputok)**

   * Végül írj ki egy üzenetet:
     `"Sikeres betételhelyezés."`
   * Írd ki a kamat összegét:
     `"Kamat: X Ft"`
     ahol `X` a kiszámolt kamat.
   * Írd ki a lejáratkor kivehető teljes összeget:
     `"Lejáratkor kivehető összeg: Y Ft"`
   * Írd ki, **melyik ügyfél milyen betétet választott**:

     * Minden elemre a `betetek` listában:

       * `"Ügyfél: U101 - Betét típusa: 1 éves betét"`

---

## Példa inputok és várható output

### 1. Érvényes eset

```text
Ügyfél azonosító: U101
Betét típusa: 1 éves betét
Mekkora összeget szeretnél elhelyezni? 50000
```

**Várható output:**

```text
Sikeres betételhelyezés.
Kamat: 2500 Ft
Lejáratkor kivehető összeg: 52500 Ft
Ügyfél: U101 - Betét típusa: 1 éves betét
```

### 2. Nem létező ügyfél

```text
Ügyfél azonosító: U999
```

**Várható output:**

```text
Nincs ilyen ügyfél.
```

### 3. Nem létező betéttípus

```text
Ügyfél azonosító: U102
Betét típusa: Diák extra
```

**Várható output:**

```text
Nincs ilyen betéttípus.
```

### 4. Túl alacsony összeg

```text
Ügyfél azonosító: U103
Betét típusa: Látra szóló
Mekkora összeget szeretnél elhelyezni? 5000
```

**Várható output:**

```text
A betét összege túl alacsony.
```

### 5. Érvényes ügyfél és betét, megfelelő összeg

```text
Ügyfél azonosító: U104
Betét típusa: Prémium betét
Mekkora összeget szeretnél elhelyezni? 100000
```

**Várható output:**

```text
Sikeres betételhelyezés.
Kamat: 5000 Ft
Lejáratkor kivehető összeg: 105000 Ft
Ügyfél: U104 - Betét típusa: Prémium betét
```
