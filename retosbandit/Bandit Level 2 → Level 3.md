## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
**Usuario:** bandit2
**Contraseña:** rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
**Servidor:** bandit.labs.overthewire.org
## Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```
## Notas adicionales
Cat no entiende los espacios en el nombre de archivos, los detecta como archivos separados. Para solucionarlo se deberá colocar entre comillas o usar una "\" en cada espacio.
## Referencias
[Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)