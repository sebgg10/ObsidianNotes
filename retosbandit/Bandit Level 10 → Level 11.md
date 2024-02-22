## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.
## Datos de acceso al nivel
**Usuario:** bandit10
**Contraseña:** G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==" | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

bandit10@bandit:~$ python3
Python 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> cadena = open("data.txt").read()
>>> base64.b64decode(cadena)
b'The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM\n'
>>>
```
## Notas adicionales
Con " | base64 " se codifica y con " | base64 " se decodifica.
Se sale de python con ctrl + D
## Referencias