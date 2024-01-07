<h1 align="center">
<img src="../.pictures/visual-studio-code.png" alt="steam" width=64 />
</h1>

---

## visual studio code telepítése debian rendszerekre

> Telepítés

```
sudo apt update && sudo apt upgrade -y
```

```
sudo apt install software-properties-common apt-transport-https wget
```

```
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
```

```
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
```

```
sudo apt install code
```

```
sudo apt update && sudo apt upgrade -y
```

[Vissza](../README.md)
