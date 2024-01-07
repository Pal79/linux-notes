<h3 align="center">
<img src="../.pictures/java.png" alt="java" width=64 />
</h3>

---

> Telepítés debian rendszeren:
   > jelen esetben a 17-es java-t telepítem

```
sudo apt install openjdk-17-jre
sudo apt install openjdk-17-jdk
```

---

> JAVA_HOME

> Terminálban írd ezt (a * helyére a java verziószáma megy):

```
export JAVA_HOME="/usr/lib/jvm/java-*-openjdk-amd64"
export PATH="$PATH:$JAVA_HOME/bin"
```

> ellenőrzés:

```
echo $JAVA_HOME
echo $PATH
```

> ha nincs meg a JAVA_HOME:

```
sudo nano /etc/profile.d/jdk_home.sh
```

> ezeket a sorokat beleírni:

```
#! /bin/bash

export JAVA_HOME=/usr/lib/jvm/java-1*-openjdk-amd64"
export PATH="$JAVA_HOME/bin:$PATH"
```

> **ctrl+x -> y -> [enter]**

---

### java telepítése és beállítása arch rendszeren

> java verzió ellenőrzése

```
java -version
```

> vagy

```
which java
```

> elérhető java verziók listázása

```
sudo pacman -sS java | grep jre
```

> LTS verziók telepítése

```
sudo pacman -S jre8-openjdk
sudo pacman -S jdk8-openjdk
sudo pacman -S jre11-openjdk
sudo pacman -S jdk11-openjdk
sudo pacman -S jre17-openjdk
sudo pacman -S jdk17-openjdk
sudo pacman -S jre21-openjdk
sudo pacman -S jdk21-openjdk
```

> java státusz

```
archlinux-java status
```

> alapértelmezett java verzió kiválasztása

```
sudo archlinux-java set java-17-openjdk
```

> alapértelmezett java deaktiválása

```
sudo archlinux-java unset java-17-openjdk
```

> automatikus alapértelmezett java kiválasztása

```
sudo archlinux-java fix
```

---

### Eltávolítás debian rendszeren

> Az összes Java-val kapcsolatos csomag eltávolítása (Sun, Oracle, OpenJDK, IcedTea plugins, GIJ):

```
dpkg-query -W -f='${binary:Package}\n' | grep -E -e '^(ia32-)?(sun|oracle)-java' -e '^openjdk-' -e '^icedtea' -e '^(default|gcj)-j(re|dk)' -e '^gcj-(.*)-j(re|dk)' -e '^java-common' | xargs sudo apt-get -y remove
sudo apt-get -y autoremove
```

> Törli a konfigurációs fájlokat. Ez a parancs eltávolítja a libsgutils2-2 és a virtualbox konfigurációs fájljait is.

```
dpkg -l | grep ^rc | awk '{print($2)}' | xargs sudo apt-get -y purge
```

> Eltávolítja a Java konfigurációt és a gyorsítótár könyvtárát.

```
sudo bash -c 'ls -d /home/*/.java' | xargs sudo rm -rf
```

> Eltávolítja a kézzel telepített Jvm-eket.

```
sudo rm -rf /usr/lib/jvm/*
```

> Eltávolítja a Java bejegyzéseket és ha még vannak, az alternatívákat is.

```
for g in ControlPanel java java_vm javaws jcontrol jexec keytool mozilla-javaplugin.so orbd pack200 policytool rmid rmiregistry servertool tnameserv unpack200 appletviewer apt extcheck HtmlConverter idlj jar jarsigner javac javadoc javah javap jconsole jdb jhat jinfo jmap jps jrunscript jsadebugd jstack jstat jstatd native2ascii rmic schemagen serialver wsgen wsimport xjc xulrunner-1.9-javaplugin.so; do sudo update-alternatives --remove-all $g; done
```

A lehetséges fennmaradó Java könyvtárak keresése.

```
sudo updatedb
sudo locate -b '\pack200'
```

---

[Vissza](../README.md)
