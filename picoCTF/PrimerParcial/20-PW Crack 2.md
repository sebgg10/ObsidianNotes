## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución

```
sebgg10-picoctf@webshell:~$ ls
level2.flag.txt.enc  level2.py
sebgg10-picoctf@webshell:~$ nano level2.py 
sebgg10-picoctf@webshell:~$ python3 level2.py level2.flag.txt.enc 
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}

```
## Notas adicionales
## Referencias