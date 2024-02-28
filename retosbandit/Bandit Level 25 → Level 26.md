## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso al nivel
**Usuario:** bandit25
**Contraseña:** p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

```
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
bandit25@bandit:~$ ssh -oHostKeyAlgorithms=+ssh-dss -i bandit26.sshkey bandit26@localhost -p 2220
bandit26@bandit:~$ id
uid=11026(bandit26) gid=11026(bandit26) groups=11026(bandit26)
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ cat /etc/bandit_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
## Notas adicionales
## Referencias
https://velog.io/@certa/OverTheWire-Bandit-more-Trick-Level-25-Level-26