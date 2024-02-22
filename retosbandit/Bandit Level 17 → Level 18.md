## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**
## Datos de acceso al nivel
**Usuario:** bandit17
**Contraseña:** VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

archivo txt con llave privada. 
```
ssh -i "LaLlave.txt" bandit17@bandit.labs.overthewire.org -p 2220
```

**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución

```
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ wc -l passwords.old
100 passwords.old
bandit17@bandit:~$ wc -l passwords.new
100 passwords.new
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
## Notas adicionales
**bandit17@bandit:~$ cat /etc/bandit_pass/bandit17**: Ver passwords de los usuarios.
**diff**: Compara dos archivos y muestra las diferencias que hay.
## Referencias