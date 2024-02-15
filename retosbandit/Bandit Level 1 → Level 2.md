## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de acceso al nivel
**Usuario:** bandit1
**Contraseña:** NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
**Servidor:** bandit.labs.overthewire.org
## Solución

*Primer intento erróneo*
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$
```

 *Solución correcta*
```
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```
## Notas adicionales
Si se le agrega un "-"  a un cat, estará esperando un argumento, se debe agregar una ruta para que lo detecté como un archivo, puede ser completa o no.
## Referencias
[Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)