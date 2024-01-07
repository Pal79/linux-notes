<h1 align="center">
<img src="../.pictures/pycharm.png" alt="pycharm" width=128 />
</h1>

---

## telepítés debian rendszerekre

### snap telepítés:

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

```
sudo ln -s /var/lib/snapd/snap /snap
```

#### Pycharm community telepítése

```
sudo snap install pycharm-community --classic
```

> vagy

```
sudo snap install pycharm-community --classic --edge
```

#### Pycharm professional telepítése

```
sudo snap install pycharm-professional --classic
```

> vagy

```
sudo snap install pycharm-professional --classic --edge
```

#### Pycharm snap törlése

> ebben a példában a community-t törlöm

```
sudo snap remove pycharm-community
```

### tar telepítés

> tar fájl letöltése

```
https://www.jetbrains.com/pycharm/download/?section=linux
```

> letöltött fájl megtekintése

```
cd Downloads
```

```
ls
```

> pycharm mappa létrehozás és a tar kicsomagolása a mappába

```
mkdir pycharm && tar -xvf pycharm-community-*.tar.gz -C pycharm --strip-components 1
```

> a "pycharm" mappa átmozgatása

```
sudo mv pycharm /opt/
```

> indító ikon létrehozása

```
sudo nano /usr/share/applications/pycharm-community.desktop
```

> fájlba beleírni

```
[Desktop Entry]
Version=1.0
Type=Application
Name=Pycharm
Comment=IDE
Exec=/opt/pycharm/bin/pycharm.sh
Icon=/opt/pycharm/bin/pycharm.png
Terminal=false
StartupNotify=false
```

> a fájl futtathatóvá tétele

```
sudo chmod u+x /usr/share/applications/pycharm-community.desktop
```

---

## pycharm telepítése arch rendszerekre

> community telepítése

```
sudo pacman -S pycharm-community-edition
```

> professional telepítése

```
sudo pacman -S pycharm-professional-edition
```

---

[Vissza](../README.md)
