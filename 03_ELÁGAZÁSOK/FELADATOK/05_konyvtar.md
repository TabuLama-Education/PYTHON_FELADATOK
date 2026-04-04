
# Könyvtári rendszer – Python feladat

Készíts Python programot egy iskolai könyvtár kölcsönzési rendszerének szimulálására! A program a következők szerint működjön:

## Adatok 

```python
tanulok = ["T101", "T102", "T103", "T104", "T105"]
konyvek  = ["Egri csillagok", "Pál utcai fiúk", "Tüskevár", "1984", "Harry Potter"]
kolcsonzesek = []
```

Statikus változók:
```python
max_nap = 14        # hány napig lehet ingyen kölcsönözni
kesesi_dij = 100    # 1 nap késés után 100 Ft késési díj
```

## A program működése

1. **Adatbekérés**
   - Kérd be a **tanulói azonosítót** (pl. `T101`).
   - Kérd be a **könyv címét** (pl. `"Pál utcai fiúk"`).
   - Kérd be, **hány napra** kéri a könyvet (egész szám).

2. **Könyvtári ellenőrzések (azonnali validálás)**

   - Ha a megadott **tanuló azonosító nincs** a `tanulok` listában:
     - írd ki: `"Nincs ilyen tanuló."`
     - és **azonnal lépjen ki** a program (pl. `exit()` segítségével).  
   - Ha a megadott **könyv nincs** a `konyvek` listában:
     - írd ki: `"Nincs ilyen könyv a könyvtárban."`
     - és **azonnal lépjen ki** a program.

3. **Kölcsönzés kezelése**

   - Ha a tanuló és a könyv is érvényes:
     - adj hozzá a `kolcsonzesek` listához egy új bejegyzést: `[azonosító, könyvcím]` formátumban.  
     - vedd ki a könyvet a `konyvek` listából a `remove()` metódussal.

4. **Késési díj számítás**

   - Ha a kölcsönzési napok száma **nagyobb, mint `max_nap`** (14 nap), akkor:
     - számold ki a késési díjat: 
   - Ha nincs késés, akkor a késési díj legyen **0**.

5. **Kimenet (outputok)**

   - Végül írj ki egy üzenetet:  
     `"Sikeres kölcsönzés."`
   - Írd ki a késési díjat:  
     `"Késési díj: X Ft"` (ahol X a kiszámolt érték).
   - Írd ki, **ki vitte el melyik könyvet**:
     - Minden elemre a `kolcsonzesek` listában:
       - `"Tanuló: T101 - Könyv: Egri csillagok"`

***

## Példa inputok és várható output

### 1. Érvényes eset

```text
Tanulói azonosító: T101
Könyv címe: Egri csillagok
Hány napra kéred? 16
```

**Várható output:**

```text
Sikeres kölcsönzés.
Késési díj: 200 Ft
Tanuló: T101 - Könyv: Egri csillagok
```

### 2. Nem létező tanuló

```text
Tanulói azonosító: T999
```

**Várható output:**

```text
Nincs ilyen tanuló.
```

### 3. Nem létező könyv

```text
Tanulói azonosító: T101
Könyv címe: Robotika
```

**Várható output:**

```text
Nincs ilyen könyv a könyvtárban.
```

### 4. Érvényes tanuló és könyv, nincs késés

```text
Tanulói azonosító: T102
Könyv címe: 1984
Hány napra kéred? 10
```

**Várható output:**

```text
Sikeres kölcsönzés.
Késési díj: 0 Ft
Tanuló: T102 - Könyv: 1984
```

***

