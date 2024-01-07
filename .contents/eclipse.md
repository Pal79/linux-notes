<h1 align="center">
<img src="../.pictures/eclipse.png" alt="eclipse" width=64 />
</h1>

---

## eclipse telepítése debian rendszerekre

### snap telepítés

> csomagok frissítése

```
sudo apt update
```

> snap telepítése (ha nincs snap)

```
sudo apt install snapd
```

> snap bekapcsolása (ha nem volt snap)

```
sudo systemctl enable snapd --now
```

> eclipse telepítése

```
sudo snap install eclipse --classic
```

### tar telepítés

> Letöltés

```
https://www.eclipse.org/downloads/packages/
```

> Letöltött fájl ellenőrzése

```
cd Downloads/
```

```
ls
```

> Letöltött fájl áthelyezése:

``` {.bash}
sudo mv downloaded_file.tar.gz /opt
```

```
cd /opt
```

> Letöltött fájl kicsomagolás

```
sudo tar -xvf downloaded-file.tar.gz
```

---

> Indító ikon létrehozása

```
sudo nano /usr/share/applications/eclipse.desktop
```

> Írd ezt a fájlba ->

```
[Desktop Entry]
Name=Eclipse
Comment=Eclipse
Exec=/opt/eclipse/eclipse
Icon=/opt/eclipse/icon.xpm
StartupNotify=true
Terminal=false
Type=Application
Categories=Development;IDE;Java;
```

> majd mentés: ctrl+x -> y -> [enter]

---

[Vissza](../README.md)
