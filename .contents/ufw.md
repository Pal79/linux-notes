# UFW

---

### Csomagtárolók és rendszer frissítése majd az UFW telepítése:

> frissítés:

```
sudo apt update && sudo apt full-upgrade -y
```

> telepítés:

```
sudo apt install ufw
```

---

### Port hozzáférés engedélyezése

> sudo ufw allow PORTSZÁM

> ssh port engedélyezése:

```
sudo ufw allow 22
```

---

### Sebességkorlátozás a port-on

> ez a funkció hasznos az SSH kapcsolatok korlátozására.

> Megnehezíthetjük egy külső forrás számára a kapcsolat erőszakos kényszerítését.

> Az ufw nem engedélyez 6 vagy több csatlakozást 30 másodpercen belül.

> Beállításhoz az "ufw limit PORTSZÁM"-ot kell használni.

> pl.:

```
sudo ufw limit 22
```

---

[Vissza](./../README.md)
