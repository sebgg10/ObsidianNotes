## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
## Datos de acceso al nivel
**Usuario:** bandit24 
**Contraseña:** VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución

```
bandit24@bandit:~$ cd /tmp
bandit24@bandit:/tmp$ mkdir bandit24123
bandit24@bandit:/tmp$ cd bandit24123
bandit24@bandit:/tmp/bandit24123$ nano prueba1.sh
Unable to create directory /home/bandit24/.local/share/nano/: No such file or directory


Unable to create directory /home/bandit24/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit24@bandit:/tmp/bandit24123$ chmod u+x prueba1.sh
bandit24@bandit:/tmp/bandit24123$ ./prueba1.sh | nc localhost 30002 | grep -v "Wrong"
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
^C
bandit24@bandit:/tmp/bandit24123$ s
s: command not found
bandit24@bandit:/tmp/bandit24123$ ls
prueba1.sh
bandit24@bandit:/tmp/bandit24123$ nano prueba1.sh
Unable to create directory /home/bandit24/.local/share/nano/: No such file or directory


Unable to create directory /home/bandit24/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit24@bandit:/tmp/bandit24123$ ./prueba1.sh | nc localhost 30002 | grep -v "Wrong"
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.

```
## Notas adicionales
## Referencias