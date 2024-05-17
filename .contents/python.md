<h1 align="center">
<img src="../.pictures/python.png" alt="python logo" width=64 />
</h1>

---

|     | Ubuntu | Manjaro |
| :-- | :----- | :------ |
| Python ellenőrzés | python3 --version | python --version |
| Python telepítése | sudo apt install python3 | sudo pacman -S python |
|  |  |  |
| pip telepítése | sudo apt install python3-pip | sudo pacman -S python-pip |
| pip ellenőrzése | pip --version | pip --version |
|  |  |  |
| tkinter telepítése | sudo apt install python3-tk | sudo pacman -S tk |
|  |  |  |
| virtualenv telepítése | sudo apt install python3-venv | sudo pacman -S python-virtualenv |
| Virtuális környezet léterhozása | python3 -m venv .venv | python -m venv .venv |
| Virtuális környezet aktiválása | | source .venv/bin/activate | source .venv/bin/activate |
| Virtuális környezet deaktiválása | deactivate | deactivate |
|  |  |  |
| Csomag telepítése virtuális környezetbe | pip install packagename | pip install packagename |
| Csomag telepítése a "requirements.txt"-vel | pip install -r requirements.txt | pip install -r requirements.txt |

---

> érdemes ezt is megcsinálni:

```
mkdir -p ~/.config/pip && nano ~/.config/pip/pip.conf
```

> majd ezt a fájlba írni

```
[global]
break-system-packages=true
```

---

[Vissza](../README.md)
