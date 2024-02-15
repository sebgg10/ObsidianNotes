## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
**Usuario:** bandit8
**Contraseña:** TESKZC0XvTetK0S9xNwm25STk5iWrBvP
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc -l data.txt
1001 data.txt
bandit8@bandit:~$ sort data.txt
...
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```
## Notas adicionales
**sort:** Ordena las líneas alfabeticamente.
**uniq:** Filtra en base a un críterio.
	-c: Cuenta las ocurrencias.
	-u: Muestra solo las líneas únicas.
## Referencias