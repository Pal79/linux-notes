---

# Gimp

---

| Telepítés típusa | Leírás | Parancs |
| :--------------- | :----- | :------ |
| snap telepítés | Telepítés | ```sudo snap install gimp``` |
|  |  |  |
| ppa telepítés | csomag hozzáadsása a repo-hoz | ```sudo add-apt-repository ppa:ubuntuhandbook1/gimp``` |
|  | csomagtároló frissítése | ```sudo apt update``` |
|  | telepítés | ```sudo apt install gimp``` |
|  | eltávolítás | ```sudo apt install ppa-purge``` |
|  | csomag törlése a repo-ból | ```sudo ppa-purge ppa:ubuntuhandbook1/gimp``` |
|  | ha a gimp nem indul el | ```sudo apt remove gimp``` |
|  | csomagtároló fissítése | ```sudo apt update``` |
|  | teljes eltávolítás függőségekkel együtt | ```sudo apt purge gimp libgegl* libbabl*``` |
|  | telepítés | ```sudo apt install gimp``` |

---

[Vissza](./../README.md)
