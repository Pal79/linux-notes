<h1 align="center">
<img src="../.pictures/swap.png" alt="swap" width=128 />
</h1>

---

### swapfile létrehozása ext4 partíción:

> ebben a példában egy 1 gigabájtos fájlt hozok létre:
   > értelemszerűen az 1G -> lehet 16G is vagy egyéb...

```
sudo fallocate -l 1G /swapfile
```

> jogosultságok beállítása:

```
sudo chmod 600 /swapfile
```

> swapfile formázása:

```
sudo mkswap /swapfile
```

> swapfile használatának engedélyezése:

```
sudo swapon /swapfile
```

> swapfile felvétele az fstab-ba:

```
sudo nano /etc/fstab
```

> beírni a következőket a fájl végére:

```
/swapfile	swap	swap	defaults	0	0
```

> vagy

```
/swapfile	none	swap	sw	0	0
```

> swapfile ellenőrzése:

```
sudo swapon --show
```

### swapfile létrehozása btrfs partíción:

> belépés root-ként

```
sudo su
```

> subvolume létrhozása swap néven

```
btrfs subvolume create /swap
```

> ebben a példában egy 4GB-os swapfile létrehozása

```
btrfs filesystem mkswapfile --size 4g --uuid clear /swap/swapfile
```

> swapfile használatának engedélyezése

```
swapon /swap/swapfile
```

> swapfile felvétele az fstab-ba:

```
sudo nano /etc/fstab
```

> beírni a következőket a fájl végére:

```
/swap/swapfile	swap	swap	defaults	0	0
```

> vagy

```
/swap/swapfile	none	swap	sw	0	0
```

---

### swappiness érték beállítása

> A swappiness egy kernel, mely meghatározza, hogy a rendszer milyen gyakran használja a csereterületet. Paraméter 0 és 100 között lehet. A 0-hoz közeli érték eredménye a swap terület használatának elkerülése, míg a magasabb érték ennek ellenkezője. Alapértelmezett beállítás: 60

> sappiness érték megtekintése

```
cat /proc/sys/vm/swappiness
```

> érték átállítása:

```
sudo sysctl vm.swappiness=30
```

> hogy az érték újraindítás után is megmaradjon

```
sudo nano /etc/sysctl.conf
```

> hozzáfűzni a fájlhoz:

```
vm.swappiness=30
```

> Érdemes apró lépésenként csökkenteni vagy növelni az értéket az optimális érték megtalálásához.

---

### Swap fájl törlése

> swapfile deaktiválása:

```
sudo swapoff -v /swapfile
```

> fstab-ból a swap törlése:

```
sudo nano /etc/fstab
```

> ezt a sort kell törölni:

```
/swapfile	none	swap	sw	0	0
```

> swapfile törlése:

```
sudo rm -f /swapfile
```

---

[Vissza](../README.md)
