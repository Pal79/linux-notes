<h1 align="center">
<img src="../.pictures/chrome.png" alt="chrome" width=64 />
</h1>

---

### google chrome telepítése

|     | Ubuntu |
| :-- | :----- |
| Chorme kulcs letöltése | ```wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub \| sudo apt-key add -``` |
| Chrome repo hozzáadás | ```sudo add-apt-repository "deb http://dl.google.com/linux/chrome/deb/ stable main"``` |
| Csomagok frissítése | ```sudo apt update``` |
| Telepítés | ```sudo apt install google-chrome-stable``` |
| Eltávolítás | ```sudo apt remove google-chrome-stable``` |

---

|     | Manjaro |
| :-- | :------ |
| csomag adatbázis frissítése | ```sudo pacman -Syy``` |
| git telepítése | ```sudo pacman -S git``` |
| google-chrome csomag letöltése git-ről | ```git clone https://aur.archlinux.org/google-chrome.git``` |
| belépés a letöltött könyvtárba | ```cd google-chrome``` |
| base-devel telepítése | ```sudo pacman -S base-devel``` |
| telepítés | ```makepkg -si``` |

---

[Vissza](../README.md)
