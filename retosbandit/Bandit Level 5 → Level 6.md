## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
## Datos de acceso al nivel
**Usuario:** bandit5
**Contraseña:** lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit5@bandit:~/inhere$ find . -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Notas adicionales
**ls -R:**
**find:** Busca archivos dentro de carpetas.
	**-redeable:** Que sea legible
	**-size:** El tamaño del archivo (c para bytes)
	**-type:** Tipo del archivo (f para archivo regular)
## Referencias
Manual de ayuda de find