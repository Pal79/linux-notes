<h1 align="center">
<img src="../.pictures/spring-tool-suite.png" alt="spring tool suite" width=64 />
</h1>

---

> Letöltés

```
https://www.spring.io/
```

> Letöltött fájl ellenőrzése

```
cd Downloads/
```

```
ls
```

> Letöltött fájl áthelyezése

```
sudo mv downloaded_file.tar.gz /opt
```

```
cd /opt
```

> Letöltött fájl kicsomagolása

```
sudo tar -xvf downloaded-file.tar.gz
```

> Indító ikon létrehozása

```
sudo nano /usr/share/applications/stsLauncher.desktop
```

> Írd ezt a fájlba ->

```
[Desktop Entry]
Name=Spring Tool Suite
Comment=Spring Tool Suite 4.16.0
Exec=/opt/sts-4.16.0.RELEASE/SpringToolSuite4
Icon=/opt/sts-4.16.0.RELEASE/icon.xpm
StartupNotify=true
Terminal=false
Type=Application
Categories=Development;IDE;Java;
```

> majd mentés: ctrl+x -> y -> [enter]

---

[Vissza](../README.md)
