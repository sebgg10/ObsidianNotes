## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**.
## Datos de acceso al nivel
**Usuario:** bandit7 
**Contraseña:** z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```
## Notas adicionales
**head:** Muestra las primeras 10 líneas.
**tail:** Muestra las últimas 10 líneas.
**wc -l:** Cuenta las líneas de un archivo.
**grep:** Filtra líneas en base a un patrón.
## Referencias