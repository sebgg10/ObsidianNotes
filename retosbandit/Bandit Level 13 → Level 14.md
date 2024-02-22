## Objetivo
## Datos de acceso al nivel
**Usuario:** bandit13
**Contraseña:** wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ file sshkey.private
sshkey.private: PEM RSA private key
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
bandit14@bandit:~$ cat /etc/bandit_pass/dandit14
cat: /etc/bandit_pass/dandit14: No such file or directory
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

```
## Notas adicionales
## Referencias