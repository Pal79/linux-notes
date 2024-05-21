<h1 align="center">
<img src="../.pictures/spring-tool-suite.png" alt="spring tool suite" width=64 />
</h1>

---

| Leírás | Parancs |
| :----- | :------ |
| Letöltés | ```https://www.spring.io/``` |
| Letöltött fájl ellenőrzése | ```cd Downloads/```<br>```ls``` |
| Letöltött fájl áthelyezése | ```sudo mv downloaded_file.tar.gz /opt``` |
| Az áthelyezett fájl helyének megnyitása | ```cd /opt``` |
| Letöltött fájl kicsomagolása | ```sudo tar -xvf downloaded-file.tar.gz``` |
| Indító ikon létrehozása | ```sudo nano /usr/share/applications stsLauncher.desktop``` |
| Írd ezt a fájlba | ```[Desktop Entry]```<br>```|Name=Spring Tool Suite```<br>```Comment=Spring Tool Suite 4.16.0```<br>```Exec=/opt/sts-4.16.0.RELEASE/SpringToolSuite4```<br>```Icon=/opt/sts-4.16.0.RELEASE/icon.xpm```<br>```StartupNotify=true```<br>```Terminal=false```<br>```Type=Application```<br>```Categories=Development;IDE;Java;``` |
| Mentés | Ctrl + x -> y -> [enter] |

---

[Vissza](../README.md)
