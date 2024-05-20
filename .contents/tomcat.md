# Tomcat

---

| Leírás | Parancs |
| :----- | :------ |
| Letöltés | ```https://tomcat.apache.org/download-90.cgi``` |
| Könyvtár létrehozás | ```sudo mkdir /opt/tomcat``` |
| Letöltött fájl kicsomagolása a létrehozott könyvtárba | ```sudo tar -xvf tomcat.tar.gz -C /opt/tomcat/ --strip-components=1``` |
| Tomcat indítása | ```sudo /opt/tomcat/bin/startup.sh``` |
| Ellenőrzés | ```localhost:8080``` |
| Tomcat leállítása | ```sudo /opt/tomcat/bin/shutdown.sh``` |
