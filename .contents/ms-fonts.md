<h1 align="center">
<img src="../.pictures/ms-fonts.png" alt="microsoft fonts" width=128 />
</h1>

---

|      | Ubuntu | Manjaro |
| :--- | :----- | :------ |
| csomagok frissítése | ```sudo apt update``` | ```sudo pacman -Syu```<br>ha rég volt frissítve<br>```sudo pacman -Syyu``` |
| AUR engedélyezése | ---- | ```sudo sed -Ei '/EnableAUR/s/^#//' /etc/pamac.conf``` |
| Telepítés | ```sudo apt install ttf-mscorefonts-installer``` | ```pamac build ttf-ms-fonts``` |

---

[Vissza](../README.md)
