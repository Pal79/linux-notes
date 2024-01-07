# Érintőkijelző

> Ha nem tudod érintéssel görgetni a webböngésző tartalmát:

> nyisd meg szerkesztésre a fájlt:

```
sudo nano /etc/security/pam_env.conf
```

> majd add hozzá a fájlhoz:

```
MOZ_USE_XINPUT2 DEFAULT=1
```

> mentés majd újraindítás

> vagy

> ha így sem működik, akkor nyisd meg a vebböngésződ és írd be:

```
about:config
```

> majd keresd meg ezt

```
dom.w3c_touch_events.enabled=2
```

> majd írd át:

```
dom.w3c_touch_events.enabled=1
```

> ezután indítsd újra a rendszert.

---

[Vissza](../README.md)
