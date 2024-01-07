<h1 align="center">
<img src="../.pictures/ssh.png" alt="ssh" width=64/>
</h1>

---

> ssh kulcs beállítása

```
ssh-keygen -t rsa -b 4096 -C "youremail@gmail.com"
```

```
eval "$(ssh-agent -s)"
```

```
ssh-add ~/.ssh/id_rsa
```

> publikus ssh kulcs kiíratása

```
cat ~/.ssh/id_rsa.pub
```

> majd a megjelenített kulcs kijelölése és másolása ide: github.com -> Settings -> SSH and GPG keys

---

### ha ezt az üzenetet kapod:

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
The fingerprint for the ED25519 key sent by the remote host is
SHA256:R+hosszú kód van ide írva :) .
Please contact your system administrator.
Add correct host key in /home/username/.ssh/known_hosts to get rid of this message.
Offending ECDSA key in /home/username/.ssh/known_hosts:5
  remove with:
  ssh-keygen -f "/home/username/.ssh/known_hosts" -R "192.168.1.1**"
Host key for 192.168.1.1** has changed and you have requested strict checking.
Host key verification failed.
```

> töröld a kulcsot

```
ssh-keygen -R <hostname>
```

> vagy

```
ssh-keygen -R 192.168.1.***
```

> ezután próbáld újra a kapcsolódást

---

[Vissza](../README.md)
