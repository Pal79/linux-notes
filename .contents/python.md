<h1 align="center">
<img src="../.pictures/python.png" alt="python logo" width=64 />
</h1>

---

## Python telepítése arch rendszeren:

> python verzió ellenőrzése

```
python --version
```

> Ha esetleg nincs telepítve

```
sudo pacman -S python
```

### pip telepítése

```
sudo pacman -S python-pip
```

### tkinter telepítése

```
sudo pacman -S tk
```

### pip telepítési beállítás

```
mkdir -p ~/.config/pip && nano ~/.config/pip/pip.conf
```

> majd ezt a fájlba írni

```
[global]
break-system-packages=true
```

### pip csomagok telepítése

```
pip install pandas
pip install pyperclip
pip install selenium
pip install requests
pip install twilio
pip install bs4
pip install spotipy
pip install webdriver-manager
pip install flask
pip install Flask-WTF
pip install Werkzeug
```

---

[Vissza](../README.md)
