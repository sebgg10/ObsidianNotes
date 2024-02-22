## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
**Usuario:** bandit14
**Contraseña:** fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$ echo "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq" | nc localhost 30000
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

bandit14@bandit:~$ nc localhost 30000 <<< "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq"
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

```
## Notas adicionales
**nc**: Me permite conectarme o mandar algo a un puerto especifico.
## Referencias