<h1 align="center">
<img src="../.pictures/pycharm.png" alt="pycharm" width=128 />
</h1>

---

## Pycharm telepítése

| Telepítési mód | Leírás | Ubuntu |
| :------------- | :----- | :----- |
| snap telepítés |  |  |
|  | csomagok frissítése | ```sudo apt update``` |
|  | snap telepítése (ha nincs snap) | ```sudo apt install snapd``` |
|  | snap bekapcsolása (ha nem volt snap) | ```sudo systemctl enable snapd --now``` |
|  |  | ```sudo ln -s /var/lib/snapd/snap /snap``` |
|  | Pycharm-community telepítése | ```sudo snap install pycharm-community --classic```<br>vagy<br>```sudo snap install pycharm-community --classic --edge``` |
|  | Pycharm-professional telepítése | ```sudo snap install pycharm-professional --classic```<br> vagy<br>```sudo snap install pycharm-professional --classic --edge``` |
|  | Törlés | ```sudo snap remove pycharm-community```<br>vagy<br>```sudo snap remove pycharm-professional``` |
|  |  |  |
| tar telepítés |  |  |
|  | tar fájl letöltése | ```https://www.jetbrains.com/pycharm/download/?section=linux``` |
|  | letöltött fájl megtekintése | ```cd Downloads```<br>```ls``` |
|  | pycharm mappa létrehozás és a tar kicsomagolása a mappába | ```mkdir pycharm && tar -xvf pycharm-community-*.tar.gz -C pycharm --strip-components 1``` |
|  | a "pycharm" mappa átmozgatása | ```sudo mv pycharm /opt/``` |
|  | indítóikon létrehozása | ```sudo nano /usr/share/applications/pycharm-community.desktop``` |
|  |  fájlba beleírni: |```[Desktop Entry]```<br>```Version=1.0```<br>```Type=Application```<br>```Name=Pycharm```<br>```Comment=IDE```<br>```Exec=/opt/pycharm/bin/pycharm.sh```<br>```Icon=/opt/pycharm/bin/pycharm.png```<br>```Terminal=false```<br>```StartupNotify=false``` |
|  | a fájl futtathatóvá tétele | ```sudo chmod u+x /usr/share/applications/pycharm-community.desktop``` |

---

|     | Manjaro |
| :-- | :------ |
| community telepítése | ```sudo pacman -S pycharm-community-edition``` |
| professional telepítése | ```sudo pacman -S pycharm-professional-edition``` |

---

[Vissza](../README.md)
