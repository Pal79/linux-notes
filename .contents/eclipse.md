<h1 align="center">
<img src="../.pictures/eclipse.png" alt="eclipse" width=64 />
</h1>

---

# Eclipse

| Telepítési mód | Művelet | Leírás |
| :------------- | :------ | :----- |
| snap telepítés |  |  |
|  | csomagok frissítése | ```sudo apt update``` |
|  | snap telepítése (ha nincs snap) | ```sudo apt install snapd``` |
|  | snap bekapcsolása (ha nem volt snap) | ```sudo systemctl enable snapd --now``` |
|  | Telepítés | ```sudo snap install eclipse --classic``` |
|  |  |  |
| tar telepítés |  |  |
|  | Letöltés | ```https://www.eclipse.org/downloads/packages/``` |
|  | Letöltött fájl ellenőrzése | ```cd Downloads/```<br>```ls``` |
|  | Letöltött fájl áthelyezése | ```sudo mv downloaded_file.tar.gz /opt``` |
|  | Belépés a könyvtárba |```cd /opt``` |
|  | Letöltött fájl kicsomagolás | ```sudo tar -xvf downloaded-file.tar.gz``` |
|  | Indító ikon létrehozása | ```sudo nano /usr/share/applications/eclipse.desktop``` |
|  | Írd ezt a fájlba: | ```[Desktop Entry]```<br>```Name=Eclipse```<br>```Comment=Eclipse```<br>```Exec=/opt/eclipse/eclipse```<br>```Icon=/opt/eclipse/icon.xpm```<br>```StartupNotify=true```<br>```Terminal=false```<br>```Type=Application```<br>```Categories=Development;IDE;Java;``` |
|  | majd mentés: | ```Ctrl+x -> y -> [enter]``` |

---

[Vissza](../README.md)
