## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel
**Usuario:** bandit3
**Contraseña:** aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
## Solución

```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Oct  5 06:19 .
drwxr-xr-x 3 root    root    4096 Oct  5 06:19 ..
-rw-r----- 1 bandit4 bandit3   33 Oct  5 06:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```
## Notas adicionales
El parámetro l en el comando ls muestra la información extra de los archivos listados y la a muestra los ocultos.
## Referencias