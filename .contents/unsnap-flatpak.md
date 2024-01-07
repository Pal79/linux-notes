<h1 align="center">
<img src="../.pictures/unsnap.png" alt="unsnap" width=128 />
</h1>

> snap csomagok listázása

```
snap list
```

> csomagok törlése ebben a sorrendben

```
sudo snap remove --purge firefox
sudo snap remove --purge snap-store
sudo snap remove --purge gnome-3-38-2004
```

```
sudo snap remove --purge gtk-common-themes
sudo snap remove --purge snapd-desktop-integration
sudo snap remove --purge bare
sudo snap remove --purge core20
sudo snap remove --purge snapd
```

```
sudo apt remove --autoremove snapd
```

> a snap végleges letiltása

```
sudo -H gedit /etc/apt/preferences.d/nosnap.pref
```

> beleírni a fájlba

```
Package: snapd
Pin: release a=*
Pin-Priority: -10
```

> a rendszer csomagok frissítése

```
sudo apt update
```

> a törlések után a megfelelő csomagok visszaállítása snap nélkül

```
sudo apt install --install-suggests gnome-software
```

> majd a Firefox telepításe PPA-ból

```
sudo add-apt-repository ppa:mozillateam/ppa
sudo apt update
sudo apt install -t 'o=LP-PPA-mozillateam' firefox
```

> firefox automatikus frissítésének bekapcsolása

```
echo 'Unattended-Upgrade::Allowed-Origins:: "LP-PPA-mozillateam:${distro_codename}";' | sudo tee /etc/apt/apt.conf.d/51unattended-upgrades-firefox
```

> majd létrehozok egy másik preferenciafájlt a Firefox számára, hogy magas prioritást biztosítson a Firefox számára, különben a rendszer automatikusan visszatelepíti a snap-et és egyéb csodás dolgait 

```
sudo -H gedit /etc/apt/preferences.d/mozillateamppa
```

> fájlba beleírni

```
Package: firefox*
Pin: release o=LP-PPA-mozillateam
Pin-Priority: 501
```


<h2 align="center">
<img src="../.pictures/flatpak.png" alt="flatpak" width=64 />
</h2>
### Flatpak telepítése

```
sudo apt install flatpak
```

> a továbbiakban, hogy ne kelljen mindig termiálból telepíten, hanem a csomagkezelőből is lehessen

```
sudo apt install gnome-software-plugin-flatpak
```

> Falthub engedélyezése

```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

> majd végül, újraindítás

```
sudo reboot
```

---

[Vissza](../README.md)
